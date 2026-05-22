---
title: CROSS Canonical Round Configuration Schema
version: 0.1.0
date: 2026-05-22
license: CC0
status: Working draft. Initial specification.
companion_standards:
  - WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
related_documents:
  - CROSS-common-reporting-outcome-standards-schema-0_2_0.md
  - CROSS-grant-configurator-0_2_0.md
  - WALKRI-interface-specification-0_1_0.md
  - WALKRI-CROSS-boundary-0_1_0.md
  - WALKRI-canonical-form-field-profile-0_1_0.md
---

# CROSS Canonical Round Configuration Schema

Version 0.1.0 | 2026-05-22 | CC0

---

## Part I: Purpose and Scope

The CROSS Canonical Round Configuration Schema is the machine-readable format in which a CROSS-conformant round specification is expressed, stored, transported, and imported by grantee tools. It is the output of the CROSS Grant Configurator (CROSS-grant-configurator-0_2_0.md) at the Commit stage of the CLEAR lifecycle and the input to grantee Theory of Change tools, reviewer dashboards, and data analysis pipelines.

This document specifies the schema. It is a JSON Schema (draft-07) document with WALKRI extensions at the field level. CROSS governs the obligation architecture fields at the round level; WALKRI governs the criterion specification quality fields at the field level. The governing authority boundary is specified in WALKRI-CROSS-boundary-0_1_0.md.

**Format agnosticism.** The canonical format is the source of truth. It is not the rendering format for any specific form platform. Platform translators convert from this format to Fillout, Jotform, Typeform, KoBoToolbox, XLSForm, or any other rendering target. A translator must preserve all canonical fields; it may add platform-specific properties. Translators are platform responsibilities, not schema responsibilities.

**The CLEAR Commit stage.** Publishing a canonical round configuration is the Commit stage of the CROSS CLEAR lifecycle (Commit, List, Evaluate, Attest, Register). A round configuration published at the Commit stage before applications open is the authoritative coordination instrument for that round. Fields defined in a published round configuration may not be removed or relaxed without republication with a documented revision reason.

**The Round Import interface.** A canonical round configuration may be loaded by a grantee Theory of Change tool to guide the grantee in producing an obligation commitment that is structurally conformant to the round's published specification. The field-level x-walkri- properties tell the grantee tool what each field measures, what evidence is required, and what constitutes a conformant response.

---

## Part II: Top-Level Round Configuration Fields

The following fields constitute the CROSS obligation architecture at the round level.

### 2.1 Required Fields (All Obligation Modes)

| Field | Type | Description |
|---|---|---|
| `id` | string | Stable identifier for this round configuration. Recommended form: a slug or UUID that is stable across revisions. |
| `title` | string | Human-readable round name. |
| `schema_version` | string (semver) | Version of this schema used (e.g., `0.1.0`). |
| `obligation_mode` | enum | CROSS obligation mode: `build`, `change`, `retroactive`, or `compound`. |
| `gate_type` | enum | Gate this configuration governs: `entry-specification`, `milestone`, `completion`, or `continuation`. |
| `sections` | array | Ordered array of Section objects. See Part III. |

### 2.2 Optional Fields (All Obligation Modes)

| Field | Type | Description |
|---|---|---|
| `program` | string | Program or organization name. |
| `published_at` | string (ISO 8601) | Timestamp when this configuration was published as the authoritative round specification. |
| `evidence_standard` | enum | Minimum evidence strength required at the completion gate: `self-report`, `third-party-verifiable`, or `independent-review`. |

### 2.3 Conditional Fields

**`change_specification`** (required for `change` and `compound` obligation modes; null for `build` and `retroactive`):

| Field | Type | Description |
|---|---|---|
| `from_state` | string | The condition being addressed, stated measurably. |
| `from_state_source` | string | The named source from which the FROM state is drawn. Must be an external, verifiable source. |
| `to_state` | string | The target condition in the same units as `from_state`, at a stated time horizon. |
| `indicator` | string | The specific metric by which change is measured. |
| `indicator_operational_definition` | string | A definition precise enough for two independent parties to produce the same measurement. |
| `causal_mechanism` | string | The if-then argument connecting the funded intervention to the target condition. |
| `key_assumptions` | array of strings | The conditions that must hold for each link in the causal chain. Minimum two. |
| `evidence_threshold` | string | What constitutes proof that the change happened and proof that it did not. |
| `evaluation_timeline` | string | The time horizon at which the change claim is evaluated. |

**`components`** (required for `compound` obligation mode; null for all others):

An array of Component objects. Each component is a Build obligation whose completion contributes to the program-level Change claim.

