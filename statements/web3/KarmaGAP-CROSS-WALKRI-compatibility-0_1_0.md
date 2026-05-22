---
title: KarmaGAP Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-16
license: CC0
standards: CROSS v0.3.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - KarmaGAP (gap.karmahq.xyz)
  - Karma GAP SDK (github.com/show-karma/karma-gap-sdk)
  - Ethereum Attestation Service (attest.sh)
  - DAOIP-3 (DAOstar/Metagov Attestation Standard)
programs: Octant, Gitcoin, Arbitrum DAO, Optimism, Celo, Scroll, Lisk
---

# KarmaGAP Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

KarmaGAP and CROSS+WALKRI operate at different and complementary layers of the grants accountability stack. KarmaGAP provides cross-program project tracking, milestone visibility, and grantee reputation via Ethereum Attestation Service (EAS) on-chain attestations. CROSS provides the obligation architecture governing what funded interventions must demonstrate and at which gate. WALKRI provides the field specification quality layer governing how collection instruments must be designed.

Neither system replaces the other. A program running CROSS+WALKRI produces structured gate evidence that KarmaGAP milestone records can reference. A grantee registered in KarmaGAP provides independently verifiable prior history that CROSS's organizational identity declaration and prior work attribution requirements can use as a verification source. The two systems are most valuable when used together: CROSS+WALKRI governs the obligation architecture and data quality within a round; KarmaGAP provides the cross-program reputation layer that makes accountability visible across rounds and programs.

---

## What KarmaGAP Is

KarmaGAP (Grantee Accountability Protocol) is Karma's grants accountability platform. It tracks grants, milestones, and grantee activity across multiple programs on a shared registry. The platform is used by Octant, Gitcoin, Arbitrum DAO, Optimism, Celo, Scroll, Lisk, and comparable programs.

KarmaGAP is built on the Ethereum Attestation Service (EAS), a general-purpose on-chain attestation infrastructure. KarmaGAP uses a dual-attestation pattern: primary attestations define entities (Project, Grant, Milestone, Member, Community), and nested detail attestations contain the data payload for each entity. All attestations are chain-anchored and publicly verifiable.

**KarmaGAP's primary data entities:**

A **Project** represents a grantee's work. Project data includes: title, description, problem, solution, mission summary, location of impact, links, slug, tags, business model, stage, and funding raised. Projects are associated with members (contributor attestations), grants (funding records per program), milestones (deliverable commitments), and impacts (outcome records).

A **Grant** links a Project to a specific grant program's funding. Each Grant records the amount, the funding program (Community), and the project stage within that program.

A **Milestone** represents a deliverable commitment within a Grant. Milestone records include the milestone description, due date, and completion status. Milestone updates are separate attestations documenting progress or completion.

A **Community** represents a grant program in KarmaGAP. Octant, Gitcoin, Arbitrum, and others each operate as a Community. Communities contain Projects (grantees) and are the primary unit for cross-program accountability visibility.

---

## What KarmaGAP Does Not Provide

KarmaGAP does not have a program-level round configuration layer. There is no round entity, no obligation mode specification, no gate architecture, no evidence scope or strength classification, and no indicator specification. KarmaGAP tracks what grantees report having done; it does not specify what grantees are obligated to demonstrate, at what evidence level, or by which gate.

This is precisely where CROSS operates. CROSS's gate architecture (entry specification, progress verification, completion verification, continuation specification) provides the obligation structure that KarmaGAP's milestone tracking presupposes. A KarmaGAP milestone "completed" status is a grantee's self-report; CROSS specifies what evidence must accompany that report, at what strength level, and how a funder must assess it.

Similarly, KarmaGAP has no field specification quality layer. Milestone descriptions and impact records in KarmaGAP are freeform text entries with no operational definitions, no criterion intents, and no evidence form requirements. WALKRI addresses this gap at the data collection instrument level.

---

## Data Model Mapping

### Project Level

