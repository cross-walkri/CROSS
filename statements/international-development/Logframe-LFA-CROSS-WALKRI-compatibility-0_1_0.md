---
title: Logframe / LFA Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-16
license: CC0
standards: CROSS v0.3.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - Logical Framework Approach (LFA) - OECD DAC Sourcebook on Managing for Development Results
  - EC DEVCO Project Cycle Management Guidelines (2004)
  - DFID How To Note on Logframes (2011)
  - USAID ADS 203 Assessing and Learning
---

# Logframe / Logical Framework Approach Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

A CROSS+WALKRI-conformant program satisfies Logical Framework Approach (LFA) documentation requirements as a structural consequence of conformance. Programs that implement CROSS for obligation architecture and WALKRI for field specification quality produce Logframe-compatible documentation without additional work.

CROSS+WALKRI extends the Logframe in two directions the Logframe itself does not address: it adds build-obligation and retroactive-obligation modes for interventions the Logframe's change-oriented structure cannot specify, and it applies the precision obligations the Logframe places on grantees' indicator specifications to the collection instruments that funders design. Both extensions are backward-compatible: an existing Logframe-based program can adopt CROSS+WALKRI without abandoning its Logframe documentation.

---

## What the Logframe Is

The Logical Framework Approach is the dominant obligation architecture in international development programming. USAID, DFID, the European Commission, UN agencies, bilateral donors, and most major foundations use some variant of it. The Logframe was developed in the 1970s as a structured planning and management tool; it has since become a near-universal reporting requirement in the institutional development sector.

The Logframe matrix organizes a program's causal theory in four rows and four columns.

**The four rows (the causal hierarchy, from bottom to top):**

- **Activities**: the actions undertaken to produce outputs. What the program does.
- **Outputs**: the direct, tangible products of activities. What the program produces.
- **Purpose (Outcome)**: the change expected from the outputs in the target population or system. What the program is designed to achieve.
- **Goal (Impact)**: the higher-level objective the project contributes to. What the program's purpose serves at the broader societal or systemic level.

**The four columns:**

- **Narrative summary**: a description of what is to be achieved at each row level.
- **Objectively Verifiable Indicators (OVIs)**: measurable indicators showing achievement at each level.
- **Means of Verification (MoV)**: sources and methods for collecting indicator data at each level.
- **Assumptions**: external conditions that must hold for the causal logic between rows to function.

The causal logic of the Logframe runs as follows: if inputs are available and activities are implemented (given the activity-level assumptions), then outputs will be produced. If outputs are produced (given the output-level assumptions), then the purpose will be achieved. If the purpose is achieved (given the purpose-level assumptions), then the program will contribute to the goal.

---

## CROSS Mapping to the Logframe

### Row Mapping

| Logframe Row | CROSS Equivalent | Notes |
| :-- | :-- | :-- |
| Goal | Long-term Outcome or Goal (ToC hierarchy, Part IX-B) | CROSS's program-level ToC declaration distinguishes Long-term Outcomes from the Goal; the Logframe typically collapses these into one row. Both are addressed. |
| Purpose (Outcome) | Short-term Outcome or Intermediate Outcome (ToC hierarchy); Change-obligation entry specification (FROM state / TO state, Part IV) | Change-obligation grants are purpose-level interventions: they specify a measurable shift in a defined population. The FROM state is the Logframe's baseline OVI at the purpose row; the TO state is the target OVI. |
| Outputs | Output (ToC hierarchy); Build-obligation mode (Part III) | Build-obligation grants are output-level interventions: they specify a deliverable with independently verifiable completion criteria. Logframe does not have a named mode for this distinction; CROSS makes it explicit. |
| Activities | Process (ToC hierarchy) | Activities are outside CROSS's primary accountability scope; CROSS governs what must be demonstrated at each gate, not the internal process by which it is produced. |
| Inputs | Outside CROSS scope | Inputs (budget, personnel, resources) are recorded in the sufficiency architecture declaration but are not governed by CROSS gate logic. |

### Column Mapping

| Logframe Column | CROSS Equivalent | Notes |
| :-- | :-- | :-- |
| Narrative summary | Entry specification (obligation mode + FROM/TO state or deliverable specification, Part IV) | CROSS's entry specification is the machine-readable form of the Logframe's narrative summary at the relevant row level. |
| OVIs | 11-field indicator specification (Part V) | CROSS's indicator specification is a strict superset of OVI documentation requirements. See detail below. |
| Means of Verification | Data source and collection method (Part V, Field 8) + Evidence form (WALKRI Part III, Section 3.4) | CROSS specifies the data source and collection method per indicator. WALKRI specifies how the collection instrument must be designed to produce valid data from those sources. Together they produce more rigorous MoV documentation than the Logframe column typically contains. |
| Assumptions | Critical assumptions list in pathway registry (Part IX-B, Section 3) | CROSS's pathway registry requires explicit statement of critical assumptions at each causal link, following USAID ADS 201 requirements. These are the same assumptions the Logframe's fourth column captures, with the addition that CROSS requires them to be version-tracked rather than stated once at project design. |

