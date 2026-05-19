---
title: CROSS+WALKRI Primitives Foundation
version: 0.1.4
date: 2026-05-19
license: CC0
status: Working draft. All provisions in CROSS and WALKRI are derived from or should be expressible as combinations of the primitives defined here. When a new provision cannot be derived from existing primitives, the missing primitive must be named and added here before the provision is written.
---

# CROSS+WALKRI Primitives Foundation

Version 0.1.4 | 2026-05-19 | CC0

---

## Purpose

This document is the canonical source for the primitives from which CROSS and WALKRI are built. A primitive in this system is a named concept that:

- Is defined precisely enough that other concepts can be derived from it
- Cannot itself be decomposed into simpler named concepts within this system
- Is used by reference in multiple provisions or contexts across the standards

Provisions in CROSS and WALKRI are applications of these primitives to specific contexts. When a provision cannot be derived from existing primitives, the gap identifies a missing primitive that belongs here, not a reason to invent a standalone provision. This discipline keeps the standards internally consistent and prevents example-driven accretion that produces redundancy, overlap, and conceptual drift.

The document is organized by conceptual layer, not by which standard a primitive first appeared in. Each primitive includes its definition, its relationships to other primitives, and the provisions it generates.

---

## Layer 1: Methodological Primitives

These primitives govern how the standards themselves are written, how terms are used, and how provisions are derived.

### Bidirectional Precision

The same operational definition rigor that obligation standards require of applicants specifying indicators must be applied by funders to the fields they use to collect those specifications. Precision obligations run in both directions: from funder to applicant and from applicant to funder.

**Relationships:** Generates the criterion specification requirement in WALKRI. Constrains gate criterion specification in CROSS Part IV. Is the foundational principle of WALKRI's entire field instrument architecture.

**Applications:** Every WALKRI criterion specification requirement. Every CROSS gate criterion specification requirement. The applicant identity field specification (Section 3.7 of WALKRI).

---

### Transclusion

A primitive defined once in a canonical location is included by reference wherever it applies, rather than restated. Restatement produces definitional drift; reference preserves consistency. This document exists to enable transclusion across CROSS and WALKRI.

**Relationships:** Governs how primitives relate to provisions. Enables the standards to grow without redundancy.

**Applications:** Every provision in CROSS and WALKRI that references a concept defined here rather than re-defining it.

---

### Frame Language: Pre-Replacement Admissibility

A Frame 1 term (a term that describes a mechanism of control, hierarchy, or extraction using normative or aspirational language that conceals its structural function) is admissible without replacement in seven cases: citation use (it is the official name of a specific external entity), detection use (it names the Frame 1 mechanism being identified through analysis), contextual description use (it accurately describes a Frame 1 system being referenced), developmental bridge use (it meets the reader at their developmental position before Frame 2 is established), naming the stage (it accurately names a developmental stage), communication medium use (it is necessary for structural purposes with a Frame 1 audience), and documentary record use (it appears in a quotation or cited source). In all other cases, replacement is required.

**Relationships:** Governs which terms require replacement in the standards and in applicant-facing documents. Pairs with the Frame 2 functioning check.

**Applications:** Term selection in CROSS and WALKRI provisions. Evaluation of applicant language in proposal narratives.

---

### Frame Language: Replacement Procedure Categories

When a Frame 1 term requires replacement, the replacement falls into one of four procedure categories: plain-English mechanism specification (describe what the mechanism actually does), technical corpus vocabulary (use the established term from the relevant technical field), deference claims (replace the normative claim with a claim structure that names the authority being deferred to and the conditions of that deference), or relational inversion (restructure the sentence to make the actual subject-object relationship visible).

**Relationships:** Pairs with pre-replacement admissibility. Generates specific replacement decisions for individual terms.

**Applications:** CROSS and WALKRI provision drafting. Frame Language skill.

---

### Frame Language: Frame 2 Functioning Check

A term or claim that has been expressed in Frame 2 vocabulary may still fail to function as Frame 2 in one of eight ways: Transcendence Claim (the language claims to escape the conditions it operates within), Declaration Exploit (the act of naming a commitment is treated as evidence of the commitment), Precision Facade (the language appears specific but the specificity does not carry operational content), Partial Instantiation (a Frame 2 structure is partially implemented while a Frame 1 assumption does the remaining work), Direction Without Destination (the language names motion toward a goal without specifying the goal), Vocabulary Without Architecture (Frame 2 terms are used without the structural requirements Frame 2 implies), Correct Map/Wrong Territory (Frame 2 language accurately describes a different context but not the one it is applied to), and Frozen Map (Frame 2 language that was accurate at specification has not been updated as conditions changed).

**Relationships:** Applies after replacement procedure has been applied. Catches provisions that use correct vocabulary but fail to function as intended.

**Applications:** Quality check on all CROSS and WALKRI provisions. Evaluation of applicant specification language.

---

## Layer 2: Identity Primitives

These primitives govern who is applying, what they are applying for, and whether they have sufficient resources.

### Entity Boundary

The declared boundary of a legal, operational, or organizational entity that determines what is inside (attributable to that entity) versus outside (attributable to other entities). Every identity, attribution, and scope question in CROSS+WALKRI is a question about entity boundaries.

Entity boundary has three states that must be declared:

The **applying entity**: the legal person or registered organization that is accountable for delivering the obligations and receiving disbursement. Its boundary is defined by its legal registration, governance structure, and scope of control over the work being proposed.

The **contributing entity**: the entity under whose resources, governance, or employment prior work was performed. Where a contributor exits an entity and subsequently applies for funding that cites work performed within that entity, the contributing entity's boundary is distinct from the applying entity's boundary. This distinction must be declared.

The **affiliated entity**: any entity that shares the applying entity's name, brand, key personnel, codebase, or user base without being legally identical to it. Affiliated entities may include parent organizations, chapters, working groups, spin-offs, or organizations that chose the same name independently.

**Relationships:** Generates the organizational identity declaration, the prior work attribution statement, and the applicant identity instrument in WALKRI. Constrains scope (you cannot claim scope beyond your entity boundary). Constrains sufficiency (sufficiency is measured within a declared entity boundary).

**Applications:** CROSS organizational identity declaration. CROSS prior work attribution statement. WALKRI Section 3.7 applicant identity instruments. Conflict of interest Tier 1 and Tier 2 classifications.

---

### Scope

The declared portion of an entity's full program or work portfolio that a specific application, grant, or obligation covers. Scope is always relative to an entity boundary: an entity may have multiple programs; a grant funds a specific scope within that entity.

Scope determines what outputs, outcomes, and evidence are attributable to a specific grant rather than to the entity's full operation. When an organization applies for funding of a specific aspect of its work (a particular program, a sub-entity, a specific deliverable within a larger effort), the scope of that application must be declared explicitly. Without a declared scope, evaluators cannot assess additionality, attribute outcomes, or determine whether multiple applications from related entities cover the same scope or different scopes.

