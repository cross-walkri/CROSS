---
title: Allo Protocol Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-16
license: CC0
standards: CROSS v0.3.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - Allo Protocol v2 (github.com/allo-protocol/allo-v2)
  - Allo Registry (on-chain profile system)
  - Gitcoin (gitcoin.co)
programs: Gitcoin, Octant, direct grants programs on EVM-compatible chains
---

# Allo Protocol Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

Allo Protocol and CROSS+WALKRI operate at different layers of the grants stack and address different problems. Allo is on-chain financial infrastructure: it manages pool creation, application submission, fund allocation, and distribution across multiple EVM-compatible chains. CROSS is the obligation architecture layer: it specifies what applicants must demonstrate at each gate, what evidence standards apply, and how reviewers must document their determinations. WALKRI is the field specification quality layer: it specifies how the application fields that collect those demonstrations must be designed.

Allo has no obligation specification layer. It records that applications were submitted and funds were distributed; it carries no specification of what applicants were required to demonstrate, at what evidence level, or how reviewers assessed eligibility. This is precisely the gap CROSS addresses. A program running Allo handles financial mechanics through the protocol while CROSS governs the accountability architecture above it.

---

## What Allo Protocol Is

Allo Protocol v2 is an open-source smart contract system for creating and managing grants pools on EVM-compatible chains. It is the infrastructure layer underlying Gitcoin Grants and is available for any program to deploy independently.

Allo Protocol's primary components:

The **Registry** is Allo's on-chain organizational profile system. Any entity can create a Profile in the Registry, which establishes an anchor address and an owner. The Profile is the persistent on-chain identity record for a grantee across pools and programs. A Profile owner can manage team members and apply to any Allo pool.

The **Allo Core Contract** manages Pool creation, application submission, and fund distribution. A Pool is an instance of a specific allocation strategy funded with an initial deposit. Pool managers configure the pool parameters, open and close the application window, and trigger distribution.

**Strategies** are modular smart contracts that implement allocation logic. Allo v2 separates the pool mechanics (handled by Allo Core) from the allocation decision (handled by the Strategy). Standard strategies include Quadratic Funding (QF), Direct Grants (manual review and allocation), and Donation Voting. Programs can deploy custom strategies. The strategy does not specify what applicants are obligated to demonstrate; it specifies how approved applications receive funds.

**Applications** are on-chain events linking a Profile (organizational identity) to a Pool (round). The application event records the submission; the Strategy determines eligibility, approval, and allocation.

---

## What Allo Protocol Does Not Provide

Allo is financial infrastructure. It is deliberately silent on obligation architecture: what applicants must demonstrate at entry, what evidence must accompany progress claims, what criteria govern completion determination, and what the accountability record of a funded cycle must contain.

This silence is appropriate at the protocol level. Allo is designed to be obligation-agnostic: any type of grant program, with any accountability standards, can run on Allo. But the obligation-agnosticism at the protocol layer means that every program running on Allo must define its own obligation architecture above the protocol. CROSS provides that architecture.

Allo also has no field specification quality layer. The application form fields that collect applicant information in an Allo-based program have no structural requirement for criterion intent, operational definition, evidence form, or compliance threshold. A program can publish any application form, with any level of definitional clarity, over any Allo pool. WALKRI addresses this at the data collection layer above Allo.

---

## Layer Architecture

An Allo-based program with CROSS+WALKRI conformance operates across three distinct layers:

**Allo Protocol layer (on-chain financial mechanics):** Pool creation and parameterization, application submission and anchoring, strategy-governed allocation, fund distribution. This layer handles all financial state transitions.

**CROSS layer (obligation architecture, off-chain specification):** Round configuration specifying obligation mode, gate architecture, evidence scope and strength requirements at each gate, indicator specification requirements, Theory of Change pathway registry, and publication requirements. The CROSS round specification governs what applicants must demonstrate; Allo records when they submit and whether they receive funds.