| KarmaGAP Field | CROSS+WALKRI Equivalent | Notes |
| :-- | :-- | :-- |
| Project title | Project name (entry specification) | |
| Problem | FROM state (change-obligation entry gate) | The KarmaGAP problem field is the narrative form of CROSS's structured FROM state. CROSS requires the problem to be stated as a specific measurable condition in a defined population with a named data source. KarmaGAP accepts free text. |
| Solution | TO state or deliverable specification | CROSS requires the solution to be stated as a specific measurable target (change-obligation) or a falsifiable deliverable (build-obligation). KarmaGAP accepts free text. |
| Stage | Project stage (drafting, submitted, active, reporting, completed) | CROSS's project stages map to KarmaGAP's stageIn field, but CROSS's stages are gate-governed while KarmaGAP's are self-reported. |
| Links | Project GitHub, website | |
| Tags | Domain tags from sufficiency architecture declaration | |
| Members | Legal entity + contributors from organizational identity declaration | KarmaGAP's member attestations provide cross-program verification of contributor identity, which is useful corroboration for CROSS's organizational identity declaration. |

### Grant Level

| KarmaGAP Field | CROSS+WALKRI Equivalent | Notes |
| :-- | :-- | :-- |
| Community | Round funder (CROSS program identifier) | |
| Grant amount | Award amount | |
| Grant status | Project stage within round | |
| Milestones | Gate deliverables and progress records | KarmaGAP milestones correspond to CROSS gate commitments. CROSS specifies the evidence scope and strength required at each milestone; KarmaGAP tracks the grantee's self-reported completion. |

### Milestone Level

| KarmaGAP Milestone Field | CROSS+WALKRI Equivalent | Notes |
| :-- | :-- | :-- |
| Milestone description | Gate completion criteria (entry specification) | CROSS's completion criteria are specified before the round opens and locked. KarmaGAP milestone descriptions are set by the grantee after award. A CROSS-conformant program should pre-populate KarmaGAP milestones from the CROSS gate configuration rather than allowing grantees to set them post-award. |
| Completion status | Gate completion verification record | KarmaGAP's completion status is a binary attestation. CROSS's completion verification gate is a structured assessment against published criteria with a documented funder determination. |
| Milestone updates | Progress verification gate evidence | KarmaGAP milestone updates are progress records. CROSS progress verification gates require evidence meeting a specified scope and strength level. |

---

## Attestation Layer Comparison

Both KarmaGAP and CROSS produce on-chain attestations, but through different mechanisms with different properties:

**KarmaGAP attestations** are EAS (Ethereum Attestation Service) attestations. They are chain-anchored, publicly verifiable, and schema-typed via schemaUID. Any address can create a KarmaGAP attestation; the platform does not require funder authentication. KarmaGAP attestations are designed for broad cross-program visibility and grantee self-sovereignty: a grantee can attest to their own milestones.

**CROSS gate attestations** are cryptographically attributed, publicly verifiable records signed by the funder at each gate. They carry structured gate evidence metadata: obligation mode, evidence scope, evidence strength, and funder determination. CROSS gate attestations require funder signature; they are not self-attested. They may be expressed in any verifiable format appropriate to the program's infrastructure, including W3C Verifiable Credentials, EAS attestations, signed institutional documents, or comparable mechanisms.

These are complementary, not competing. KarmaGAP EAS attestations provide the cross-program visibility layer: any consumer can see that this project received funding from Octant, completed milestone 2, and has prior history across four programs. CROSS gate attestations provide the structured accountability layer: the funder signed a determination that this completion met the published criteria at the specified evidence level. A CROSS+WALKRI-conformant program producing both types of records gives downstream consumers two independently verifiable records of the same accountability event.

The practical integration: a CROSS completion gate record can be referenced from a KarmaGAP milestone update attestation. The KarmaGAP record provides the cross-program visibility; the CROSS gate record provides the structured funder-signed verification. Consumer tools that understand EAS attestations can verify the KarmaGAP layer; tools that understand the CROSS gate schema can verify the obligation fulfillment layer. Both layers reference the same accountability event.

---

## KarmaGAP Registration and CROSS Identity Requirements