| Field | Type | Required | Description |
|---|---|---|---|
| `id` | string | yes | Stable identifier for this component. |
| `name` | string | yes | Human-readable component name. |
| `obligation_mode` | enum | yes | Always `build` for components within a compound round. |
| `deliverable` | string | yes | The specific artifact this component produces. |
| `operational_definition` | string | yes | What the deliverable is, precisely enough to determine whether it exists and matches specification. |
| `completion_criteria` | string | yes | The binary test determining whether this component is complete. |
| `contribution_to_change` | string | yes | How completion of this deliverable advances the causal chain toward the program-level Change. A component that cannot answer this question is outside the causal chain. |
| `sections` | array | no | Section objects scoped to this component's application fields. |

---

## Part III: Section Schema

A Section groups fields that belong to the same logical part of the round. Sections may be scoped to a specific gate.

| Field | Type | Required | Description |
|---|---|---|---|
| `id` | string | yes | Stable identifier for this section. |
| `title` | string | yes | Human-readable section name. |
| `description` | string | no | Guidance text shown to applicants above the section. |
| `gate` | enum | no | Gate this section belongs to. When absent, the section applies to the gate declared at the round level. |
| `fields` | array | yes | Ordered array of Field objects. See Part IV. |

---

## Part IV: Field Schema

A Field is a JSON Schema property definition with WALKRI criterion specification properties added as vendor extensions using the `x-walkri-` prefix. WALKRI-extended fields remain valid JSON Schema: compliant validators ignore properties they do not recognize.

### 4.1 JSON Schema Base Properties

| Property | Type | Description |
|---|---|---|
| `id` | string | Stable field identifier, unique within the round configuration. |
| `label` | string | The field label shown to applicants. |
| `description` | string | Additional guidance text. Optional. |
| `type` | enum | JSON Schema type: `string`, `number`, `boolean`, or `array`. |
| `format` | string | JSON Schema format: `date`, `date-time`, `uri`, `email`. Optional. |
| `enum` | array | Valid values for single-select and multi-select fields. Each value must have a corresponding definition in `x-walkri-operational-definition.inclusion`. |
| `required` | boolean | Whether a response is required for submission. |
| `minLength` | number | Minimum character length for string fields. |
| `maxLength` | number | Maximum character length for string fields. |
| `minimum` | number | Minimum value for number fields. |
| `maximum` | number | Maximum value for number fields. |
| `pattern` | string | Regular expression constraint. The pattern must be documented in `x-walkri-operational-definition`. |
| `conditional_on` | object | Conditional display rule. Contains `field_id` (string) and `value` (string). |

### 4.2 WALKRI Criterion Specification Properties

These five properties are required for every field in a CROSS+WALKRI conformant round. A field missing any one of them is a WALKRI conformance failure, regardless of how complete the CROSS obligation architecture is. See WALKRI-canonical-form-field-profile-0_1_0.md for the full field-level reference.

**`x-walkri-criterion-intent`** (string, required)

A written statement of what this field measures, distinct from its label. Answers: what does a conformant response to this field tell us about the applicant?

**`x-walkri-operational-definition`** (object, required)

A complete definition of what qualifies and what does not qualify as a conformant response. Four sub-fields, all required:

- `inclusion`: What a qualifying response looks like. For `enum` fields: one definition per option. For text fields: scope and minimum content of a complete response.
- `exclusion`: What a non-qualifying response looks like. The string `"none"` is a valid documented assertion that no exclusion conditions exist. A blank field is an incomplete specification.
- `unit-of-analysis`: The unit being measured or described.
- `edge-case`: At least one edge case and its determination.

**`x-walkri-response-form-justification`** (string, required)

A written justification for why the chosen field type fits the criterion intent. A justification states why defined options (or free text, or a number) are the right response form for what this field measures, not merely what the field type does.

**`x-walkri-evidence-form`** (string, required)

The specific artifact type and access path that constitutes conformant evidence for this field. Not "evidence of X" but the specific form: "a URL to the LICENSE file in the root of a public repository" or "a Dune Analytics dashboard URL with the query returning results for the applicant's contract address."

**`x-walkri-compliance-threshold`** (object, required)

Required for all fields. When no external standard is referenced, carry `{"minimum-threshold": "none"}` as an explicit assertion. When an external standard is referenced, include: `standard-url`, `version-anchor`, `required-components`, `evidence-per-component`, and `minimum-threshold` (`all`, `minimum-N-of-M`, or `custom`).

### 4.3 WALKRI Audit Properties

**`x-walkri-verdict`** (enum: `instrument` | `label`, required)