**WALKRI layer (field specification quality, off-chain instrument design):** Criterion specification requirements for each application field before any pool opens. A WALKRI audit ensures that the fields collecting applicant demonstrations are defined precisely enough to produce reliable, comparable data rather than open-ended text with definitional variance across respondents.

These layers are independent and additive. A program running Allo without CROSS+WALKRI has financial mechanics but no obligation architecture. A program with CROSS+WALKRI without Allo has an accountability specification but must use a different infrastructure layer for financial mechanics. A program with all three has the complete stack.

---

## Data Model Mapping

### Pool and Round Configuration

| Allo Concept | CROSS Equivalent | Notes |
| :-- | :-- | :-- |
| Pool | Round Configuration | An Allo Pool is the on-chain financial container. A CROSS Round Configuration is the accountability specification governing what applicants must demonstrate. A conformant program has both: the Pool is the on-chain anchor; the CROSS specification governs the obligation architecture. |
| Pool manager | Program operator (CROSS Cohort 1) | The entity that configures the Pool and triggers distribution. CROSS specifies the obligations that Pool manager must publish before the pool opens. |
| Strategy | Allocation mechanism | The Strategy determines how funds are allocated among approved applications. CROSS specifies what makes an application approvable; the Strategy specifies how approved applications receive shares of the pool. A CROSS-informed strategy could gate QF participation on gate passage rather than pure quadratic weighting. |
| Pool funding token and amount | Award pool | |
| Application window open/close | Entry gate publication date | CROSS requires full question list and plain-language summary publication before the application window opens. |

### Profile and Organizational Identity

| Allo Concept | CROSS Equivalent | Notes |
| :-- | :-- | :-- |
| Registry Profile | Organizational identity declaration | The Allo Registry Profile is the persistent on-chain identity record. CROSS's organizational identity declaration requires legal entity name, jurisdiction, representative, and prior round history. An Allo Profile anchor address can serve as the on-chain identity anchor for the CROSS declaration; the Profile's prior application history across pools is independently verifiable corroboration for CROSS's prior round history requirement. |
| Profile anchor address | Legal entity on-chain anchor | The Allo anchor address is deployed as a deterministic contract per Profile, providing a stable on-chain identity that persists across pools and programs. |
| Profile owner and members | Legal entity and contributors | Allo Profile members are the contributor team associated with the organizational identity. These correspond to the contributors listed in CROSS's organizational identity declaration. |

### Application and Gate

| Allo Concept | CROSS Equivalent | Notes |
| :-- | :-- | :-- |
| Application submission | Entry gate submission | The Allo application event anchors the submission on-chain. CROSS's entry gate specifies what the submission must contain, what evidence it must carry, and what baseline documentation is required for change-obligation programs. |
| Strategy eligibility review | Entry gate determination | The Strategy governs eligibility; CROSS specifies the entry gate criteria that the eligibility review must assess. |
| Fund allocation and distribution | Completion gate trigger | In standard Allo programs, distribution follows the allocation round. In a CROSS-conformant program, distribution at each stage should correspond to a gate determination, not purely to the allocation round close. |
| Application metadata URI | Round specification reference | Allo applications include a metadata URI (typically an IPFS pointer) for application data. This URI can reference the CROSS round specification document and the WALKRI field definitions, making the accountability specification available to any party that resolves the application record. |

---

## Integration Patterns

### Pattern 1: CROSS Round Specification Published Before Pool Opens

The CROSS round configuration document is published before the Allo Pool opens its application window. The Pool's metadata URI or a documented reference links the Pool to the CROSS round specification. Any party resolving the Pool's on-chain record can retrieve the accountability specification governing the round.

The round specification includes: obligation mode, gate architecture, evidence scope and strength at each gate, indicator specification requirements, plain-language summary, and full question list. The Allo Pool opens only after all WALKRI field specification requirements are satisfied for every application field.

### Pattern 2: Gate-Triggered Distribution