CROSS's organizational identity declaration requires applicants to disclose prior round history: whether they or any substantially overlapping entity has applied to this program in prior rounds, under what name, and with what outcome. KarmaGAP is the most comprehensive public registry of this information for Web3 grants programs.

Where a grantee has a KarmaGAP profile, that profile provides:
- Independent verification of prior grants received across programs
- Milestone completion history that can be reviewed against claimed track records
- Cross-program identity anchoring that validates the organizational identity declaration

CROSS-conformant programs should treat KarmaGAP registration as a recommended condition at the continuation gate for returning grantees: a grantee who received prior funding and has not registered in KarmaGAP has not created the cross-program accountability record that would allow independent verification of their track record claim.

This is not a requirement for entry gate eligibility, because requiring KarmaGAP registration before any applicant can receive funding would exclude first-time grantees. But at the continuation gate, a returning grantee who has not registered their prior grant in KarmaGAP has structurally withheld their accountability record from the cross-program commons.

---

## CROSS Milestone Configuration in KarmaGAP

The most common integration failure between KarmaGAP and CROSS-conformant programs is grantee-defined milestones. In standard KarmaGAP usage, grantees define their own milestone descriptions after receiving a grant. This produces milestones that reflect grantee intent rather than funder-specified gate criteria, making the milestone completion record difficult to assess against published standards.

A CROSS-conformant program running KarmaGAP should pre-populate milestone descriptions from the published gate configuration. The milestone description in KarmaGAP should state: the gate type (progress verification or completion verification), the evidence scope required, and the evidence strength required. This makes the KarmaGAP milestone record an externally verifiable statement of the CROSS gate configuration rather than a post-hoc grantee narrative.

Where Grants Forge is used for round configuration, it should export KarmaGAP-formatted milestone templates as part of its round specification output, enabling grantees to register the correct milestone structure in KarmaGAP at the time of award rather than defining their own.

---

## What This Integration Enables

A CROSS+WALKRI-conformant program running alongside KarmaGAP produces a layered accountability record that no system alone provides:

**KarmaGAP provides**: cross-program visibility, grantee reputation across the Web3 ecosystem, EAS-anchored milestone records publicly accessible to any consumer, and the historical record needed to verify track record claims in CROSS's organizational identity declaration.

**CROSS provides**: the obligation architecture specifying what must be demonstrated and at which gate, structured indicator data with operational definitions and baselines, funder-signed completion determinations, and the machine-readable round configuration that makes KarmaGAP milestone descriptions meaningful rather than self-defined.

**WALKRI provides**: the field specification quality layer ensuring that data collected through KarmaGAP-adjacent forms is reliable, comparable, and FAIR-compliant rather than freeform text with definitional variance across grantees.

Together: a grantee's KarmaGAP record provides the ecosystem-visible reputation layer; the CROSS gate records provide the structured obligation layer; the WALKRI field specifications provide the data quality layer. All three are necessary for a complete grants accountability picture.

---

## Adoption Guidance

Programs currently using KarmaGAP and adopting CROSS+WALKRI should:

1. Pre-populate KarmaGAP milestone descriptions from the CROSS gate configuration rather than allowing post-award grantee definition. Each KarmaGAP milestone should state the CROSS gate type, evidence scope, and evidence strength required.

2. Configure the continuation gate to require KarmaGAP registration and milestone completion records for returning grantees. This treats KarmaGAP's cross-program record as the independent verification of track record claims.

3. Link CROSS completion gate records from KarmaGAP milestone update attestations. This gives each milestone update a structured, funder-signed verification record alongside the grantee's self-reported completion. The gate record may be expressed in any verifiable format the program uses; the link from the KarmaGAP attestation to the gate record is what matters for interoperability.

4. Use KarmaGAP profiles as a corroboration source for CROSS's organizational identity declaration: prior grant history visible in KarmaGAP is independently verifiable confirmation of claims made in the prior round history field.

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

KarmaGAP: gap.karmahq.xyz

Karma GAP SDK: github.com/show-karma/karma-gap-sdk

Octant KarmaGAP community: gap.karmahq.xyz/community/octant

License: CC0