The result of WALKRI audit for this field. A field satisfying all five criterion specification requirements at conformant quality is an `instrument`. A field missing or failing any one is a `label`. A label may not be published in a CROSS+WALKRI conformant round without a documented override and revision timeline.

**`x-walkri-specification-version`** (string, semver, required)

The version of this field specification. Enables downstream consumers to determine which definition governed the data collected in any given reporting period.

**`x-walkri-specification-date`** (string, ISO 8601 date, required)

The date this field specification was last revised.

---

## Part V: Obligation Mode Variants

### Build

`change_specification`: null. `components`: null. Sections collect the deliverable specification, completion criteria, and evidence form for the artifact being produced.

### Change

`change_specification`: required, all nine fields. `components`: null. Sections collect FROM state evidence, indicator methodology, and causal mechanism documentation alongside organizational identity and eligibility fields.

### Retroactive

`change_specification`: null. `components`: null. Sections collect prior work attribution, evidence of completion, and evidence of use or adoption.

### Compound

`change_specification`: required, all nine fields. `components`: required, minimum two components, each carrying `contribution_to_change`. Sections exist at the round level (program-level Change fields) and optionally at the component level (component-specific Build fields). Completing all Build components does not automatically constitute achieving the program-level Change. The two evaluation tracks are separate.

---

## Part VI: Worked Example (Minimal Build Round)

The following is a minimal conformant round configuration for a Build obligation round. Field specification properties are abbreviated for readability; a conformant implementation carries the full values.

```json
{
  "id": "example-build-round-001",
  "title": "Developer Tooling Grant Round 1",
  "program": "Example Foundation",
  "schema_version": "0.1.0",
  "published_at": "2026-05-22T00:00:00Z",
  "obligation_mode": "build",
  "gate_type": "entry-specification",
  "evidence_standard": "third-party-verifiable",
  "change_specification": null,
  "components": null,
  "sections": [
    {
      "id": "org-identity",
      "title": "Organizational Identity",
      "gate": "entry-specification",
      "fields": [
        {
          "id": "legal-entity-name",
          "label": "Legal entity name and jurisdiction",
          "type": "string",
          "required": true,
          "minLength": 5,
          "x-walkri-criterion-intent": "Establishes the legal identity of the applying entity for accountability and cross-program identity matching.",
          "x-walkri-operational-definition": {
            "inclusion": "The name of the natural person or registered organization exactly as it appears in the relevant jurisdiction of registration, followed by the jurisdiction name. Example: 'Acme Protocol Ltd., Delaware, USA'.",
            "exclusion": "Project names, display names, or GitHub organization names that are not also the legal name. Exception: if no legal entity exists, the applicant states this explicitly and names the accountable individual.",
            "unit-of-analysis": "One legal entity per response.",
            "edge-case": "An unincorporated collective: must state 'No legal entity. Accountable individual: [full name].' This satisfies the field."
          },
          "x-walkri-response-form-justification": "Free text with no fixed-option constraint because legal names and jurisdictions vary in length and form. A dropdown cannot capture the full name-plus-jurisdiction as a combined response without truncation or omission.",
          "x-walkri-evidence-form": "The legal name as it appears in a public registration record. Program verifies against a public registry where available.",
          "x-walkri-compliance-threshold": {
            "minimum-threshold": "none"
          },
          "x-walkri-verdict": "instrument",
          "x-walkri-specification-version": "0.1.0",
          "x-walkri-specification-date": "2026-05-22"
        }
      ]
    }
  ]
}
```

---

## Part VII: Translator Contract

A platform translator converts from this canonical format to a specific form rendering platform's import format.

**Preservation requirements.** A translator must preserve: the field identifier (`id`), the verdict (`x-walkri-verdict`), all five criterion specification properties, the specification version and date, and the round-level obligation architecture (obligation_mode, gate_type, change_specification, components). Properties that a target platform cannot render natively must be preserved as metadata fields, not discarded.

**Addition permissions.** A translator may add platform-specific properties required for rendering. Platform properties do not override canonical properties; where a conflict exists, the canonical property governs.

**Label enforcement.** A translator must not silently publish a field carrying `x-walkri-verdict: "label"`. The operator must be informed before the configuration is submitted to the platform.

**Round-level fields.** A translator that converts only the field sections must also produce a separate machine-readable export of the round-level obligation architecture (obligation_mode, change_specification, components) so that the canonical round specification is not lost in translation.

---

## Changelog

| Version | Date | Changes |
|---|---|---|
| 0.1.0 | 2026-05-22 | Initial specification. |