---

## OVI Specification: CROSS as a Strict Superset

The Logframe's OVI column typically contains: an indicator name, a target value, and a baseline. These three elements are necessary conditions for an OVI; they are not sufficient for the data quality requirements that evaluation teams and audit bodies apply when assessing whether the OVI was properly measured.

CROSS's 11-field indicator specification satisfies the three Logframe OVI requirements and extends them with eight additional fields that address the precision gaps the Logframe leaves open:

| Logframe OVI Requirement | CROSS Field |
| :-- | :-- |
| Indicator name | Indicator name (Field 1) |
| Baseline | Baseline / FROM state (Field 10), with named data source and population |
| Target | Target / TO state (Field 11), in the same units as the baseline |
| (not in Logframe) | Rationale for indicator (Field 2) |
| (not in Logframe) | Measurement form and evidence classification (Field 3) |
| (not in Logframe) | Operational definition (Field 4) |
| (not in Logframe) | Construction and aggregation methodology (Field 5) |
| (not in Logframe) | Cumulative or non-cumulative designation (Field 6) |
| (not in Logframe) | Disaggregation (Field 7), with disaggregation ratchet |
| (not in Logframe) | Data source and collection method (Field 8) |
| (not in Logframe) | Data cost estimation (Field 9) |

A CROSS-conformant program produces OVI documentation at a level of rigor that satisfies both the Logframe requirement and the more demanding specifications required by OECD DAC evaluation criteria, USAID PIRS requirements, and donor audit standards. The Logframe requirement is a floor; CROSS's indicator specification exceeds it.

---

## Means of Verification: WALKRI Fills the Logframe Gap

The Logframe's MoV column specifies where indicator data will come from and how it will be collected. In standard practice, MoV entries are brief: "project monitoring reports," "household surveys," "government statistics." These entries identify the source but do not specify the collection instrument.

This is the Logframe's most significant accountability gap. A program that specifies "household survey" as its MoV has not specified: which questions the survey asks, how the questions are operationally defined, what response types are accepted, what evidence is required, or how the survey produces data that is comparable across rounds and reviewers. Two implementing partners using "household surveys" as their MoV may produce data that cannot be compared because their instruments were designed differently.

WALKRI addresses this gap directly. WALKRI's five criterion specification requirements apply to every field in the data collection instrument, including fields collecting OVI data for Logframe reporting:

| Logframe MoV Requirement | WALKRI Equivalent |
| :-- | :-- |
| Data source | Evidence form (Section 3.4): the specified artifact that satisfies the criterion, including document type, data source, and collection methodology |
| Collection method | Operational definition (Section 3.2): the complete definition of what counts, with counting rules and boundary conditions |
| (not in Logframe) | Criterion intent (Section 3.1): what the field actually measures, distinct from its label |
| (not in Logframe) | Response form justification (Section 3.3): why the response type is appropriate for the criterion |
| (not in Logframe) | Calibration record (Part V, Section 5.4): worked examples ensuring reviewer consistency across the collection |
| (not in Logframe) | Provenance fields (Part VII): field-level metadata enabling FAIR-compliant output |

A WALKRI-conformant collection instrument produces MoV-compatible documentation at the field level, making the Logframe's MoV column into a structured specification rather than a source reference.

---

## Assumptions: CROSS Extends the Logframe

The Logframe's assumptions column is typically filled in at project design and not updated systematically as the project progresses. It captures the causal conditions the project depends on but does not provide a mechanism for tracking whether those conditions are holding.

CROSS's pathway registry (Part IX-B, Section 3) requires a critical assumptions list for each declared pathway, following USAID ADS 201 requirements. These assumptions are version-tracked within the pathway registry rather than stated once. The continuation gate's sustainability assessment (Part IV) asks, at each stage transition, whether the conditions that were assumed at program design are still holding. This produces a dynamic assumptions record rather than a static one, which is the basis for the CLA-aligned adaptive management that major institutional funders increasingly require.

The critical assumptions list in CROSS corresponds directly to the Logframe's fourth column at the Purpose row (assumptions about what must be true for outputs to produce the purpose) and the Goal row (assumptions about what must be true for the purpose to contribute to the goal). CROSS additionally requires assumptions at the Output row level (what must be true for activities to produce the specified outputs), which the Logframe often treats as implicit.

---

## Three Modes vs. One: CROSS Extends Where Logframe Is Silent

The Logframe is structurally oriented toward change-obligation interventions. The narrative summary, the OVI column, the MoV column, and the assumption column are all designed around the question: did the project achieve the purpose it was designed to achieve? This works well for programs where the outputs are means to a measured change. It is poorly suited to two common grant types the Logframe does not address:

**Build-obligation grants**: interventions whose primary obligation is to produce a specified artifact (software, infrastructure, protocol, documentation) rather than a measured change in a population condition. Many technology-focused and open-source grants are build-obligation in character. The Logframe forces these into the same format as change-obligation grants, producing awkward purpose statements ("increased capacity to...," "strengthened infrastructure for...") that do not reflect the actual obligation. CROSS's build-obligation mode specifies these grants correctly without requiring the change-obligation framing.

**Retroactive grants**: interventions that reward demonstrated past contribution rather than specifying a prospective obligation. Retroactive public goods funding, recognition grants, and sustained infrastructure maintenance grants have no natural home in the Logframe's prospective structure. CROSS's retroactive-obligation mode provides a conformant structure for these.

Programs running Logframe-based monitoring for their prospective change-oriented work can adopt CROSS's build-obligation mode for their technology outputs and retroactive mode for any recognition grants without disrupting their Logframe documentation for the change-oriented components.

---

## OECD DAC Alignment

The Logframe was developed within the same OECD DAC framework that produced the six DAC evaluation criteria (Relevance, Coherence, Effectiveness, Efficiency, Impact, Sustainability). The Logframe's row structure maps to DAC criteria as follows:

| DAC Criterion | Logframe Row | CROSS Gate |
| :-- | :-- | :-- |
| Relevance | Purpose row: does the program address a real problem? | Entry specification gate: the FROM state must name a specific measurable condition |
| Coherence | Assumptions column: does the program complement other interventions? | Coherence disclosure (Part IX-A): applicants name related interventions and their relationship |
| Effectiveness | Purpose row OVIs: did the program achieve its purpose? | Completion verification gate: outcome evidence against baseline |
| Efficiency | Activities and Outputs rows: were resources well used? | Cost-effectiveness assessment at continuation gate |
| Impact | Goal row: did the program contribute to the higher-level goal? | Long-term Outcome register in program-level ToC (Part IX-B) |
| Sustainability | Assumptions at Purpose row: will the change persist? | Sustainability stance declaration at continuation gate |

A program that uses the Logframe and declares OECD DAC alignment in CROSS is not doing additional work: the Logframe already captures the structural elements DAC maps to, and CROSS's gate architecture enforces them at each decision point.

---

## Machine-Readable Output

The Logframe is a document. It lives in project files, donor submissions, and evaluation reports. It is not machine-readable, not interoperable across programs, and not aggregatable without significant manual effort by evaluation teams.

CROSS+WALKRI produces the same information in machine-readable, DAOIP-5-compatible format. A CROSS+WALKRI-conformant program's pathway registry is the Logframe in structured data: causal claims with assumptions, OVIs with full specification, MoV at the field level, and gate evidence that is version-tracked and cryptographically attributable in any format appropriate to the program's institutional context.

Programs that must submit traditional Logframe documentation to institutional donors can produce it from their CROSS+WALKRI-conformant data without additional work. The structured data contains all Logframe elements; the Logframe table is a formatted rendering of that data.

---

## Adoption Guidance

Programs that currently use the Logframe and are adopting CROSS+WALKRI should:

1. Map their existing Logframe rows to CROSS obligation modes. Purpose-row interventions are change-obligation; Output-row deliverables within those interventions are build-obligation. Where the program has mixed obligations across its portfolio, configure each component with the appropriate mode.

2. Use the 11-field CROSS indicator specification to complete and formalize each OVI in the existing Logframe. The existing OVI name, baseline, and target can be imported directly; the eight additional fields (rationale, operational definition, methodology, disaggregation, data source, data cost) fill in what the Logframe column left implicit.

3. Transfer the Logframe's assumptions column into CROSS's pathway registry as the critical assumptions list for each declared pathway. This makes the assumptions explicitly version-tracked and integrates them into the continuation gate assessment.

4. Apply WALKRI's criterion specification requirements to every field in the data collection instruments used to gather OVI data. This is the step that transforms the Logframe's MoV column from a source reference into a field-level specification.

5. Declare OECD DAC alignment as the measurement framework in the Grant Configurator. This pre-populates the external standards section with DAC criteria references and connects CROSS's gate architecture to the DAC evaluation vocabulary the program's institutional funders already use.

Programs that have not previously used the Logframe but are adopting CROSS+WALKRI will produce Logframe-compatible documentation as a structural consequence of conformance. The program-level ToC declaration (Part IX-B) generates the Logframe's narrative summary and row structure. The indicator specification (Part V) generates the OVI column. The WALKRI field specifications generate the MoV column. The pathway registry generates the assumptions column. No additional Logframe-specific documentation work is required.

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

OECD DAC LFA Sourcebook: oecd.org/dac/evaluation/daccriteriaforevaluatingdevelopmentassistance.htm

EC Project Cycle Management Guidelines: ec.europa.eu/europeaid/sites/devco/files/methodology-aid-delivery-methods-project-cycle-management-200403_en_2.pdf

License: CC0