Standard Allo programs distribute at round close after QF matching or direct grant approval. A CROSS-conformant program configures distribution to correspond to gate passage rather than simple round close.

For multi-gate programs (change-obligation or build-obligation with progress and completion gates), Allo's strategy can be configured to release tranches at gate passage. The strategy encodes the tranche schedule; CROSS specifies the gate criteria that trigger each tranche. The Allo on-chain record then carries both the financial event and a reference to the gate determination that triggered it.

### Pattern 3: Allo Profile as Prior History Verification

CROSS requires returning applicants to disclose prior round history: which programs they applied to, under which Profile, with what outcome. The Allo Registry provides independently verifiable prior history: any party can query a Profile's application history across all Allo pools, including which pools funded the Profile and which did not.

A CROSS-conformant program running on Allo should treat the applicant's Allo Profile history as a corroboration source for the prior round history field. Where a prior application exists in the Registry but is not disclosed in the CROSS declaration, this is a material discrepancy in the organizational identity declaration.

### Pattern 4: WALKRI Calibration Before Pool Opens

The application fields in any Allo-based program exist at the form layer above the protocol. A Gitcoin-style program may use a dedicated form tool to collect application data that feeds into Allo; a direct grants program may use any form infrastructure. WALKRI calibration applies to these fields regardless of which form tool sits above Allo.

Before the Pool opens its application window, each application field must satisfy the WALKRI criterion specification requirements: criterion intent, operational definition, response form justification, evidence form, and compliance threshold. A field that does not satisfy all five requirements is flagged. The Pool opens only after all flags are resolved or documented.

---

## What This Integration Enables

A CROSS+WALKRI-conformant program running on Allo Protocol produces a complete grants record across three independently verifiable layers:

**Allo Protocol provides:** On-chain anchoring of organizational identities (Registry Profiles), application submission records, allocation decisions, and fund distribution. This layer is publicly auditable by any party without access to off-chain records.

**CROSS provides:** The accountability specification: what obligation mode applies, what applicants must demonstrate at each gate, what evidence standards govern those demonstrations, what the funder's determination must document, and what machine-readable outputs the round must produce. This is the layer that makes the Allo application record meaningful rather than merely anchored.

**WALKRI provides:** Data quality assurance that the application fields collecting CROSS-required demonstrations are precisely enough defined to produce reliable, comparable data across the applicant cohort. This is the layer that makes the data produced by the round usable for portfolio analysis rather than requiring retrospective harmonization.

Together: a program can demonstrate to institutional funders that its financial mechanics are on-chain and publicly verifiable (Allo), its obligation architecture meets published accountability standards (CROSS), and its application data is reliably comparable across grantees and rounds (WALKRI). No single layer provides all three claims.

---

## Adoption Guidance

Programs currently running Allo Protocol and adopting CROSS+WALKRI should:

1. Publish a CROSS round configuration document before the Allo Pool opens. Reference the document from the Pool's metadata URI so the accountability specification is retrievable by any party resolving the on-chain Pool record.

2. Require WALKRI calibration for all application fields before opening the Pool's application window. Any field that does not satisfy the five criterion specification requirements must be remediated or the deficiency documented before applicants see it.

3. Configure the Pool strategy to correspond gate passage to distribution events where the program architecture allows. For direct grants programs, this is the most straightforward integration: each grant tranche releases at a documented gate determination.

4. Treat the Allo Registry Profile as a corroboration source for the organizational identity declaration and prior round history fields. A Profile's application history across Allo pools is independently verifiable and should be checked against the declared prior round history.

5. For programs using Gitcoin's grants infrastructure (which runs on Allo), the CROSS round configuration and WALKRI field calibration can be produced using any tool or system; the Allo Protocol layer does not constrain the off-chain specification.

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

Allo Protocol v2: github.com/allo-protocol/allo-v2

Allo Protocol documentation: docs.allo.gitcoin.co

License: CC0