Scope has a hierarchy: a grant may fund a specific deliverable (narrow scope) within a specific program (medium scope) within an entity's full operation (full scope). Declaring which level a grant covers determines what evidence is appropriate at the completion gate.

**Relationships:** Requires entity boundary to be declared first (you cannot declare scope without a declared entity). Determines what falls within concurrent funding disclosure (other sources covering the same scope). Constrains additionality (additionality is assessed at the declared scope, not at the entity level). Determines sufficiency position (sufficiency is assessed at the declared scope).

**Applications:** CROSS concurrent funding disclosure. CROSS additionality declaration. CROSS scope attribution. Funding ask field in any application. WALKRI applicant identity instruments.

---

### Sufficiency

The relationship between an entity's current resources at a declared scope and the resources required to fulfill the obligations at that scope completely. Sufficiency is a ratio, not a binary: a program may be at 40% sufficiency, approaching sufficiency, at sufficiency, or at surplus.

Sufficiency is declared per scope, not per entity overall. An entity operating multiple programs may be at sufficiency for some and critically underfunded for others. No grant program provides sufficiency on its own; organizations pursue sufficiency across multiple funding sources with different eligibility criteria, which is why partial-scope applications are legitimate and expected rather than signs of gaming. The sufficiency primitive gives organizations a standard form for declaring this architecture.

Sufficiency has four declared positions: **critical gap** (current resources cover less than half of what full scope operation requires, and the program's viability depends on closing this gap), **partial** (resources cover more than half but the program operates below intended capacity), **approaching** (resources are sufficient for current operations but not for the next intended scope expansion), and **surplus** (resources exceed current scope requirements and the entity is able to sustain the program without additional funding in the current period).

**Relationships:** Requires scope to be declared first. Connects to the continuation gate (sustainability assessment at continuation asks whether outcomes are sustained, conditional, or dependent, which is a downstream consequence of sufficiency position). Connects to the additionality declaration (what a grant adds to sufficiency at a declared scope). Connects to portfolio analysis (the sufficiency distribution across a funder's portfolio).

**Applications:** Funding ask field (what gap does this grant address at this scope). Continuation gate sufficiency assessment. Portfolio analysis sufficiency dimension. Additionality declaration.

---

### Revenue Architecture

The declared model by which the applying entity generates income outside of grants and donations. Four types:

**Grant-only**: the entity has no commercial revenue model and operates entirely from grants and donations. No fees are charged for access to outputs or services.

**Fee-for-service**: the entity charges fees for access to outputs or services, but these fees are below a level that constitutes a commercially self-sustaining revenue stream. The entity remains grant-dependent for its primary operational funding.

**Commercial**: the entity generates material income through a commercial revenue model, whether licensing, subscription fees, per-transaction fees, advertising, or equivalent mechanisms. The entity is commercially viable independent of grant funding for at least some portion of its operations.

**Hybrid**: the entity operates a commercial product or revenue stream alongside a separately scoped public goods program. The grant application covers specifically the non-commercial scope, which the commercial revenue does not fund.

**Relationships:** Revenue architecture determines what additionality means for this applicant. A grant-only entity has full additionality for any non-duplicative grant: the grant funds work that would not otherwise occur. A commercial entity must specifically delineate the public goods scope that commercial revenue does not cover, because the additionality argument cannot rest on grant-only logic when commercial revenue exists. This is the anchor for the additionality declaration in CROSS Part VI-A. Revenue architecture is distinct from sufficiency position (which describes the current resource level at a declared scope) and from concurrent funding disclosure (which lists specific prior grants and investments). A commercially viable entity may hold a surplus sufficiency position from commercial revenue while still having a legitimate public goods grant ask for a specifically non-commercial scope.

**Applications:** CROSS Part II revenue architecture dimension. CROSS Part IV sufficiency architecture declaration (revenue architecture is required alongside the four sufficiency elements). CROSS Part VI-A additionality declaration (commercial and hybrid entities must specifically delineate the non-commercial scope). Evaluator sufficiency assessment.

---

### Disbursement Authority

The named person or persons who have legal authority to receive grant funds on behalf of the applying entity and approve their deployment, together with the mechanism by which that authority is exercised. Three states:

**Individual**: a single named person holds full authority to receive and deploy funds on behalf of the entity, acting on their own judgment without a required approval mechanism.

**Governed**: authority is held collectively by a named governance mechanism (multisig, board vote, DAO governance vote, committee decision), with the current key holders or decision makers named and the quorum or threshold for decisions stated.

**Delegated**: authority is held by a named role rather than a specific person, with the current holder of that role named, the scope of their delegated authority stated, and the transfer mechanism stated (who appoints successors and under what conditions).

**Relationships:** Derived from the entity boundary primitive. The applying entity can only be held accountable if the person or mechanism receiving funds can be independently identified and contacted. An entity without a declarable disbursement authority cannot satisfy the organizational identity declaration. The disbursement authority is the operational anchor of the accountability relationship: without it, the organizational identity declaration identifies who is applying but not who will act. For DAO applicants without a legal wrapper, the disbursement authority declaration must name the specific wallet address and the governance mechanism that controls it, with the current holders of governance tokens above the specified materiality threshold named where possible.

**Applications:** CROSS Part IV organizational identity declaration (fifth required field). WALKRI legal entity instrument (evidence form for disbursement authority confirmation).

---

### Governance Resilience

The declared capacity of the applying entity to continue operating in its stated form if the primary contributor or key personnel become unavailable. Three states:

**Single**: one person is essential to the entity's continued operation and no succession plan or backup capacity exists. An entity in single-point-of-failure governance state must acknowledge this explicitly, name the person on whom continuation depends, and state what would happen to active grants and funded deliverables if that person became unavailable during the grant period.

**Partial**: the primary contributor is essential for direction and decision-making, but backup capacity exists for execution. At least one named secondary contributor is ready to continue core operational functions if the primary becomes unavailable, though strategic direction would be interrupted.

**Resilient**: multiple contributors each hold documented responsibility for specific functions, succession mechanisms are documented, and the entity can continue operating without any single named individual. No person's departure would halt active grant obligations.

**Relationships:** Derived from entity boundary and scope. Governance resilience constrains what sustainability stance is credible at the continuation gate. An entity with single-point-of-failure governance cannot credibly declare a sustained sustainability stance without a named succession mechanism. Single-point-of-failure governance is a disclosure, not a disqualifier: some legitimate public goods projects are maintained by one person, and disclosure of that fact is more useful than denial of it. The appropriate funder response is to configure governance resilience as a completion gate condition for grants above a threshold, requiring evidence of partial or resilient governance before final disbursement.

**Applications:** CROSS Part II governance resilience dimension. CROSS Part IV continuation specification gate assessment. Sustainability stance constraint at continuation.

---

## Layer 3: Obligation Primitives

### Obligation Mode

The classification of what type of commitment a grant creates. Three modes are recognized:

**Build obligation**: the funded work must produce a specified deliverable with independently verifiable completion criteria. The obligation object is the deliverable itself. Theory of Build is the correct and complete specification within this mode.

**Change obligation**: the funded work must produce a measurable shift in a specified condition in a defined population, from a declared FROM state to a declared TO state. The obligation object is the measured change. Theory of Build is a failure mode in this context: an application that describes building without specifying the condition it addresses cannot satisfy the change-obligation entry specification.

**Retroactive obligation**: the funded work has already been performed and the funding rewards demonstrated past contribution. The obligation object is the prior contribution, assessed against the program's published criteria.

**Relationships:** Determines what the entry specification gate asks. Determines what evidence scope is appropriate at the completion gate. Determines whether Theory of Build is correct (build mode) or a failure mode (change mode). Maps to the ToC hierarchy: build obligation operates at the Output layer, change obligation at the Outcome layers.

---

### Development Stage

The declared position of the applying work on a five-position maturity scale, reflecting what has been built, proven, and adopted at the time of application. The development stage is declared by the applicant and must be supported by evidence from sources outside the applicant's control.

Five stages:

**Stage 1: Proof of concept.** Something demonstrably exists and has been tested in controlled or internal conditions. Code has been written or a prototype produced. No external users outside the team have used it in production conditions. Completion evidence at this stage is output evidence: the artifact exists, is publicly accessible, and meets stated completion criteria. A project at Stage 1 cannot credibly commit to usage or outcome evidence at the completion gate.

**Stage 2: Early adoption.** External users have used the work in real conditions. Feedback exists from parties outside the team. Adoption is small but independently verifiable from sources outside the applicant's control. Completion evidence at this stage is usage evidence at minimum: adoption by named external parties at a level verifiable from public sources.

**Stage 3: Growth.** A growing user base is independently verifiable from public sources. Demonstrated value has been documented by parties outside the team. The trajectory of adoption is visible in independently accessible data. Completion evidence at this stage is outcome evidence against a declared baseline: a measurable change from a sourced starting point, documented by an independent party.

**Stage 4: Established infrastructure.** Sustained operation with demonstrated community value has been documented over at least 12 months. The central question is continuation rather than validation. The obligation object is maintained operation at declared service standards, not a new deliverable or a measured change from a baseline. Completion evidence at this stage is usage evidence at maintained scale plus a sustainability stance declaration. A project at Stage 4 that declares a build obligation is claiming to add new functionality, not merely maintain existing function; this distinction must be explicit in the entry gate submission.

**Stage 5: Retroactive recognition.** The contribution is complete and its value is demonstrable from historical evidence. The question is recognition of prior contribution, not support for future activity. The entry submission consists of prior contribution evidence. A forward commitment may be configured by the funder as a condition of the award but is not an entry requirement.

**Relationships:** Development stage constrains coherent obligation mode assignment. A Stage 1 project committing to outcome evidence at the completion gate is misrepresenting its stage; the completion gate cannot require evidence the project cannot yet produce. A Stage 4 project applying in a build-obligation round is either adding new functionality (legitimate) or using build framing to avoid change-obligation evidentiary requirements (a framing misrepresentation). The declared stage must be consistent with the evidence the applicant provides at the entry gate. Funder round configurations declare which stages are within scope, allowing programs to target specific maturity cohorts without requiring a narrative description of their targeting criteria.

**Applications:** CROSS Part II development stage dimension. CROSS Part IV entry gate declaration. CROSS round configuration stage targeting. Dashboard configurator stage selector. Evaluator assessment of stage-evidence alignment.

---

### On-chain Identity Anchor

A wallet address (externally owned account or smart contract) that serves as the canonical verifiable identity root for an entity's blockchain interactions. Distinguished from Disbursement Authority (which specifies who receives and deploys funds) by being the identity root rather than the fund receipt mechanism. An entity may have one Disbursement Authority and multiple on-chain addresses; the On-chain Identity Anchor is the address against which cross-program identity matching is performed. For DAO applicants without legal wrappers, the On-chain Identity Anchor and the Disbursement Authority may be the same address. For incorporated entities, they are often distinct.

**Relationships:** Derived from the entity boundary primitive. The On-chain Identity Anchor is the blockchain-layer expression of the applying entity's identity, distinct from the Disbursement Authority (which is the fund receipt mechanism). The anchor enables cross-program identity matching: it is the address that grant databases, attestation registries, and Attestation Corpus queries use to retrieve records associated with a given entity. Where the On-chain Identity Anchor and the Disbursement Authority are the same address, that fact must be stated explicitly; conflation without declaration is a non-disclosure risk equivalent to omitting the affiliated entity field. The On-chain Identity Anchor feeds the Attestation Corpus primitive (Layer 4): the corpus is queried against this address.

**Applications:** CROSS Part IV organizational identity declaration (sixth required field). Cross-program identity matching. Attestation Corpus query input. Cohort Position assessment (Layer 7).

---

### Gate Type

The classification of when in the funding lifecycle an assessment occurs. Four gate types are recognized:

**Entry specification gate**: what an applicant must demonstrate before entering the round. Content determined by obligation mode.

**Progress verification gate**: what a grantee must demonstrate to trigger mid-funding disbursement. Developmental in character.

**Completion verification gate**: what a grantee must demonstrate to receive final payment. Summative in character.

**Continuation specification gate**: what a project must demonstrate to advance between stages or receive funding in a subsequent round. Configured at the program level, not the round level.

**Relationships:** Gate character (developmental vs. summative) is determined by gate type. Evidence scope and evidence strength requirements are configured per gate type. The organizational identity declaration and prior work attribution statement are required at the entry specification gate.

---

### Gate Character

The functional classification of a gate that determines grantee rights and funder obligations during assessment.

**Developmental**: progress verification gates. Purpose is to surface what needs to change before the next gate. Grantees retain iteration rights. The appropriate funder posture is formative.

**Summative**: completion verification gates. Purpose is to render a documented determination of whether the obligation was met. Grantees have redress rights, not iteration rights. The appropriate funder posture is final.

**Relationships:** Derived from gate type. Determines whether grantee iteration rights apply. Constrains funder behavior during assessment.

---

### Obligation Fulfillment Record

The documented history of commitments made under prior grants and whether those commitments were met, for any entity applying on the basis of prior work or prior funding relationships. Three states per prior obligation:

**Fulfilled**: the committed deliverable was produced, the committed change was measured, or the committed contribution was verified, and the documentation is publicly accessible from a source outside the applicant's control.

**Partially fulfilled**: work began and some progress was made. The record must include specific documentation of what was produced and what was not, and a stated explanation of why full fulfillment did not occur.

**Unfulfilled**: the commitment was not met, no deliverable or measurable change was produced, and no satisfactory explanation exists in public records.

**Relationships:** The obligation fulfillment record is required in three cases: when the applying entity has received prior grants from the same funder and is applying again; when the applying entity cites prior work as evidence of capability at the entry gate; and when the applying entity's prior round history includes unresolved KarmaGAP milestones or open gate conditions from prior rounds. The obligation fulfillment record activates the prior work attribution statement (Layer 5) when prior work performed under a different entity is cited. For continuation gate assessment, the obligation fulfillment record is the primary evidence of track record. A returning applicant who cannot provide an obligation fulfillment record for prior grants received from the same funder, or whose prior record shows unfulfilled commitments without adequate explanation, has not established the track record the continuation gate requires.

**Applications:** CROSS Part IV entry specification gate (returning applicants). CROSS Part IV continuation specification gate. CROSS prior work attribution statement activation. Returning applicant eligibility assessment.

---

### Conflict of Interest

The classification of a relationship between a reviewer and an applicant that affects review integrity. Three tiers:

**Tier 1 (categorical bar)**: financial interest, employment relationship, or familial relationship. No waiver possible; reviewer must be replaced.

**Tier 2 (disclosure required, qualified waiver possible)**: prior collaboration, public advocacy, or prior funder-grantee relationship. Disclosure required; waiver requires documented justification and program administrator approval.

**Tier 3 (disclosure encouraged)**: professional acquaintance or network overlap. Reasonable third-party standard applies.

**Relationships:** Governs reviewer access to applications. Generates the conflict of interest declaration requirement at the entry gate of the reviewers process.

---

### Public Benefit Mechanism

The declared mechanism by which the funded work produces benefit to parties outside the applicant's organization, in a form that is non-excludable or non-rivalrous at the point of delivery. Every eligibility claim in a public goods program rests on one of four mechanism types, each of which corresponds to one of the four evidence scope levels defined in Layer 4.

**Output production** corresponds to output evidence scope. The funded work produces an artifact, infrastructure, protocol, or resource that others can use. The mechanism is the existence and accessibility of the artifact. The access condition is the license or access terms under which any party can use, copy, modify, or distribute it.

**Access provision** corresponds to usage evidence scope. The funded work makes something accessible to a population that otherwise lacks access, at a scale verifiable from sources outside the applicant's control. The mechanism is the delivery of access to a defined population. The access condition is the access mechanism (how beneficiaries reach the resource), the cost structure (zero cost, subsidized, or sliding scale), and the non-excludability mechanism (how access is maintained for the target population).

**Condition change** corresponds to outcome evidence scope. The funded work shifts a measurable condition in a defined population from a declared FROM state toward a declared TO state. The mechanism is the causal pathway from the funded activity to the measured change. The access condition is the beneficiary population definition and the intervention mechanism.

**Ecosystem shift** corresponds to impact evidence scope. The funded work contributes to systemic or structural change in a field, protocol, or ecosystem. The mechanism is an argued causal contribution to change at a level above the individual project. The access condition is the named causal pathway, the named co-factors, and the basis for the contribution claim.

**Relationships:** Derived from Evidence Scope (Layer 4). Determines which access condition type is required (see Access Condition, below). Connects to the eligibility pathway logic in CROSS Part II. The mechanism type declared at entry determines what evidence scope is required at the completion gate: output production claims require output evidence at minimum; access provision claims require usage evidence; condition change claims require outcome evidence; ecosystem shift claims require impact evidence or a documented contribution argument. This is the constraint that prevents applicants from claiming a high-level mechanism (ecosystem shift) while committing only to low-level evidence (output evidence).

**Applications:** CROSS eligibility declaration in Part II. CROSS entry gate public benefit mechanism declaration in Part IV. WALKRI output license declaration (for output production mechanism). WALKRI access provision declaration (for access provision mechanism). WALKRI beneficiary population instrument (for condition change and ecosystem shift mechanisms).

---

### Access Condition

The declared terms under which the public benefit mechanism holds and can be independently verified. Every public benefit mechanism claim must be paired with an access condition declaration that specifies (1) the mechanism-specific terms that enable the benefit to reach the stated population, (2) the evidence form by which those terms can be confirmed by an independent party at the appropriate gate, and (3) whether the terms apply at the time of application, at the time of reporting, or at both times.

For output production: the access condition is the named SPDX license identifier, the location of the license file in the repository or attached to the artifact, and confirmation that the license applies to the output at the time of reporting, not only at the time of application. A copyright notice that permits free access without granting modification or redistribution rights does not satisfy the output production access condition.

For access provision: the access condition is the named access mechanism (URL, API, physical location, service delivery channel), the cost structure at the point of access for the target population, and the governance or policy mechanism that prevents exclusion of the stated population.

For condition change: the access condition is the FROM state baseline established from a named independent source, the population definition that determines who the change is measured for, and the named intervention mechanism connecting the funded activities to the expected change.

For ecosystem shift: the access condition is the named causal pathway connecting the funded work to the ecosystem change, the list of acknowledged co-factors, and the basis on which the funded work's contribution is claimed to be material rather than incidental.

**Relationships:** Derived from Public Benefit Mechanism (Layer 3) and the Evidence Form criterion specification element (Layer 5). The access condition specifies the evidence form for the public benefit mechanism claim. Without a declared access condition, a public benefit mechanism claim is an assertion without a verification path.

**Applications:** CROSS Part II public benefit mechanism dimension. CROSS Part IV entry gate access condition declaration. WALKRI output license declaration field (reference implementation for output production mechanism). WALKRI access provision declaration field. All application forms in CROSS-conformant programs where eligibility includes a public goods claim.

---

## Layer 4: Evidence Primitives

### Evidence Scope

The classification of how strong an evidential claim is at a given gate. Four levels in ascending order of rigor:

**Output evidence**: the specified deliverable exists or a measurable artifact demonstrates progress toward it.

**Usage evidence**: the deliverable is being used by parties outside the applicant's control at independently verifiable scale.

**Outcome evidence**: a measurable change has occurred in the specified population, documented against the baseline established at entry.

**Impact evidence**: a credible causal link is established between the funded work and the measured change through methodology sufficient to support causal inference.

**Relationships:** Configured per gate type. Minimum evidence scope at the completion gate is set by the Coordination Scaling Standard based on grant scale. Determines which WALKRI evidence types are required.

---

### Evidence Strength

The classification of how rigorous the verification mechanism is at a given gate. Four levels in ascending order of rigor:

**Self-report with documentation**: grantee narrative with supporting links reviewed by funder staff.

**Third-party verifiable**: evidence independently accessible to any reviewer from sources outside the applicant's control.

**Independent review**: a named party outside the funder-grantee relationship confirms the evidence meets completion criteria.

**Independent evaluation**: a qualified evaluator with domain expertise conducts a structured assessment.

**Relationships:** Configured per gate type. Minimum evidence strength at the completion gate is set by grant scale. Higher evidence strength does not substitute for higher evidence scope; both dimensions are configured independently.

---

### Evidence Type

The classification of what kind of proof a submission constitutes. Five types recognized:

**Standing evidence**: attests to organizational credibility, recognition, accreditation, or institutional membership. Elements: attesting body, domain of standing, scope, currency window, public verification path.

**Activity evidence**: attests that named activities occurred at a stated date, location, and scale. Elements: date, location, activity type, quantity metric, counting methodology. For scientific monitoring data, the named protocol must be stated.

**Outcome evidence**: attests that a named condition changed or that a performance claim is verified against a baseline. Elements: measurement methodology, baseline, post-intervention value, independent verifier. Only evidence type sufficient at completion gates in change-obligation rounds.

**Planning evidence**: attests to future intent, procurement arrangements, or structural agreements. Elements: plan details, parties, timeline. Must be labeled as planning evidence, not outcome evidence.

**Financial accountability evidence**: attests to how prior funding was deployed by expenditure category. Elements: period, expenditure by category, verification path. All links must resolve without authentication walls.

**Relationships:** Governs what a reviewer must look for when assessing a submission. Generates the evidence form requirement in WALKRI's criterion specification. Determines whether outcome-level evidence scope can be satisfied at a given gate.

---

### Causality Stance

The declared position on what kind of causal claim an intervention makes at a given gate or pathway. Two stances:

**Attribution stance**: claims that the intervention caused the observed outcome. Requires counterfactual methodology: a documented estimate of what the indicator would have been without the intervention, an attribution argument, a comparison period or group, and independent attestation.

**Contribution stance**: claims that the intervention contributed to the observed outcome among other factors. Requires a named causal pathway from the activity to the outcome, a list of acknowledged co-factors, and a materiality argument explaining why the intervention's contribution was meaningful rather than incidental.

**Relationships:** Configured at the gate level and at the pathway level. Attribution stance at the pathway level should correspond to counterfactual reference configuration at the associated gate. Contribution stance is appropriate for most public goods and Web3 contexts where multiple actors contribute to shared ecosystem outcomes.

---

### Intended vs. Unintended Effects

The classification of whether an effect was specified in the entry gate or discovered during or after the grant period.

**Intended effects**: outcomes specified in the entry gate. Assessed against the published completion criteria.

**Unintended effects**: effects that occurred during the grant period that were not specified in the entry gate and that are plausibly connected to the funded work. Both positive (discoveries) and negative (adverse signals) unintended effects must be disclosed at the completion gate. Negative unintended effects trigger the Adverse Signal Engagement Principle for the continuation gate assessment.

**Relationships:** Generates the unintended outcomes disclosure requirement at the completion gate. Connects to the Adverse Signal Engagement Principle (referenced from CROSS Part I).

---

### Beneficiary Accountability Gate

A gate element requiring that the people or communities served by a funded program participate in verifying what was delivered, not merely that independent third parties confirm delivery. Distinguished from independent review (a level within Evidence Strength) by specifying who the verifier must be: verification by a qualified external evaluator does not satisfy a beneficiary accountability gate unless the evaluator's methodology includes structured input from beneficiaries. Distinguished from usage evidence (which measures adoption from sources outside the applicant's control) by requiring active participation in verification rather than passive measurement of use.

Three configuration elements: the beneficiary population (the named group whose participation is required, defined at the entry specification gate using the same population definition as the condition change or access provision public benefit mechanism), the participation mechanism (how beneficiary input is collected and documented), and the minimum participation threshold (what proportion of the beneficiary population must have participated for the gate to be satisfied).

The beneficiary accountability gate addresses a specific structural gap in the standard evidence strength framework: a program can satisfy independent review by evaluators who are technically qualified but structurally distant from the people the program serves. The beneficiary accountability gate prevents this substitution by making beneficiary participation a gate condition rather than an optional quality enhancement.

**Relationships:** An extension of Evidence Strength (Layer 4): the beneficiary accountability gate is a specific configuration of the independent review evidence strength level in which the independent reviewer must be, or must systematically incorporate, the beneficiaries themselves. Connects to the Public Benefit Mechanism primitive (Layer 3): the beneficiary accountability gate is most directly applicable to condition change and access provision mechanism types, where a defined beneficiary population is the primary basis for the public goods claim. A program claiming condition change in a named population that does not include beneficiary participation in verification is claiming change on behalf of a population while excluding that population from the accountability mechanism.

**Applications:** CROSS Part XII (CRS ProPack beneficiary feedback as gate element; World Vision LEAP beneficiary verification mechanism). Humanitarian and community-development grants programs. Any program claiming a condition change or access provision public benefit mechanism with a named beneficiary population.

---

### Attestation Corpus

The set of claims about an entity made by parties outside the entity's control, retrievable from named public sources without the entity's participation or submission. Distinguished from evidence (applicant-submitted), gate records (funder-issued for this entity specifically), and standing evidence (institutional endorsements submitted by the applicant) by being third-party, public, and queryable independently. The Attestation Corpus includes on-chain attestations (EAS attestations across chains, KarmaGAP grant and milestone records, RPGF impact attestations), off-chain program completion records (Gitcoin Explorer, Giveth, Open Collective), and named endorsements from identifiable ecosystem participants. The Attestation Corpus is a funder-side data collection, not an applicant disclosure requirement. Its contents inform the track record assessment but are not substitutes for the applicant's own Obligation Fulfillment Record.

**Relationships:** The Attestation Corpus is queried against the On-chain Identity Anchor (Layer 2): the anchor address is the input to cross-program attestation lookups. Distinguished from the Obligation Fulfillment Record (which is applicant-submitted and covers this funder's prior rounds specifically) by being independently queryable from named third-party sources without applicant participation. Where the Attestation Corpus reveals prior grants, milestones, or completion obligations not disclosed in the applicant's Obligation Fulfillment Record, the discrepancy is an adverse signal under the Evidence Type primitive's standing evidence category and is treated as non-disclosure of a prior obligation. The corpus does not require a specific attestation format; any named public source from which claims about an entity can be retrieved without that entity's cooperation or submission qualifies.

**Applications:** CROSS Part IV funder-side Attestation Corpus query procedure. Cross-program track record assessment. Adverse signal detection in returning applicant review.

---

## Layer 5: Specification Primitives

### Criterion Specification Elements

The five elements that a field must carry before it is a measurement instrument rather than a label. All five are required; a field lacking any one is not WALKRI-conformant.

**Criterion intent**: a written statement of what the field measures, distinct from its label. Answers: what does a true response to this field tell us about the applicant or subject?

**Operational definition**: a complete definition of each option or response category with qualifying and non-qualifying examples. For numeric fields: the unit, the counting rule, and the boundary conditions. For text fields: the scope and minimum content requirements.

**Response form**: the response type with a written justification for why that type is appropriate for the criterion intent. Response type is a measurement decision, not a formatting decision.

**Evidence form**: the specification of the artifact that satisfies the criterion: document type, data source, collection methodology at a level sufficient for independent replication.

**Compliance threshold**: for fields referencing an external standard, which components apply, what evidence satisfies each, and what the minimum threshold for passage is.

**Relationships:** Generated by the bidirectional precision primitive. Applies to all fields in any WALKRI-conformant form, including identity fields. Generates the data quality standards (validity, integrity, precision, reliability, timeliness) as quality checks on the specification itself.

---

### Data Quality Standards

The five standards against which a WALKRI-conformant field specification is assessed.

**Validity**: the logical chain from the evidence specified in the evidence form to the result claimed in the criterion intent is documented and sound.

**Integrity**: evidence collection is separated from the entity that benefits from favorable outcomes of that collection.

**Precision**: the measurement instrument is capable of detecting the magnitude of differences that are relevant to the criterion intent.

**Reliability**: the instrument produces consistent results across reporting periods and across different reviewers applying the same operational definition.

**Timeliness**: the evidence is current to the decision cycle it is intended to inform.

**Relationships:** These are quality checks on criterion specification elements, not independent requirements. A field that satisfies all five criterion specification elements but fails a data quality standard has a well-specified but poorly designed instrument.

---

### External Standard Identifier Types

The classification of how an external standard is identified in a WALKRI compliance threshold or CROSS external standard reference. Ten types recognized:

DOI (Digital Object Identifier), ISO number, IETF RFC number, SPDX identifier, W3C dated URL, ELI URI (European Legislation Identifier), regulatory citation, repository version tag, IRIS+ indicator identifier, URL (general, least preferred due to link rot).

**Relationships:** Each identifier type has an associated access model and archival anchor requirement. Identifier type determines the appropriate version anchor.

---

### Access Models

The classification of how an external standard is accessed. Four models:

**Open and free**: available to any user without registration or payment.

**Open with registration**: available without payment but requires account creation.

**Paid and licensed**: requires payment or institutional license for access.

**Government and regulatory**: published by a regulatory or governmental authority; formally free but may require navigation of official systems.

**Relationships:** Constrains what compliance threshold language is appropriate: a paid standard cannot require evidence that only a paying subscriber could produce. The access model must be declared alongside the external standard reference.

---

### Applicant Identity Instrument Types

The classification of identity fields as WALKRI instruments. Three types, each with its own criterion intent and operational definition:

**Legal entity instrument**: criterion intent is to identify the legal person or registered organization accountable for delivering the grant obligations. Operational definition: the name as it appears in the jurisdiction of registration, with registration number and jurisdiction stated. Trading names, brand names, and project names do not satisfy this field unless they are the legal name.

**Display name instrument**: criterion intent is to identify the publicly known name the applicant uses when presenting this work. Operational definition: the name used consistently in prior public communications, repositories, and grant histories. A name chosen specifically for this application that has no prior public use is not a display name.

**Prior entity relationship instrument**: criterion intent is to identify any entity under whose resources, employment, or governance cited prior work was performed. Operational definition: the name of the entity, the applicant's relationship to it at the time of the work, and the current status of that relationship. Activates whenever prior work is cited.

**Relationships:** Generated by the entity boundary primitive applied at the field level. Generates the self-reference consistency requirement: all self-references in an application must resolve to the declared legal entity or display name.

---

## Layer 6: Causal Architecture Primitives

### Theory of Change Hierarchy

The classification of levels in a causal chain from intervention to goal. Six levels following the Compact Logic structure:

**Process**: the interventions, activities, and investments being funded.

**Outputs**: artifacts, infrastructure, capacity, or conditions produced by the Process layer. Build-obligation grants operate primarily here.

**Short-term Outcomes**: conditions produced directly by the program's outputs within the program's active period. Directly measurable at the project level within a single grant cycle. The highest outcome level at which a completion gate can require outcome evidence rather than output evidence.

**Intermediate Outcomes**: conditions produced by the convergence of short-term outcomes over the program time horizon. Typically measurable within the program time horizon but not within a single project cycle. The primary accountability level for institutional funders in multi-year programs.

**Long-term Outcomes**: conditions that persist after the program's active intervention period ends. Not directly measurable at any single project completion gate. Attribution of any single project to a long-term outcome is an argued contribution, not a directly measured one.

**Goal**: the ultimate change the program is designed to contribute to. At the population or system level, operating over the full program time horizon.

**Relationships:** Determines what evidence is appropriate at each gate (short-term outcomes at completion; intermediate and long-term outcomes at program evaluation). Determines what attribution claims are credible at each level. Determines the directionality primitive's application (planning mode works backward from Goal; delivery mode works forward from Process).

---

### Theory Layer

The classification of which layer of the Theory of Change an intervention or pathway primarily operates in. Two values:

**Build**: the intervention operates in the Process-to-Outputs layer, producing artifacts, infrastructure, or capacity. Corresponds to build obligation mode at the round level.

**Change**: the intervention operates in the Outputs-to-Outcomes layer, producing measurable shifts in conditions. Corresponds to change obligation mode at the round level.

**Relationships:** Applied at the pathway level in the program-level ToC declaration. A build-layer pathway declares an intended outcome level (short-term, intermediate, or long-term) identifying what outcomes the built artifact is designed to enable downstream.

---

### Specification Directionality

The classification of whether a pathway or program was specified from the desired outcome backward (planning mode) or from available capacity forward (delivery mode).

**Planning mode**: the specification begins with the desired target node (outcome) and works backward to identify what source nodes (outputs or processes) and causal mechanisms are necessary to reach it.

**Delivery mode**: the specification begins with the available source node (what the program can produce) and claims forward to a target node.

**Relationships:** Delivery-mode pathways naturally cluster at the short-term outcome level; planning-mode specification is required to reach intermediate and long-term outcomes. A portfolio in which all pathways are delivery-mode specified will show structural gaps at higher outcome levels.

---

### Pathway

A numbered causal claim declaring the relationship between a source node at one ToC hierarchy level and a target node at the next level up. Each pathway carries: a unique identifier, source node, target node, causal mechanism statement (the if-then claim), critical assumptions list, external risk list, dependency declarations, theory layer tag, intended outcome level (for build-layer pathways), causality stance tag, and specification directionality tag.

**Relationships:** The pathway is the unit of causal architecture. Dependency declarations between pathways generate the dependency map that enables portfolio analysis. Causality stance tag at the pathway level should match the gate configuration for rounds advancing that pathway.

---

### Sustainability Stance

The declared position on whether outcomes produced by prior rounds are self-sustaining or dependent on continued intervention. Three positions:

**Sustained**: outcomes continue under their own momentum without additional intervention.

**Conditional**: outcomes persist under specified conditions that are independent of this program's continued funding.

**Dependent**: outcomes will not persist without continued intervention. A dependent stance is a disclosure, not a disqualifier.

**Relationships:** Required at the continuation gate. Distinct from the impact question (did the outcome occur?) and the cost-effectiveness question (is further investment worthwhile?). A program can pass both and still have a dependent sustainability stance.

---

## Layer 7: Portfolio Primitives

### Portfolio Position

The classification of a round's relationship to prior rounds in the same program or portfolio. Three positions:

**Initiating**: establishing a new process or output with no prior CROSS round in the same pathway.

**Continuation**: advancing an established pathway with evidence from prior rounds.

**Convergence**: designed to produce an output or outcome that depends on pathways established by other programs or funders.

**Relationships:** Determines what prior work attribution is required. Convergence rounds require dependency declarations naming the pathways they depend on.

---

### Portfolio-level Continuation Benchmark

A funder-declared threshold that the program as a whole must meet to justify continued operation, distinct from individual grantee continuation gates. The benchmark holds the funder's program accountable rather than its individual grantees. Three configuration elements: the metric (what is measured at the program level, such as percentage of grants reaching a specified development stage, total ecosystem adoption attributable to the portfolio, or aggregate outcome evidence across the cohort), the threshold (the minimum level that constitutes program continuation), and the review period (the span across which the benchmark is assessed, typically multiple grant cycles).

Distinguished from the individual continuation gate (which governs a single grantee's eligibility for subsequent funding) and from portfolio analysis outputs (which are analytical tools, not accountability mechanisms) by being a binding condition on the funder's own program continuation. The portfolio-level benchmark applies to the program operator: if the portfolio as a whole does not meet the declared threshold, the program design must be revised before the next cycle opens.

**Relationships:** Derived from Portfolio Position and Evidence Scope. The benchmark metric must be at least as rigorous as the evidence scope required at individual grantee completion gates. A program requiring usage evidence at the grantee completion gate cannot credibly declare a portfolio benchmark based on output evidence at the program level. The benchmark threshold is declared at the entry specification gate for the program (not for individual rounds) and published before any grantee applies.

**Applications:** CROSS Part XII (SBIR/STTR portfolio-level commercialization benchmarks). Program operator accountability in multi-cycle programs. Program continuation decision at the funder level.

---

### Inter-cycle Reflection Stage

A structured learning artifact produced between grant cycles that captures what the prior cycle demonstrated, what assumptions were confirmed or disconfirmed, and how that learning will change the design of the next cycle. The inter-cycle reflection stage is distinct from the continuation gate (which determines individual grantee eligibility) by operating at the program level and by requiring that learning be formally captured and published before the next cycle's entry specification opens.

Three required elements: the reflection artifact (a published document or structured record capturing the prior cycle's findings against the entry specification that opened it), the design response (a documented account of which prior cycle findings are being addressed in the next cycle's design), and the publication timing (the reflection artifact must be published before the next cycle's entry specification opens, not after).

Without an inter-cycle reflection stage, successive grant cycles cannot be distinguished from independent experiments that share a name. The reflection stage is the structural mechanism that makes a multi-cycle program cumulative rather than repetitive.

**Relationships:** Derived from Obligation Fulfillment Record (Layer 3) and Sustainability Stance (Layer 6), applied at the program level rather than the individual project level. The inter-cycle reflection stage is the program-level analogue of the applicant's Obligation Fulfillment Record: both require documenting what was committed to, what was delivered, and what should change as a result. The reflection artifact is input to the next cycle's entry specification gate.

**Applications:** CROSS Part XII (World Vision LEAP inter-cycle reflection stage). Multi-cycle program design. Program-level learning loop. Entry specification design for successive rounds.

---

### Multi-cycle Retrospective Assessment

An assessment spanning multiple grant cycles that evaluates cumulative progress rather than single-cycle delivery. Distinct from the single-cycle completion gate (which evaluates delivery against one round's entry specification) and from the portfolio-level continuation benchmark (which holds the funder's program accountable) by aggregating evidence across multiple completed cycles for a single program or grantee.

Three forms: cumulative outcome assessment (measuring the aggregate change produced across all cycles of a program against the program's original goal), longitudinal grantee assessment (assessing a returning grantee's cumulative contribution across all prior cycles with the current funder), and cross-cycle learning assessment (evaluating whether each cycle's design demonstrably incorporated learnings from prior cycles).

The multi-cycle retrospective assessment is the only gate type that can provide evidence for intermediate and long-term outcomes as defined in the Theory of Change Hierarchy. Single-cycle completion gates can only reach short-term outcomes. Programs claiming to produce intermediate or long-term outcomes must configure a multi-cycle retrospective assessment to substantiate those claims.

**Relationships:** Derived from Theory of Change Hierarchy (Layer 6) and Obligation Fulfillment Record (Layer 3). The ToC hierarchy determines what outcome level is assessable at each gate type: single-cycle completion gates reach short-term outcomes; multi-cycle retrospective assessment reaches intermediate and long-term outcomes. The multi-cycle assessment requires a series of Obligation Fulfillment Records across cycles as its evidence base.

**Applications:** CROSS Part XII (NED Cumulative Assessment Report). Long-term outcome substantiation. Multi-year program evaluation. Intermediate outcome evidence for institutional funders requiring it.

---

### Portfolio Analysis Outputs

The five analytical outputs that a portfolio with declared ToC pathway registries enables:

**Convergence analysis**: multiple programs contributing to the same outcome node; whether contributions are complementary, parallel, or in tension.

**Gap analysis**: outcome nodes declared in pathway registries with no active programs contributing.

**Leverage point identification**: output nodes contributing to multiple downstream pathways.

**Sequencing analysis**: whether upstream-dependent pathways have completed before downstream pathways begin.

**Efficiency analysis**: whether investment concentration is proportionate to pathway position in the causal chain.

**Relationships:** These outputs are enabled by: ToC pathway registry declarations + dependency declarations + causality stance tags + round linkage records + sufficiency position declarations. The Grants Scaffold tool renders these outputs programmatically from CROSS+WALKRI-conformant data.

---

### Cohort Position

An applicant entity's relationships to other entities applying to the same funding round in the same period. Cohort Position encompasses: personnel overlap (named team members appearing in other applications in the same round), wallet overlap (the On-chain Identity Anchor or Disbursement Authority address appearing in other applications or as a recipient of funds from other applicants in the same round), endorser overlap (the same identifiable parties endorsing multiple applicants in the same round), and prior co-applicant history (entities that have applied together to this or other programs in prior rounds). Cohort Position is a funder-side assessment, not an applicant self-report. It is distinct from the Affiliated Entity Disclosure (which is the applicant's own account of relationships) by being an independent cross-applicant check. Findings from Cohort Position assessment do not automatically disqualify; they require disclosure and may trigger Tier 2 conflict of interest procedures where personnel overlap with a reviewer is discovered.

**Relationships:** Derived from the entity boundary primitive: the Cohort Position check asks whether the declared boundaries of multiple applying entities in the same round are genuinely distinct. Wallet overlap is checked against the On-chain Identity Anchor (Layer 2): the same anchor address appearing across multiple distinct applying entities is a material discrepancy requiring reconciliation. Personnel overlap activates the affiliated entity disclosure requirement (Layer 2, entity boundary) and may trigger Tier 2 conflict of interest procedures under the Conflict of Interest primitive (Layer 3). Endorser overlap is recorded as informational; it does not activate conflict of interest procedures unless the endorser holds a reviewer role.

**Applications:** CROSS Part VII Cohort Position assessment as a round-level funder procedure. Cross-applicant integrity check before final gate determinations. Personnel and wallet overlap disclosure.

---

## Relationship Map

The following relationships between primitives are load-bearing for the standards' internal consistency:

- Bidirectional precision generates criterion specification elements.
- Criterion specification elements generate data quality standards as quality checks.
- Entity boundary generates scope as a child primitive (scope is always relative to a declared entity boundary).
- Scope generates sufficiency as a child primitive (sufficiency is always measured at a declared scope).
- Obligation mode determines gate content at the entry specification gate.
- Gate type determines gate character (developmental or summative).
- Evidence scope and evidence strength are independently configured per gate; neither substitutes for the other.
- Causality stance at the pathway level must match the gate configuration for rounds advancing that pathway.
- Theory layer tag (build/change) is the obligation mode primitive applied at the pathway level.
- Specification directionality predicts outcome level clustering: delivery mode clusters at short-term outcomes, planning mode reaches intermediate and long-term outcomes.
- Sufficiency position at a declared scope determines whether continuation is primarily advancing new outcomes or sustaining prior ones.
- Revenue architecture determines what additionality means: grant-only entities have full additionality for any non-duplicative grant; commercial and hybrid entities must delineate the non-commercial scope.
- Disbursement authority is the operational anchor of the organizational identity declaration: entity boundary identifies who is applying; disbursement authority identifies who will act.
- Governance resilience constrains what sustainability stance is credible at the continuation gate: single-point-of-failure governance cannot support a sustained stance without a named succession mechanism.
- Development stage constrains coherent obligation mode assignment: the declared stage must be consistent with the evidence available at both the entry and completion gates.
- Obligation fulfillment record is required at the entry gate for returning applicants and is the primary track record evidence at the continuation gate.
- Portfolio-level continuation benchmark holds the funder's program accountable rather than individual grantees; its metric must be at least as rigorous as the evidence scope required at individual completion gates.
- Inter-cycle reflection stage is the program-level analogue of the applicant's obligation fulfillment record; it is input to the next cycle's entry specification gate and is required before that gate opens.
- Multi-cycle retrospective assessment is the only gate type that can substantiate intermediate and long-term outcomes as defined in the ToC hierarchy; single-cycle completion gates reach only short-term outcomes.
- Beneficiary accountability gate is a specific configuration of independent review evidence strength in which the beneficiary population must participate in verification; it cannot be satisfied by technically qualified evaluators who exclude beneficiary input.

---

## Primitive Gap Protocol

When a new provision is required that cannot be derived from existing primitives, the following protocol applies:

1. Name the gap: what concept is the new provision applying that is not yet a primitive?
2. Define the candidate primitive: is it irreducible? Does it derive from existing primitives, or is it genuinely new?
3. Add the primitive to this document before writing the provision.
4. Derive the provision from the primitive rather than from the specific case that revealed the gap.

This protocol prevents example-driven accretion. The case that revealed the gap is documentation context for the primitive, not the definition of the primitive.

---

## Document Relationships

CROSS (CROSS-common-reporting-outcome-standards-schema-0_2_0.md): all provisions are applications of primitives defined here. Where CROSS references a primitive concept without a pointer to this document, the pointer should be added in the next revision.

WALKRI (WALKRI-standard-0_1_0.md): all criterion specification requirements, field type classifications, and quality standards are applications of primitives defined here.

Grants Forge Suite (grants-forge-suite-product-description-0_1_0.md): the five tools implement primitives in operational interfaces. Grants Forge implements obligation mode, gate type, and scope declarations. Grants Field Calibrator implements criterion specification elements and data quality standards. Grants Causeway implements the ToC hierarchy and pathway primitives. Grants Crucible implements evidence scope, evidence strength, and evidence type. Grants Scaffold implements portfolio analysis output primitives.

Frame Language Grammar (Methodology/frame-language-grammar-0_1_0.md): the methodological primitives in Layer 1 of this document are derived from the Frame Language grammar. The grammar document is the canonical source for Frame Language primitives; this document includes them by reference for the purpose of governing how CROSS and WALKRI provisions are written.

---

*License: CC0. Any organization may use, adapt, or build upon this document without modification, attribution, or licensing arrangement.*

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.4 | 2026-05-19 | Four new primitives added from worldwide compatibility research findings. Layer 4: Beneficiary Accountability Gate (gate element requiring beneficiary population participation in verification, not substitutable by technically qualified but beneficiary-distant independent review; derived from CRS ProPack and World Vision LEAP). Layer 7: Portfolio-level Continuation Benchmark (funder-declared program-level threshold holding the program accountable rather than individual grantees; derived from SBIR/STTR commercialization benchmarks), Inter-cycle Reflection Stage (structured learning artifact produced between grant cycles, required before next cycle's entry specification opens; derived from World Vision LEAP), Multi-cycle Retrospective Assessment (assessment spanning multiple cycles, the only gate type that can substantiate intermediate and long-term ToC outcomes; derived from NED Cumulative Assessment Report). Total: 36 primitives across 7 layers. |
| 0.1.3 | 2026-05-18 | Three new primitives added. Layer 2: On-chain Identity Anchor (canonical wallet address for cross-program identity matching, distinct from Disbursement Authority). Layer 4: Attestation Corpus (third-party verifiable claims about an entity from named public sources, queryable without entity participation). Layer 7: Cohort Position (applicant's relationships to other entities in the same funding round, covering personnel, wallet, endorser, and co-applicant overlap). Total: 32 primitives across 7 layers. |
| 0.1.2 | 2026-05-18 | Layer 2: Three new identity primitives added. Revenue Architecture: four types (grant-only, fee-for-service, commercial, hybrid) anchoring additionality declarations for entities with commercial revenue models. Disbursement Authority: three states (individual, governed, delegated) providing the operational anchor for organizational accountability. Governance Resilience: three states (single, partial, resilient) constraining what sustainability stances are credible at continuation gates. Layer 3: Two new obligation primitives added. Obligation Fulfillment Record: three states (fulfilled, partially fulfilled, unfulfilled) required for returning applicants and applicants citing prior work. Development Stage: five stages (proof of concept through retroactive recognition) constraining coherent obligation mode assignment and allowing funder cohort targeting. CROSS provisions derived: Part II dimensions for revenue architecture, governance resilience, and development stage; Part IV extensions for disbursement authority (fifth organizational identity field), obligation fulfillment record (returning applicant pre-condition), and development stage declaration. |
| 0.1.1 | 2026-05-18 | Layer 3: Two derived primitives added. Public Benefit Mechanism: four mechanism types (output production, access provision, condition change, ecosystem shift) derived from Evidence Scope applied at the eligibility claim context. Access Condition: the declared terms under which a public benefit mechanism holds, paired with an evidence form for independent verification. Both primitives are applications of existing Layer 4 (Evidence Scope) and Layer 5 (Evidence Form) primitives to the eligibility declaration context. CROSS provision derived: Part II public benefit mechanism dimension and Part IV access condition declaration requirement. |
| 0.1.0 | 2026-05-16 | Initial release. Seven layers, twenty primitives. |
