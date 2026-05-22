---
title: CROSS Skill
version: 0.6.0
date: 2026-05-22
status: Procedural encoding of CROSS v0.4.7 for AI-assisted grant evaluation and configuration.
related_documents:
  - standards/CROSS-common-reporting-outcome-standards-schema-0_2_0.md
  - standards/CROSS-grant-configurator-0_2_0.md
  - standards/CROSS-canonical-round-configuration-schema-0_1_0.md
  - standards/CROSS-grantee-dashboard-0_2_0.md
  - standards/CROSS-reviewers-dashboard-0_1_0.md
  - standards/CROSS-runbooks-0_1_0.md
---

# CROSS Skill

Invoke this skill before evaluating any grant application against CROSS requirements, before running the Grant Configurator sequence for a funder, or before assessing any indicator specification, conflict of interest relationship, gate submission, or data quality claim. This is a procedural encoding of the Common Reporting Outcome Standards Schema (CROSS) version 0.4.7 that enables consistent application across obligation modes, evaluation contexts, and gate types. It is structured so a partial task ("evaluate this FROM state claim" or "assess this gate evidence package") can be received and completed correctly.

## Runtime Sequence

When given an evaluation task, identify which operation is requested and run the corresponding procedure in full:

1. **Entry specification gate assessment.** Run when given an application text. Determine the round's declared obligation mode first; then run the correct mode procedure. Confirm that an organizational identity declaration and a sufficiency architecture declaration are both present before proceeding. See Part III and Parts IV-V below.

2. **FROM state classification (change obligation).** Run as part of the change-obligation gate assessment, or independently when asked to classify a specific claim. Returns one of five canonical classifications. See Part III, Section B below.

3. **Deliverable specification assessment (build obligation).** Run when evaluating whether an application's deliverable specification is falsifiable with independently verifiable completion criteria. See Part III, Section A below.

4. **Retroactive contribution assessment.** Run when evaluating whether a retroactive application's prior contribution evidence meets the program's published threshold criteria. See Part III, Section C below.

5. **Organizational identity declaration assessment.** Run as a pre-condition to any entry gate assessment, across all three obligation modes. See Part IV below.

6. **Sufficiency architecture declaration assessment.** Run as a pre-condition to any entry gate assessment, alongside the organizational identity declaration. See Part V below.

7. **Prior work attribution assessment.** Run when any entry gate submission cites prior work as evidence of capability, track record, or past contribution. See Part VI below.

8. **Indicator field assessment.** Run when evaluating a single indicator specification or a full indicator set. Applies the 11-field checklist and field clustering rules. See Part VII below.

9. **Gate evidence assessment.** Run when evaluating a progress verification or completion verification gate submission. Applies the evidence scope and evidence strength requirements from the round specification. See Part XI below.

10. **Conflict of interest tier classification.** Run when given a description of a relationship between a reviewer and an applicant, or between applicants and committee members. See Part VIII below.

11. **Data quality standards assessment.** Run when evaluating a reported indicator claim or a proposed measurement methodology. See Part IX below.

12. **Grant Configurator sequence.** Run when a funder wants to generate a round specification from their criteria. See Part X below.

13. **Obligation dimension activation.** Run when given a set of funder criteria or a specific application profile to determine which obligation dimensions are active. See Part II below.

14. **Scope attribution and outcome credit assessment.** Run when concurrent funding is disclosed. See Part XII below.

15. **Counterfactual verification assessment.** Run when a completion or continuation gate is configured at counterfactual reference level. See Part XI below.

16. **Program-level ToC architecture configuration.** Run when configuring a program-level theory of change declaration for a multi-round or multi-stage program. See Part XIII below.

17. **Institutional framework alignment identification.** Run when asked how CROSS conformance maps to OECD DAC, IRIS+, USAID PIRS, or DAOIP-5. See Part XIV below.

18. **Recommendation generation.** Run after completing a gate assessment and dimension evaluation. Returns one of three canonical recommendation terms. See Part XV below.

19. **Funder obligation compliance check.** Run when evaluating whether a funder has met its CROSS obligations: publishing gate configurations, maintaining records, providing redress mechanisms. See Part XVI below.

20. **Privacy-sensitive accommodation assessment.** Run when an applicant claims a privacy-sensitive accommodation. See Part XVII below.

21. **Novel runbook configuration selection.** Run when a program type does not match the six standard runbooks from CROSS-runbooks-0_1_0.md. Assess whether the program implements one of seven new structural primitives: inter-cycle reflection stage (Runbook 7), multi-cycle retrospective assessment (Runbook 8), threshold-scaled independence (Runbook 9), participatory indicator selection (Runbook 10), computational retroactive allocation (Runbook 11), portfolio benchmark (Runbook 12), or beneficiary accountability gate (Runbook 13). See CROSS-runbooks-0_2_0.md.

22. **Portfolio benchmark compliance assessment.** Run when a program operates Runbook 12 or when a funder has published portfolio-level performance thresholds. Assesses funder-side accountability against the published benchmark rather than only individual grantee gate outcomes. See Part XVI and CROSS-runbooks-0_2_0.md.

23. **Beneficiary accountability mechanism assessment.** Run when a program operates Runbook 13 or when program MEAL requirements include community feedback and complaint response. Confirms that the mechanism is specified before any beneficiary is enrolled. The mechanism must name what it can receive, how it operates, who is responsible, the response timeline, and what records are maintained. A mechanism that names a channel without these specifications is a label, not a mechanism.

25. **Compound obligation entry gate assessment.** Run when the declared obligation mode is compound: a program-level Change claim with multiple Build components as the causal pathway. Confirm that a complete change specification is present at the program level and that each component carries a contribution_to_change statement. See Part III, Section D below.

24. **Primitive classification for new frameworks.** Run when asked how a new external framework aligns with CROSS+WALKRI. Identify which measurement primitive the framework exemplifies using the CROSS-WALKRI-primitives-framework-index-0_1_0.md. Report whether a full compatibility statement is warranted (structurally novel exemplar) or a Tier 2 index entry suffices (existing primitive with existing exemplars). The ten primary primitives are: pre-specification/entry gate, obligation mode (Build/Change/Retroactive), Theory of Change hierarchy, causality stance, disaggregation ratchet, independent verification pathway, portfolio aggregation, organizational identity anchor, evidence form specification (WALKRI), and coherence disclosure. Candidate new primitives from v0.4.7 research: inter-cycle reflection stage, multi-cycle retrospective assessment, portfolio-level continuation benchmark applied to funder, beneficiary accountability mechanism, regulatory approval pathway as terminal gate.

25. **Public benefit mechanism and access condition assessment.** Run as a pre-condition at all entry gates, alongside organizational identity and sufficiency architecture declarations. Classifies the declared mechanism type and confirms the access condition is stated with mechanism-appropriate specificity. See Part IVa below.

22. **Revenue architecture and development stage assessment.** Run at entry gate. Classifies the applicant's revenue architecture and development stage, checks consistency with the obligation mode and additionality claim, and checks stage alignment with the round's configured stage targeting where configured. See Part IVb below.

23. **Obligation fulfillment record assessment.** Run for returning applicants and applicants citing prior work with prior grants from the same or other programs. Checks milestone completion status of prior-cited grants before entry gate assessment proceeds. See Part IV, Obligation Fulfillment Record section below.

---

## Part I: CROSS Purpose and Scope

CROSS specifies what funded interventions are obligated to produce. It provides grants ecosystems with a portable obligation schema that accommodates three distinct obligation modes, calibrates evidentiary pressure to program context, and generates structured reporting data comparable across funders, rounds, and grantees.

CROSS is not a process standard. It does not specify how rounds are structured, how funds are distributed, or how round administration decisions are made. CROSS specifies the content of obligation: what applicants must demonstrate, what funders must evaluate, and what grantees must report.

**Suite standard references.** CROSS inherits requirements from four companion standards. When evaluating conformance, apply these inherited requirements:

- Adverse-Signal Engagement Principle Core Standard: applicants must surface adverse signals (prior rejections from similar programs, contradictory technical findings, negative due diligence from other funders). Reviewers must not suppress adverse signals found during evaluation.
- Information Asymmetry Classification Standard: undisclosed concurrent funding is an omission asymmetry. The concurrent funding disclosure requirement instantiates this standard's omission class in the grant application context.
- Precision-First Design Standard: the double-negation invariant applies. Documentation requirements must not be so light that obligation is absent, and must not be so heavy that legitimate small-team applicants are excluded.
- Coordination Scaling Standard: calibrates the rigor tier. Determined by scale indicators (funding amount, population claim scope), not by gate passage alone.

The Regenerative Obligation Standard and CROSS are structurally paired but independent. Regenerative Obligation Standard addresses direction; CROSS addresses destination. Run both evaluations independently when both apply; do not merge them.

Frame Language was the conceptual development tool for CROSS. It is not a formal dependency. The diagnostic categories D1 and D2 from Frame Language appear in Part III as shorthand for change-obligation gate failure types; they are not required vocabulary outside that context.

---

## Part II: Independent Obligation Dimensions

CROSS specifies multiple independent obligation dimensions. Each dimension has its own triggering logic. Dimensions do not scale together.

**Procedure for dimension activation:** For each dimension, apply the trigger test independently. If the trigger condition is met, that dimension is active regardless of other dimensions.

### Dimension 1: Outcome Documentation Rigor

**Trigger:** Funding amount above a round-level threshold OR public impact claim at a scale above the Coordination Scaling Standard minimum.

**Active requirements:** Indicator sourcing, baseline documentation, and (at Standard scale) theory of change formalization. Rigor level scales with the Coordination Scaling Standard tier.

### Dimension 2: Institutional Capacity

**Trigger:** The scope of the proposed work is materially larger than the applying organization's demonstrated track record.

**Active requirements:** Capacity assessment. Result calibrates disbursement conditions tier; it is not a disqualifier.

### Dimension 3: Conflict of Interest

**Trigger:** Any relationship exists between a decision-maker and an applicant, or between an applicant and a committee member.

**Active requirements:** Conflict of interest classification into the correct tier. See Part VIII.

### Dimension 4: Concurrent Funding Disclosure

**Trigger:** Any grant, investment, or revenue source related to the scope of the application in the prior 24 months. For retroactive rounds: also includes any prior award for the same or overlapping contribution.

**Active requirements:** Disclosure of all related sources. Required fields: source name, source type, approximate amount, relationship to scope, ongoing obligations, governance rights.

**Critical rule:** Non-disclosure is a disqualifier. Disclosure does not disqualify.

### Dimension 5: Adverse Signal Disclosure

**Trigger:** Any adverse signal exists relating to the application or applicant.

**Active requirements:** Applicant must surface all adverse signals. Reviewers must not suppress adverse signals found during evaluation.

### Dimension 6: Open Source and Intellectual Property

**Trigger:** The funded work produces code, data, research, or other artifacts, AND the public goods claim rests on open access to those artifacts.

**Active requirements:** Outputs must be demonstrably open at the time of reporting, not only at application time.

**IP ownership declaration sub-requirement:** Where the funded work produces research outputs, models, datasets, or novel technical artifacts for which intellectual property rights are material, the applicant must submit an IP ownership declaration specifying: who holds rights in the outputs, under what terms those rights are held, and what the public's rights of access and use are. The declaration must be specific enough to answer whether a third party could use, fork, or build upon the outputs without seeking permission from any rights holder. An applicant who holds exclusive rights over outputs claimed as public goods must reconcile those rights with the public goods claim in the additionality declaration (Part XII). For programs funding decentralized science, AI model development, or research producing novel patentable outputs, the program's round configuration activates the IP ownership declaration as an explicit gate criterion rather than a supplementary disclosure.

### Dimension 7: Beneficiary Engagement and Beneficiary Validation

**Trigger:** The application claims to address a problem experienced by a defined population (change obligation) OR the deliverable addresses a named external need (build obligation, where activated by funder configuration).

**Active requirements (change obligation):** The claimed FROM state must be validated by parties outside the applicant's control. Applicants must name existing alternatives and explain why they do not serve the stated population.

**Active requirements (build obligation, if activated):** At least one named party outside the applicant's organization has confirmed the need for the deliverable.

### Dimension 8: Privacy and Data Sensitivity

**Trigger:** The beneficiary population faces elevated risk from standard outcome measurement.

**Active requirements:** Privacy-preserving measurement methodologies in lieu of standard analytics. Not an exemption from obligation; specifies which mechanisms are appropriate. See Part XVII.

### Dimension 9: Environmental and Social Impact (Optional)

**Trigger:** Activated by funder configuration.

**Active requirements:** A/B/C classification under International Finance Corporation Performance Standards derived structure. Class A: full impact assessment required. Class B: targeted assessment. Class C: screening declaration.

### Dimension 10: Gender Equity (Optional)

**Trigger:** Activated by funder configuration.

**Active requirements:** Gender-disaggregated outcome reporting for all population-level impact indicators.

### Dimension 11: Procurement Integrity (Optional)

**Trigger:** Activated by funder configuration AND sub-contracting or sub-granting exceeds 20% of the total award.

**Active requirements:** Sub-contractor disclosure. See field clustering rules in Part VII.

---

## Part III: Entry Specification Gate

The entry specification gate is a pre-criterion that operates before any rigor-tier assessment begins. It is binary and non-negotiable.

**First step before any gate assessment:** Confirm that three declarations are present: an organizational identity declaration (Part IV), a sufficiency architecture declaration (Part V), and a public benefit mechanism declaration with access condition (Part IVa). An entry gate submission that lacks any of these three is incomplete and is not assessed until all three are provided.

**Second step:** Confirm the declared obligation mode from the round specification. The mode determines which gate section applies. Do not apply change-obligation gate criteria to a build-obligation application, and do not apply build-obligation gate criteria to a change-obligation application. Misapplying the gate is a reviewer error, not an applicant failure.

---

### Section A: Build Obligation Entry Gate

**The gate question:** Can the applicant name a falsifiable deliverable with independently verifiable completion criteria?

**Pass criteria:** A named artifact, product, or documented output, with completion criteria specific enough that a reviewer who did not commission the work could determine whether they are met, from publicly accessible evidence without contacting the applicant.

**Fail criteria (Direction specification without deliverable):** The application describes a goal, vision, or direction but does not name a specific deliverable. Example: "making DeFi more transparent" is a direction. "A reporting module producing a human-readable fee summary for any ERC-4626 vault, published as an open-source library, with a deployed instance on Ethereum mainnet and a documented application programming interface" is a deliverable. The difference is testability: the first cannot be verified or falsified; the second can.

**Fail criteria (Underspecified completion criteria):** A deliverable is named but the completion criteria are too vague for independent verification. "A working prototype" names a form but not a standard. Completion criteria must specify what done means, not just what will be built.

**Critical rule:** The Theory of Build is not a failure mode in build-obligation rounds. An application that describes what it will build, with falsifiable criteria, is correct and complete for this mode. Do not import change-obligation gate logic into a build-obligation assessment.

**Gate finding options:**

Gate passes: "Entry specification gate passes: applicant names [deliverable] with completion criteria: [list criteria], independently verifiable by [named method]."

Gate fails: "Entry specification gate fails: [describe what was offered instead of a falsifiable deliverable or verifiable criteria]. Failure type: direction specification without deliverable / underspecified completion criteria."

---

### Section B: Change Obligation Entry Gate

**The gate question:** Can the applicant name the FROM state as a specific measurable condition in a defined population?

**Pass criteria:** A specific condition (not a category) in a named population with a named, independently accessible source.

**Fail criteria:** A category, a values aspiration, or a generic claim.

**Application timing is not the diagnostic.** A team that built something before a grant opportunity appeared is not exhibiting a gate failure if they can name the specific FROM state they addressed.

### FROM State Classification

Apply one of five canonical classifications:

**Specific pass:** The FROM state names a condition (not a category), a named population, and a named, independently accessible source. Gate passes. Proceed to rigor tier.

**Specific with minor gap:** The FROM state is specific and names a population, but the source is absent or not independently accessible. Gate conditionally passes; require source documentation before proceeding.

**D1 failure (canonical vocabulary without structural grounding):** The FROM state uses technically correct vocabulary but does not name a measurable condition. Example: "lack of developer tooling in the ecosystem" uses the right field but names a category without a measurable condition or named source. D1 applications can produce technically coherent responses when asked for more information; the underlying diagnosis is absent. Gate fails. Communicate the failure at the rigor tier level.

**D2 failure (values aspiration without conditions):** The FROM state is a values or mission statement, not a diagnosis. When asked to specify the FROM state, D2 applications produce more values language because no diagnosis was performed. Gate fails. Communicate the gate failure clearly.

**Insufficient information:** The application does not contain enough text to assess the FROM state. Return this classification with a list of what would need to be present to run the assessment.

### Rigor Tier (post-gate)

Rigor tier only runs after the gate passes. Assigns a tier calibrated by the Coordination Scaling Standard:

- Tier 1 (minimal): small funding, narrow scope, specific diagnosis. Indicator sourcing and baseline required; full theory of change formalization not required.
- Tier 2 (standard): mid-range funding, regional or protocol-level impact claims. Full indicator set, sourced baseline, theory of change narrative required.
- Tier 3 (full institutional): large funding, broad population impact, complex multi-year programs. Full indicator set, sourced baseline, formal theory of change, organizational capacity documentation, audit trail required.

Default if no Grant Configurator has been run: assign Tier 2 and note that a Configurator run would allow accurate calibration.

---

### Section C: Retroactive Obligation Entry Gate

**The gate question:** Does the applicant present evidence of prior contribution meeting the program's published threshold criteria?

**What must be present:** (1) A description of what contribution was produced; (2) the period during which it was produced; (3) evidence of who is using or has benefited from it, accessible from sources outside the applicant's control; (4) concurrent funding disclosure covering any prior awards for the same or overlapping contribution.

**Pass criteria:** All four elements present with at least one independently accessible source of evidence for contribution and at least one independently accessible source for use.

**Fail criteria:** Any of the four elements absent. Contribution evidence that consists entirely of applicant self-assertion without any independent source. Use evidence that is not independently accessible.

**Gate finding options:**

Gate passes: "Entry specification gate passes: applicant presents contribution evidence of [type] from [period], with independent sources confirming [contribution] and [use]."

Gate fails: "Entry specification gate fails: [describe which element is absent: contribution description, period, independent contribution evidence, independent use evidence, or prior award disclosure]."

---

### Section D: Compound Obligation Entry Gate

**The gate question:** Does the application present (1) a program-level Change specification that would pass the Change obligation entry gate, and (2) component-level Build specifications, each carrying a contribution_to_change statement explaining how that component's deliverable advances the causal chain toward the program-level Change?

**What must be present:** A complete change_specification block at the program level: FROM state with source, TO state in the same units as FROM, named indicator with operational definition, causal mechanism with explicit assumptions, evidence threshold, evaluation timeline. A components array with at least two components. Each component must carry: a named deliverable, completion criteria specific enough for independent verification, and a contribution_to_change statement.

**Pass criteria:** The program-level Change specification passes the Section B gate. Each component passes the Section A gate independently. Each component's contribution_to_change statement makes a specific causal claim, not a general connection to program goals.

**Critical rule:** Completing all Build components does not automatically constitute achieving the program-level Change. The two evaluation tracks are separate. A compound grant that completes all Build components but does not produce the specified Change has met its Build obligations and failed its Change obligation. These are distinct findings and must be reported separately.

**Fail criteria:**

- Program-level Change specification fails the Section B gate: classify the failure using the FROM state classifications above.
- Any component fails the Section A gate: "Component [name] entry specification gate fails: [failure description]."
- A component's contribution_to_change statement does not make a specific causal claim: "Component [name] contribution_to_change is generic. The statement connects the deliverable to the program goal but does not state the mechanism by which the deliverable advances the causal chain."

**Gate finding options:**

Gate passes: "Compound entry specification gate passes: program-level Change specification [summary]; [N] components with passing deliverable specifications and contribution_to_change statements."

Gate fails (program level): "Compound entry specification gate fails at program level: [Change obligation failure description]."

Gate fails (component level): "Compound entry specification gate passes at program level. Component [name] fails: [Build obligation failure description]."

---

## Part IV: Organizational Identity Declaration Procedure

The organizational identity declaration is a pre-condition for gate assessment at all entry gates, across all three obligation modes. It is not a scored criterion. An entry gate submission that does not include the organizational identity declaration is incomplete and is not assessed until the declaration is provided.

The four required fields derive from the Entity Boundary primitive (CROSS+WALKRI Primitives Foundation, Layer 2): the applying entity, affiliated entity, and contributing entity states each correspond to a required field.

### Field 1: Legal Entity Name and Jurisdiction

**What is required:** The name of the natural person or registered organization exactly as it appears in the relevant jurisdiction of registration, and the jurisdiction itself.

**What does not satisfy this field:** A project name, display name, or GitHub organization name, unless it is also the legal name.

**Where no legal entity exists:** The applicant must state this explicitly and name the individual who assumes personal accountability for the obligation.

**Assessment procedure:** Verify that the name provided is a legal name or that the applicant has explicitly declared no legal entity exists and named an accountable individual. A display name without the explicit no-legal-entity declaration does not satisfy this field.

### Field 2: Parent Organization Declaration

**What is required:** Whether the applicant operates under or is affiliated with a larger organization, network, or chapter structure. Where a parent organization exists: its name must be stated. The relationship must be described: does the parent organization know about this application, does it share the applicant's brand or personnel, and is it separately applying to this or concurrent rounds of the same program?

**Critical rule:** Silence on parent organization is not acceptable where an affiliation is publicly documented or where the applicant's name, brand, or personnel overlaps with a known larger organization.

**Assessment procedure:** Check whether the applicant's name, domain, personnel, or codebase shows any publicly documentable connection to a larger organization. If yes and the field is silent, flag as non-conformant. Disclosure of a parent organization is not a disqualifier; non-disclosure of a publicly documentable affiliation is.

### Field 3: Affiliated Entity Disclosure

**What is required:** Any other organization, project, or entity that shares the applicant's name, brand, domain, key personnel, or codebase, whether or not a formal legal relationship exists.

**Purpose of this field:** Surface name collisions (a new applicant using a name associated with an established org), internal fragmentation (a sub-entity applying separately from a parent that may also apply), and personnel overlap (key team members holding funded roles in other organizations applying to the same round).

**Critical rule:** Disclosure is not a disqualifier. Non-disclosure of a publicly documentable affiliation is a conformance failure.

### Field 4: Prior Round History

**What is required:** Whether the applicant or any substantially overlapping entity (same personnel, same codebase, same project name, or same legal entity under a different display name) has applied to this program in prior rounds, under what name, and with what outcome.

**Purpose of this field:** Catch serial rebranding: applicants who received a prior rejection and return under a different name claiming no prior history with the program.

**Corroboration note:** Where a prior funder's gate determination exists as a publicly verifiable signed record, an applicant may cite it as corroboration, and the reviewing program may query it as independent verification. A funder-signed gate record from a prior round is stronger corroboration than an applicant's written account of the same outcome.

### Obligation Fulfillment Record (Returning Applicants)

**Activation:** Required when the applicant has prior grant history with this program or when the application cites prior grants from other programs as evidence of capability or track record.

**What is required:** For each prior grant cited or for each prior grant from this program, provide: the granting program, the grant period, the declared deliverable or intervention at entry, the fulfillment state (fulfilled, partially fulfilled, or unfulfilled), and where not fulfilled, a brief explanation.

**Three fulfillment states:**

- Fulfilled: all milestones were met within the grant period, all deliverables were completed as specified, and all reporting obligations were met.
- Partially fulfilled: some milestones were met and some were not, or a milestone was met with documented scope reduction, or reporting was late but submitted.
- Unfulfilled: key milestones were not met, key deliverables were not produced, or the grant was abandoned without a documented wind-down.

**Assessment procedure:** Check publicly verifiable milestone status sources (KarmaGAP, the granting program's public records, on-chain deliverable verification) before relying on the applicant's self-report. A partially fulfilled or unfulfilled prior obligation does not automatically fail the entry gate, but it must be disclosed and addressed. A pattern of unfulfilled obligations across multiple grants is an adverse signal requiring Block J investigation in the evaluation SOP.

**Corroboration note:** A granting program's signed gate record showing milestone completion is stronger corroboration than an applicant's written account.

### Field 5: Disbursement Authority Declaration

**What is required:** Who receives and deploys the grant funds, in one of three states:

- Individual: a named natural person who assumes personal accountability for fund deployment. Requires: full legal name, jurisdiction, and a statement of how deployment decisions will be made.
- Governed: an organization or on-chain entity with a governance mechanism that authorizes fund deployment. Requires: the name of the entity, a description of the governance mechanism, and confirmation that the mechanism is documented and independently verifiable.
- Delegated: funds are received by one entity and partially or fully deployed by another entity. Requires: the identity of both the receiving entity and the deploying entity, the terms of the delegation, and whether the delegation is formally documented.

**Assessment procedure:** Verify that the named entity or individual matches the organizational identity declaration (Field 1). A mismatch between the legal entity name in Field 1 and the entity receiving funds in Field 5 requires explicit reconciliation. The delegation state is not a disqualifier; undisclosed delegation is.

---

## Part IVa: Public Benefit Mechanism and Access Condition Declaration Procedure

The public benefit mechanism declaration is a pre-condition for entry gate assessment at all entry gates, across all three obligation modes. It is not a scored criterion. An entry gate submission that does not include both a mechanism type declaration and an access condition is incomplete.

### Mechanism Type Classification

Classify the applicant's declared mechanism into one of four types:

**Output production:** The public benefit is the production of a publicly accessible artifact, dataset, documentation, software package, or infrastructure component. The mechanism is the act of production and publication. The access condition is the licensing or access terms under which the output is available.

**Access provision:** The public benefit is providing access to an existing system, service, or capability to a population that would not otherwise have it. The mechanism is the access expansion itself. The access condition names the population receiving access, the means of access, and any usage restrictions.

**Condition change:** The public benefit is a measurable change in an external condition for a defined population. The mechanism is the intervention that produces the change. The access condition is the evidence required to verify the condition changed and that the claimed population experienced it.

**Ecosystem shift:** The public benefit is a structural change in how a system, protocol, or practice operates, affecting multiple downstream participants. The mechanism is the protocol change, governance change, or standard adoption. The access condition specifies what triggers the shift and who is bound by or benefits from it.

### Mechanism-Evidence Scope Alignment

Each mechanism type constrains the minimum evidence scope required at completion verification:

- Output production: independently accessible deliverable (the output must be publicly accessible, not just claimed as produced).
- Access provision: self-reported usage evidence minimum; independent verification at higher gate configurations.
- Condition change: independent measurement source required; self-report-only does not satisfy this mechanism type at completion.
- Ecosystem shift: independent adoption evidence required; the shift must be documentable from sources outside the applicant's control.

### Assessment Procedure

1. Identify which mechanism type is claimed. Where not stated, classify from the application's description of what benefit is produced and who receives it.
2. Confirm the access condition is stated. An access condition is mechanism-specific: it names the terms under which the public benefit claim holds. A generic statement ("this is open source") without naming the license is a partial declaration.
3. Check mechanism-evidence scope alignment against the round's gate configuration. Where the mechanism type requires independent measurement and the round is configured below that evidence scope, flag as a configuration mismatch requiring funder review.
4. Where no mechanism type can be identified from the application text, flag as a gate pre-condition failure.

**Finding options:**

Pass: "Public benefit mechanism declared as [type]. Access condition: [stated condition]. Mechanism-evidence scope alignment: [pass / flag, with explanation]."

Fail: "Public benefit mechanism declaration absent / access condition missing / mechanism type unidentifiable from application text."

---

## Part IVb: Revenue Architecture, Governance Resilience, and Development Stage Procedures

These three procedures apply at entry gate. Each produces a classification that feeds into the additionality declaration assessment (Part XII) and the gate evidence configuration.

### Revenue Architecture Classification

Classify the applicant's revenue architecture into one of four types:

- Grant-only: the entity's sole or primary revenue source is grant funding. No commercial revenue, service contracts, or token sale proceeds are present or expected within the grant period.
- Fee-for-service: the entity earns revenue by providing defined services to identified clients under explicit terms. Grant funding supplements service revenue for work that does not generate fees.
- Commercial: the entity has material commercial revenue from product sales, licensing, token appreciation, staking rewards, or other market transactions. Grant funding is additive to a primarily commercial revenue base.
- Hybrid: the entity has multiple significant revenue streams including a mix of grants, fees, and commercial revenue.

**For commercial and hybrid types:** Require that the additionality declaration specifies explicitly what the grant funds that commercial revenue does not. The claim that commercial revenue is insufficient without a grant is not self-evidencing; the applicant must name the specific scope boundary.

**Assessment procedure:** Search for: active token contracts (governance or utility), service agreements mentioned in the application, product pricing pages, treasury disclosures, prior round history showing commercial revenue, and any VC or institutional investment. Classification into grant-only when commercial signals exist is a material classification error.

### Governance Resilience Check

Classify the applicant's governance resilience into one of three states:

- Single: all material decisions (fund deployment, roadmap, publication) reside with one natural person, and that person is not substitutable within the grant period without a material change to the project.
- Partial: multiple contributors exist but one person holds veto or exclusive control over the primary deliverable. The project would survive the loss of a secondary contributor but not the primary.
- Resilient: no single person can unilaterally block delivery or fund deployment. At least two contributors have both the access and the mandate to continue the project independently.

**How it affects assessment:** Single-contributor governance is not a gate failure but it is a risk factor that surfaces in the recommendation. At the "Fund with conditions" finding, single-contributor risk is a standard condition to name. At the "Do not fund" threshold, single-contributor governance combined with an unfulfilled prior obligation record elevates the adverse signal weight.

### Development Stage Classification

Classify the applicant's development stage into one of five stages:

- Stage 1: Proof of concept. A prototype, minimal viable product, or experimental implementation exists. No production users or sustained usage evidence.
- Stage 2: Early adoption. The product or service has a small number of active users or participants with documented usage. Feedback loops exist.
- Stage 3: Growth. The product or service has a growing user base, documented traction, and a defined scaling pathway.
- Stage 4: Established infrastructure. The product or service is operationally stable, has sustained usage, and is relied on by other systems or organizations as a dependency.
- Stage 5: Retroactive recognition. The contribution was completed before the grant round and the application seeks retroactive support for prior impact.

**Stage-obligation mode consistency check:** Stage 1 and Stage 2 declarations are most consistent with build-obligation mode. Stage 3 and Stage 4 declarations are most consistent with change-obligation or continuation modes. Stage 5 declarations should use retroactive-obligation mode. A Stage 4 applicant submitting a build-obligation application should be examined for whether the deliverable is genuinely new or whether it extends existing infrastructure. A Stage 5 applicant submitting a build-obligation application is a classification inconsistency requiring explanation.

**Stage-round alignment check:** Where the round specification declares a target stage range (e.g., "Stage 1 through Stage 3 only"), verify whether the applicant's declared stage falls within range. A Stage 4 applicant in a Stage 1-3 round is a configuration mismatch requiring funder review; it is not automatically a gate failure, as the funder may accept it by exception.

---

## Part V: Sufficiency Architecture Declaration Procedure

The sufficiency architecture declaration is also a pre-condition for entry gate assessment, submitted alongside the organizational identity declaration. It collects four required elements.

### Element 1: Scope Declaration

**What is required:** The specific program, sub-entity, or aspect of the applying entity's work that this application covers, stated clearly enough that an independent reviewer could determine what falls within it and what falls outside it.

**Where the application covers the entire entity's operation:** This must be stated explicitly. Most applications cover a specific scope within a larger entity; declaring that scope allows evaluators to assess additionality, attribute outcomes, and understand how this grant fits within the entity's broader funding architecture.

### Element 2: Sufficiency Position

**What is required:** One of four declared positions, assessed at the declared scope, not at the entity level overall:

- Critical gap: resources cover less than half of full scope requirements and the program's viability depends on closing this gap.
- Partial: resources cover more than half but the program operates below intended capacity.
- Approaching: resources are sufficient for current operations but not for the next intended scope expansion.
- Surplus: resources exceed current scope requirements in the current period.

**Corroborating evidence requirement:** Where the round is configured at independent review evidence strength or above, a self-report-only sufficiency position declaration does not satisfy this element. Corroborating evidence may include: public treasury disclosures, on-chain funding history, documented parallel funding commitments, or a prior round's gate record confirming the declared position. Where corroborating evidence is not available, the applicant must state this explicitly and explain why. Newly formed entities with no funding history must state that explicitly and declare their position on the basis of projected costs versus available resources.

Self-report-only declarations are permitted at evidence strength levels below independent review. They must be labeled as self-reported in the evaluation finding.

An entity with multiple programs may be at critical gap on one program and surplus on another; each application declares its own position at its own declared scope.

### Element 3: Portfolio Context Statement

**What is required:** How other funding sources in the applying entity's funding architecture address other scopes or aspects of the entity's work.

**Distinction from concurrent funding disclosure:** Concurrent funding disclosure (Part II, Dimension 4) asks about other funding for the same scope. The portfolio context statement asks how the entity has organized its pursuit of sufficiency across all its programs.

**Critical rule:** The presence of other funding sources for other scopes is expected and is not a disqualifier. Silence about other funding sources in an entity with multiple programs requires explicit explanation.

**Corroboration note:** Where co-funding is documented in a publicly verifiable coordination record before any work begins, that record constitutes independently verifiable evidence of the portfolio context declaration. It distinguishes declared co-funding (asserted without independent verification) from confirmed co-funding (verifiable from a record outside any single program's control).

### Element 4: Grant Contribution Statement

**What is required:** What specific gap at the declared scope this grant would close, and what the sufficiency position at that scope would be after the grant's contribution.

**Assessment note:** This is a declaration of where in the sufficiency architecture the grant fits, not a promise about what will be achieved.

---

## Part VI: Prior Work Attribution Assessment

This assessment is required whenever any entry gate submission cites prior work as evidence of capability, track record, or past contribution. It applies to all three obligation modes: build-obligation applicants who cite prior deliverables as evidence of capacity; change-obligation applicants who cite prior outcomes as evidence of a measurable baseline or established methodology; retroactive-obligation applicants whose entire entry submission consists of prior work.

The prior work attribution statement derives from the contributing entity state of the Entity Boundary primitive (CROSS+WALKRI Primitives Foundation, Layer 2).

For each piece of prior work cited, three questions must be answered:

### Question 1: Entity of Performance

Under which legal entity or organizational context was the cited work performed?

If the work was performed as an employee, contractor, or contributor to an organization that is not the applying entity, that organization must be named. If the work was performed under the applying entity's own resources and governance, that must be stated explicitly.

**Assessment:** Verify that the entity named is specific. "Personal project" without a legal entity declaration, or silence on the organizational context, does not satisfy this question.

### Question 2: Applicant's Relationship at the Time and Current Status

What was the applicant's role in the entity under which the work was performed? What is the current status of that relationship?

An individual who founded a project within an organization and has since departed is in a materially different position from an individual who founded an independent project they have controlled throughout. A contributor who wrote 30% of a codebase held by another entity is in a materially different position from the entity that owns and maintains that codebase. Both the relationship at the time of creation and the relationship at the time of application must be stated.

### Question 3: Current Ownership and Access

Who currently holds the intellectual property rights to the cited work, who controls the deployment or codebase, and who has the user relationship with any users cited as evidence of impact?

If the applying entity does not hold the IP, does not control the deployment, or does not have the relationship with the cited users, this must be stated.

**Critical rule:** A claim of prior contribution to a project does not confer the right to represent that project's user base or codebase as the applicant's own in a continuation or retroactive funding application.

**Adverse signal implication:** An applicant who cannot truthfully complete the attribution statement for their cited prior work has surfaced a misrepresentation in the core evidential basis of their application. An application whose track record is built on work performed under a different entity, without that entity's knowledge or endorsement of the application, is claiming accountability for outcomes the applicant did not control and cannot warrant continuing. Treat this as an active adverse signal requiring disclosure and clarification before the gate assessment proceeds.

---

## Part VII: Indicator Field Assessment

CROSS requires applicants to self-specify their outcome indicators. Assess each of the 11 fields for every indicator submitted. Report findings per field, then apply field clustering rules.

The operational definition field must meet WALKRI requirements for inclusion criteria, exclusion criteria, unit of analysis, and edge case determination (WALKRI-standard-0_1_0.md, Part III, Criterion 2).

### Field 1: Indicator Name

**Pass:** Concise, descriptive, and unique within the indicator set.

**Flag:** Generic, duplicative, or absent.

### Field 2: Rationale for Indicator

**Mandatory. No waiver.** An indicator set with no rationale field passes no other field assessment until this one is complete.

**Pass:** Names at least one alternative indicator considered and rejected, with a specific reason. Or names a methodological constraint making this the only feasible indicator.

**Flag:** Absent. Generic justification. Restates what the indicator measures without addressing alternatives.

### Field 3: Measurement Form and Evidence Classification

The applicant names the measurement form in plain language. Reviewers classify it against three axes.

**Axis 1 (source type):** On-chain verifiable (accessible from public blockchain data with a named contract or address) / off-chain verifiable (accessible from public sources outside the blockchain) / qualitative or narrative (requires human evaluator).

**Axis 2 (measurement form):** Quantitative (number, proportion, rate, currency, duration) / ordinal (position on a defined ordered scale) / binary (met or not met against named completion criteria) / qualitative (documented condition or artifact assessed against named criteria).

**Axis 3 (aggregation type):** Cumulative (values sum across reporting periods) / non-cumulative (values describe a status at a point in time; summing across periods is a construction error).

**Pass:** Applicant names the measurement form in plain language with enough specificity to classify against all three axes without inference. The classification is consistent with the construction methodology in Field 5.

**Flag:** Description so general that axis classification cannot be determined. Classification conflicts with Field 5 methodology. No description present.

**Mode notes:** For build-obligation indicators, the form is typically binary or qualitative; describe what done looks like and how a reviewer would confirm it. For change-obligation indicators, the form is typically quantitative or ordinal; name the unit of measurement and direction of desirable change.

### Field 4: Operational Definition

**Four required sub-fields: all must be present.** Must meet WALKRI criterion specification requirements.

(a) Inclusion criteria: what qualifies as one instance.
(b) Exclusion criteria: what the indicator explicitly does not count. Must name at least one specific exclusion, not merely restate the inclusion criteria inverted.
(c) Unit of analysis: the named entity being counted or assessed.
(d) Edge case determination: at least one example of how an ambiguous instance is resolved.

**Pass:** All four sub-fields present and specific.

**Flag:** Any sub-field absent. Edge case "will be determined at reporting time" (must be specified in advance).

### Field 5: Construction and Aggregation Methodology

**Pass:** Formula or counting rule stated explicitly (or, for build-obligation indicators, the completion determination process: who verifies, by what method). Partial data handling named. Sub-unit aggregation specified if disaggregated data will be combined.

**Flag:** Formula absent. Partial data handling absent. Sub-unit aggregation absent when disaggregation categories are specified in Field 7.

### Field 6: Cumulative or Non-Cumulative

**Pass:** One of the two states named correctly, consistently with Field 11. For binary build-obligation completion criteria, mark as not applicable.

**Flag:** Absent. Inconsistency between Field 6 and Field 11 (cumulative indicator with a point-in-time target, or non-cumulative with a summed target).

### Field 7: Disaggregation Categories

**Ratchet rule:** Disaggregation categories may be added during the grant period. Removing a committed category requires committee approval and documented rationale.

**Pass:** Categories named. If "none committed," explanation provided for why disaggregation is not applicable.

**Flag:** Absent without explanation.

### Field 8: Data Source and Collection Method

**Pass:** Source is named specifically (contract address, named public application programming interface endpoint, named third-party platform, named institutional partner, or named survey instrument). Source is independently accessible. Collection method specifies who collects, when, and how.

For build-obligation indicators: the named artifact location and the named party who will confirm completion criteria are met.

**Flag:** Internal source only with no independent verification path. Source named but not independently accessible. Collection method absent.

### Field 9: Data Cost Estimation

**Pass:** Feasibility attestation present. Cost estimate mapped to a budget line and proportionate to the grant amount. For free sources, confirmation of access is sufficient.

**Flag:** Absent. Cost estimate not mapped to a budget line. Data collection plan requires resources not included in the budget.

### Field 10: Baseline (FROM State)

**Mode-specific assessment.**

For change-obligation indicators: a specific value, measured before the intervention, from a named independently accessible source. Must be consistent with the FROM state named in the gate assessment.

For build-obligation indicators (coordinating-party engagement dimension activated): the documented current absence or inadequacy of the deliverable, with named independent evidence of the gap. Applicant assertion of the gap alone does not satisfy this field.

For build-obligation indicators (coordinating-party engagement dimension not activated): any reasonable plain-language statement of the gap addressed. Advisory only.

For retroactive obligation indicators: the documented state of the prior contribution at the time the award period begins, with named evidence of use.

**Flag (change obligation):** Absent. Aspirational ("we expect baseline data to be available"). Baseline that measures something different from what the indicator tracks. Source absent or not independently accessible.

### Field 11: Target (TO State)

**Mode-specific assessment.**

For change-obligation indicators: same units as baseline. Format matches cumulative/non-cumulative classification.

For build-obligation indicators: completion criteria with enough specificity that an independent reviewer could verify whether they are met. "A working prototype" fails. Named criteria specifying what done looks like and how verification occurs passes.

For retroactive with forward commitment: the named action the awardee commits to, expressed with falsifiable completion criteria.

**Flag:** Target in different units from the baseline. Non-cumulative indicator with a cumulative target. Completion criteria too vague for independent verification. Absent.

### Sustainability and Transition Plan (Optional Field)

Activated by funder configuration. Required for grants above a funder-defined size threshold or grants producing infrastructure, software, or services with ongoing operational requirements beyond the grant period.

**Required content:** What happens to the funded work at grant end (who maintains it, under what conditions it remains publicly accessible, what operational costs are required). How those costs will be covered after the grant ends (name the expected source with enough specificity to assess plausibility). Where the funded work will be handed to another party: the identity of the receiving party and the conditions of the transition. Where the funded work reaches a defined end state after which maintenance is not required: a specification of that end state and the conditions under which it will be declared reached.

### On-Chain Execution and Verification Instruments (Contract-Centric Deliverables)

For interventions where the primary deliverable is a smart contract, protocol, or on-chain system, the indicator specification must additionally contain four sub-fields:

**Invariant specification:** A narrative description of the invariants or properties the contract must satisfy (for example, conservation of balances, absence of re-entrancy on named functions, bounded slippage for a specific operation). This is the human-readable counterpart of the formal specification used in verification tools.

**Verification method:** A statement of whether the invariant will be assessed by formal verification, independent audit, manual review of on-chain behavior, continuous monitoring, or a combination. If formal verification is used, the named tool or approach must be specified (for example, model checking, theorem proving, or a named framework).

**Verification artifact:** The concrete artifact that constitutes completion evidence: a proof object, an audit report from a named firm, or a named contract and query that a reviewer can use to reproduce the behavioral check from public chain data.

**Failure surface:** At least one example of behavior that would constitute a failure to meet the invariant, and how such a failure would be detected by the chosen instrument.

**Assessment rule:** Indicators that rely solely on applicant-controlled test suites or private monitoring dashboards, without any independent verification instrument, fail the integrity standard. They may appear as supplementary evidence but do not satisfy the minimum verification requirement at the completion gate for contract-centric deliverables.

### Field Clustering Rules

Apply after completing the 11-field assessment. Each trigger independently activates additional mandatory fields.

**If measurement form = composite/multi-component:** Component indicators, weightings, and aggregation rule become mandatory.

**If privacy-sensitive accommodation is invoked (Part XVII):** Specific harm field and alternative methodology field become mandatory.

**If any venture capital or institutional investment is disclosed in Dimension 4:** Investor name, governance rights, and scope relationship fields become mandatory.

**If Dimension 9 is active:** A/B/C classification is mandatory.

**If progress verification gates are configured:** Milestone or progress specification fields become mandatory for each tranche gate.

**If Dimension 11 is active AND sub-contracting exceeds 20% of the award:** Sub-contractor disclosure fields are mandatory.

**If retroactive round:** Prior award disclosure is mandatory (all prior awards for the same or overlapping contribution).

---

## Part VIII: Conflict of Interest Tier Classification

**Governing standard:** The reasonable third-party test. A conflict of interest finding is warranted when a reasonable third party, examining the relationship, would question the objectivity of the reviewer or the independence of the applicant.

**Process requirements:** Pre-review declaration submitted to the named receiving function before any application is opened. Post-review certification after assessment. Bidirectionality: reviewers disclose to applicants, applicants disclose to reviewers and committee.

### Procedure for Tier Classification

Apply the following in order. Stop at the first tier that applies.

**Tier 1 (categorical bar, no waiver):**

- Direct financial interest: equity, revenue share, or token holdings above the materiality threshold (funder-configured default: greater than 1% of token supply or greater than \$5,000 in value at time of review).
- Family relationship: spouse, domestic partner, parent, sibling, child, or household member.
- Prior funded work in the same area from the same funder, where the reviewer's funded work is directly related to the applicant's scope.
- Named on the applicant project's public materials (compensated or not, including advisory roles listed publicly).

**Attestation integrity provision:** A Tier 1-conflicted party may not serve as the independent reviewer or sign an attestation confirming that applicant's gate evidence, regardless of the attestation format used. A Tier 1-conflicted party who signs an on-chain attestation, issues a signed document, or issues a credential confirming milestone completion has not satisfied the independent review requirement; the attestation does not meet the evidence strength standard regardless of its format.

**Tier 2 (disclosure required, qualified waiver possible):**

A qualified waiver requires: (a) a written justification submitted to a named authority other than the conflicted party, (b) approval granted before participation, not after, and (c) documentation in the review record. Waiver is not available where the relationship creates a financial interest.

- Employment with the applicant in the past 36 months.
- Co-authorship or collaboration with applicant principals in the past 48 months.
- Mentor or student relationship (no expiration).
- Governance token voting on the applicant's proposals.
- Decentralized autonomous organization co-governance roles involving both parties.
- Honorarium, award, or gift from the applicant in the past 12 months.
- Future employment arrangements under discussion.
- Organizational conflict: reviewer's employer has a material financial relationship with the applicant.
- Organizational role conflict: holds a paid or unpaid leadership, advisory, or operational role in another organization applying to this round, or that received awards from this funder in the most recent prior round in the same program area. This disclosure is required even when no direct financial relationship exists between the reviewer and the applicant under review; the structural position across multiple funding relationships is itself the conflict.
- Active job negotiations with the applicant organization.

**Attestation note for Tier 2:** A Tier 2-conflicted party requires a qualified waiver before serving as attestor for that applicant, using the same procedure as the reviewer waiver requirement. Programs must verify reviewer and attestor conflict status before accepting any attestation as satisfying independent review evidence strength.

**Tier 3 (disclosure encouraged):**

- Social or community relationships.
- Cross-round interactions in different program areas.
- Informal mentorship without ongoing engagement.

**Funder-side consulting conflicts.** Where an evaluation participant is under a paid consulting or service contract with the funder at the time of evaluation, that relationship must be disclosed to the receiving function regardless of its connection to any specific applicant, for any paid engagement covering the same program area as the applications under review.

Where the consulting arrangement covers the same program area as the applications under review: Tier 2 qualified waiver applies.

Where the consulting arrangement constitutes the primary mechanism through which the reviewer receives income from the ecosystem being evaluated: categorical bar applies. The categorical bar does not require the reviewer to have a direct financial relationship with any specific applicant; structural income dependency on the funder's continued operation and on favorable award decisions is itself the conflict.

**Web3-specific categories (apply same tier structure):**

- Token holdings above the materiality threshold: Tier 1.
- Token holdings below the materiality threshold: Tier 3.
- Governance token voting on applicant proposals: Tier 2.
- Core contributor or unpaid advisory status listed on public materials: Tier 1.
- Investment from the same named investor: Tier 2.
- Decentralized autonomous organization co-governance roles: Tier 2 or Tier 3 depending on nature.

---

## Part IX: Data Quality Standards Assessment

Apply the five WALKRI data quality standards in order to any indicator claim or proposed measurement methodology (WALKRI-standard-0_1_0.md, Part V). A claim that fails any standard fails the data quality assessment regardless of performance on others.

### Standard 1: Validity

**Operative test:** Remove the applicant from the verification process. Can an independent reviewer confirm that the data collected measures the claimed condition, using only the indicator specification and the named data source?

**Pass:** Logical chain from data to result is explicit and independently verifiable. For build-obligation indicators: the completion criteria have a documented logical chain to the deliverable being what the applicant claims.

**Fail:** Chain requires the applicant's interpretation, cooperation, or access to materials not named in the indicator specification. Macro-level metric claimed as evidence of specific project contribution without documented causal chain.

### Standard 2: Integrity

**Operative test:** Does any evidence for this application's claims originate from a source independent of the applicant?

**Pass:** Named independent verification mechanism present for each material claim.

**Fail:** All evidence is applicant-controlled with no named independent corroboration. For build-obligation: the named verifying party for completion criteria is the applicant themselves.

### Standard 3: Precision

**Operative test:** Is the claimed effect larger than the variance of the measurement method? For build-obligation indicators: are the completion criteria specific enough to distinguish a passing deliverable from a failing one?

**Pass:** Measurement precision is documented and consistent with claimed effect size. Build-obligation criteria distinguish done from not done without ambiguity.

**Fail:** Claimed effect within the instrument's margin of error. Build-obligation criteria accept any output as qualifying ("a working prototype" with no further specification).

### Standard 4: Reliability

**Operative test:** If the methodology changed between periods, is the change documented with a comparability assessment?

**Pass:** Same methodology across periods, or changes documented with comparability assessment. First-time applicants: methodology is specified with enough precision to apply consistently.

**Fail:** Methodology change without documentation. Different definitions of the same indicator used across periods without explanation.

### Standard 5: Timeliness

**Operative test:** Is the data current to the reporting period? Does collection frequency match the decision cycle?

**Pass:** Data collection timing specified, data covers the relevant period, reporting frequency matches the decision cycle.

**Fail:** Data collected in a prior period reported as current. Annual data collection for a quarterly disbursement structure. Gate evidence submitted for a period not covered by the collection methodology.

---

## Part X: Grant Configurator Question Sequence

Run when a funder wants to generate a round specification. Ask questions in the following order. Compile the output into a round configuration document after all questions are answered.

The Grant Configurator produces the Commit stage output of the CLEAR lifecycle (Commit, List, Evaluate, Attest, Register). The Commit stage output is a machine-readable round specification published before any application opens. It is the authoritative coordination instrument for that round: applicants interact with the round specification, not with the CROSS standard directly. The canonical format for this output is specified in CROSS-canonical-round-configuration-schema-0_1_0.md. Publishing the round specification in this format enables grantees to import it into Theory of Change tools and receive structured guidance toward a conformant application.

Before publishing any round, verify that these pre-publication requirements are met: (1) a plain-language applicant-facing summary of the round's requirements is published before the round opens and remains publicly accessible for the full duration; (2) the full application question list is published before the round opens, publicly accessible without creating an account or contacting the funder, showing every question in order with the response form type and the criterion intent for each question; (3) all gate criteria meet WALKRI criterion specification requirements at Standard certification level or above before the round opens.

**Q0: Program type and runbook selection.**

Does this program match any of the thirteen runbook configurations across CROSS-runbooks-0_1_0.md and CROSS-runbooks-0_2_0.md?

Original six (0_1_0): Discovery Sprint, Staged Development, Community Allocation with Build Obligation, Retroactive Impact, Graduated Evidence, Institutional Conformance.

New seven (0_2_0): Adaptive Learning Cycle (inter-cycle reflection stage), Multi-Cycle Retrospective Program (multi-cycle retrospective assessment), Threshold-Scaled Independence (threshold-based independent evaluation), Participatory Indicator Selection (indicator menu with confirmation gate), Computational Retroactive Allocation (formula-based allocation with impact chain declaration), Portfolio Benchmark Program (funder-side portfolio accountability), Beneficiary Accountability Gate (community feedback mechanism as gate element).

If yes, load the matching runbook as the starting configuration and surface its default gate configuration. Multiple runbooks may be combined per the combining guidance in CROSS-runbooks-0_2_0.md. If no match, proceed through the full sequence.

For program type bundle context: the ten program type bundles in the bundles/ directory provide combined CROSS runbook + WALKRI field specifications + compatibility map for: Web3/public goods, international development, research grants, community foundation, corporate CSR/impact, challenge prizes, participatory/equity, Islamic/endowment, European philanthropy, and fiscal sponsorship.

**Q1: Round identification.**

Round name, funding organization, opening date, closing date, stage number (if multi-stage), named conflict of interest receiving authority.

**Q2: Accountability mode and program structure.**

Which obligation mode: build / change / retroactive / compound / multi-stage with different modes per stage? For retroactive rounds: is a forward commitment requirement configured?

For compound rounds: the program declares a program-level Change obligation and a set of Build component obligations whose completion forms the causal pathway toward the Change. The canonical round configuration must carry both a complete change_specification block and a components array. Each component must carry a contribution_to_change statement. See Section D of Part III for the compound entry gate procedure.

**Q3: Eligibility domain.**

Work type, open source requirement and license, Digital Public Good classification requirement, organizational type restrictions.

**Q4: Funding amount range.**

Minimum and maximum award amounts. Tiered categories if applicable. The Coordination Scaling Standard tier calibration follows from Q4 and Q6 combined.

**Q5: Program-level continuation gate (multi-stage programs only).**

For each stage transition: evidence scope, evidence strength, obligation mode of the next stage, infrastructure declaration if at independent review level or above. Cost-effectiveness consideration active at Stage 2-to-Stage 3 transition? Sustainability stance required at continuation?

**Q6: Public impact claim scope.**

Geographic or network scope of expected impact claims. For change obligation: is beneficiary validation required? For build obligation: is the coordinating-party engagement dimension activated?

**Q7: Track record requirement.**

Minimum track record for eligibility. Independent verification requirement. First-time applicant policy.

**Q8: Conflict of interest configuration.**

Tier 2 waiver permitted or all Tier 2 as categorical bars? Token holdings materiality threshold?

**Q9: Optional dimensions.**

Environmental and social impact assessment: activate? Gender equity: activate? Procurement integrity: activate?

**Q10: Round-level common indicators.**

Any indicators required of all applicants? If yes, provide the full measurement form description (not just a data type label), source type, measurement form, aggregation type, operational definition, construction methodology, disaggregation categories, and named data source. Applicants complete baseline and target fields; indicator definition is locked.

**Q11: Round-level gate configuration.**

For each active gate: evidence scope (output / usage / outcome / impact), evidence strength (self-report with documentation / third-party verifiable / independent review / independent evaluation), causality stance (attribution or contribution), infrastructure declaration if at independent review level or above. For build-obligation completion gates: confirm that the public accessibility requirement is active (mandatory; cannot be configured out). For retroactive rounds: publish the assessment rubric and name the review panel.

For gates configured at independent review level or above: confirm that reviewer calibration is included in the infrastructure declaration. The calibration exercise must present reviewers with the published gate criteria, criterion intents, and compliance thresholds, and must include at least two worked examples (one passing, one failing) with documented assessments. Inter-rater consistency must be checked for multi-institution review panels before live applications are assessed.

**Q12: Reporting frequency.**

How often must grantees report? Options: monthly, quarterly, semi-annual, milestone-triggered, grant end only.

**Q13: Pre-award indicator confirmation window.**

Is a pre-award indicator confirmation window configured? If yes, specify the window duration. Confirm the funder understands the silence-as-confirmation rule: failure to respond within the window constitutes written confirmation; the confirmed indicator specification governs all subsequent gate assessments.

**Q14: Concurrent funding presence and Part VI-A activation.**

Does the program anticipate concurrent funding disclosures? If yes, confirm that additionality declaration and outcome credit attribution requirements (Part XII) are configured and visible in the published gate configuration.

**Q15: External standard references.**

For any gate that references an external standard: confirm that the reference includes the identifier, version anchor, scope, and compliance threshold. A reference without a compliance threshold delegates interpretation to reviewers and is a gate criterion specification failure.

**Q16: Round specification pre-commitment and canonical format.**

Will the program publish a verifiable commitment to the round specification before the application window opens? The canonical format for this commitment is specified in CROSS-canonical-round-configuration-schema-0_1_0.md. Publishing in this format enables grantees to import the specification into Theory of Change tools and receive structured guidance toward a conformant application. A pre-commitment record is also the evidentiary basis for applicant redress rights in procedural appeals alleging criteria changed after submission.

---

## Part XI: Gate Evidence Assessment

Run this procedure when evaluating a progress verification gate submission or completion verification gate submission against the round's published gate configuration.

### What to confirm before assessing evidence

From the round specification, confirm: (a) the obligation mode; (b) the evidence scope required at this gate (output / usage / outcome / impact); (c) the evidence strength required (self-report with documentation / third-party verifiable / independent review / independent evaluation); (d) whether an infrastructure declaration exists naming the verification contact; (e) whether a causality stance has been declared (attribution or contribution); and (f) whether the gate is developmental (progress verification) or summative (completion verification).

### Gate Function: Developmental vs. Summative

**Progress verification gates are developmental:** Their purpose is to surface what needs to change before the next gate, not to render a final judgment. A progress gate resulting in a hold or revision request is functioning correctly. Grantees retain iteration rights between progress gates. The appropriate reviewer posture is formative.

**Completion verification gates are summative:** Their purpose is to render a documented determination of whether the obligation was met as specified. A completion gate failure is a final judgment; it does not trigger iteration rights, though it does trigger redress rights under Part XVI. Do not negotiate outcomes at a completion gate or treat partial progress as acceptable without a documented gate amendment.

### Pre-Award Indicator Confirmation

Where a pre-award indicator confirmation window was configured: confirm whether written confirmation of the indicator specification was issued. If yes, the confirmed specification governs this gate assessment; the funder may not impose requirements at the completion gate that were not visible in the confirmed specification. If the window elapsed without response, silence constitutes confirmation.

### Evidence Scope Assessment

**Output evidence:** Does a specified artifact exist? For build-obligation gates: is the deliverable publicly accessible from the named location? Does it meet the published completion criteria? For contract-centric deliverables: does a verification artifact exist demonstrating that the contract satisfies the specified invariant set?

**Usage evidence:** Is the deliverable being used by parties outside the applicant's control? Is the evidence independently accessible (on-chain data, named public analytics, named third-party corroboration)?

**Outcome evidence:** Has a measurable change occurred in the specified population, documented against the baseline established at entry? Is the data current to the reporting period?

**Impact evidence:** Is a credible causal link established between the funded work and the measured change, through methodology sufficient to support causal inference?

### Evidence Strength Assessment

**Self-report with documentation:** Grantee narrative with supporting links, files, or on-chain data references. Assess: does the narrative reference the correct period? Are supporting links accessible?

**Third-party verifiable:** Evidence accessible to any reviewer with internet access from sources outside the applicant's control. Assess: is each claimed source actually independently accessible without the applicant's cooperation?

**Independent review:** A named party outside the funder-grantee relationship confirms the submitted evidence meets the completion criteria. Assess: was the reviewer named in the infrastructure declaration? Has their confirmation been received and documented? Does the reviewer hold any Tier 1 or unwaived Tier 2 conflict with the applicant?

**Independent evaluation:** A qualified evaluator conducts a structured assessment. Assess: were the evaluator's qualifications appropriate to the evidence scope? Was the process consistent with the published infrastructure declaration?

### Counterfactual Verification Procedure

When a gate is configured at counterfactual reference level, four elements are required in the grantee's submission:

**Counterfactual baseline:** A documented estimate of what the indicator value would have been during the grant period without the intervention, derived from: historical trend extrapolation from pre-intervention data, a matched comparison group not exposed to the intervention, or a modeled counterfactual with stated assumptions and sensitivity ranges.

**Attribution argument:** A written account of why the observed change is attributable to the intervention rather than to confounding factors, naming the main alternative explanations and explaining why they are insufficient to account for the observed change.

**Comparison period or group:** A defined period or population that serves as the counterfactual reference, described specifically enough that an independent reviewer can assess whether it is an appropriate comparison.

**Independent attestation:** Confirmation from a party outside the grantee organization that the counterfactual method and comparison group are reasonable given the intervention context and available data.

**Where a comparison group cannot be defined** (because the intervention affects an entire ecosystem or operates at a protocol level with universal effects): the grantee must document why a comparison group approach is not feasible and provide a modeled counterfactual with stated assumptions. Absence of a comparison group is not itself a gate failure; absence of a counterfactual estimate and attribution argument is.

### Attribution vs. Contribution Stance

**Attribution stance:** Requires evidence that the intervention caused the observed change. Counterfactual reference (above) is the standard methodology. Appropriate where the funder needs to defend a causal claim to an institutional body, where the intervention is the primary or only active change effort in the target population, or where future funding decisions depend on causal proof.

**Contribution stance:** Requires evidence that the intervention plausibly contributed to the observed outcome, with co-factors named and the mechanism of contribution stated. Does not require a counterfactual. Requires: a named causal pathway from the funded activity to the observed change; a list of other interventions, conditions, or actors that also contributed; and a written account of why the funded intervention's contribution was material rather than incidental.

**Assessment rule:** The causality stance must be declared in the gate configuration. A gate that requires outcome evidence but has not declared a causality stance is under-specified. Flag this as a gate criterion specification failure.

### Continuation Gate Procedure

The continuation gate sits at the program level, not the round level. It is configured before any round opens. When evaluating a continuation gate submission:

**Cost-effectiveness consideration (change-obligation programs at Stage 2 and above):** Does the evidence from the prior stage indicate that further investment in this intervention produces meaningful change relative to available alternatives?

**Sustainability stance:** The grantee must declare one of three positions on outcomes produced in prior rounds:
- Sustained: outcomes are self-sustaining and do not require additional intervention to continue.
- Conditional: outcomes persist under specified conditions independent of this program's funding.
- Dependent: outcomes will not persist without continued intervention. A dependent sustainability stance is not a disqualifier; it is a disclosure requiring an explicit funder choice to sustain rather than only advance.

**Track record assessment:** Where funder-signed gate records from prior stages exist as publicly verifiable records, those records are stronger corroboration than self-reported history for the same reason stated in Part IV: they reflect the prior funder's determination rather than the applicant's characterization.

### Unintended Outcomes Disclosure

Completion gate submissions must include an unintended outcomes disclosure. The grantee identifies any effects, positive or negative, that occurred during the grant period that were not specified at entry and are plausibly connected to the funded work. Silence on this field does not satisfy the disclosure requirement; grantees who state no unintended outcomes occurred must state this explicitly. An unintended negative outcome triggers the Adverse-Signal Engagement Principle for the continuation gate assessment.

### Critical Rule for Completion Verification Gates (Build Obligation)

The gate must confirm that the specified deliverable is publicly accessible before final payment is released. Grantee self-assertion of public accessibility does not satisfy this requirement. A publicly accessible URL must be present and accessible.

### Gate Evidence Finding Options

**Verified:** "Gate verified: evidence submitted meets the published [evidence scope] requirement at [evidence strength] level. [Named verifying party / verification method confirmed]."

**Failed:** "Gate fails: [describe specifically what evidence is missing, what evidence does not meet the published scope or strength requirement, or what completion criteria are not met]."

**Conditional:** "Gate conditionally verified pending: [specific item that must be resolved, named verification method, timeline]."

---

## Part XII: Scope Attribution and Outcome Credit

This assessment is triggered when concurrent funding is disclosed under Dimension 4. Where no concurrent funding exists, this Part does not apply.

### 1. Additionality Declaration (Entry Gate)

Required for any application with concurrent funding. Failure to submit when concurrent funding is disclosed is a gate failure at entry.

The additionality declaration must contain:

**Scope boundary:** A narrative specification of the work, deliverables, or costs funded by this grant that are not funded by any concurrently disclosed source. Specific enough that a reviewer can determine whether a proposed activity lies inside or outside this grant's scope.

**Overlap statement:** A brief statement of where overlap exists between this grant and concurrent sources, if any, and how double funding of the same input is avoided in practice.

**Assurance of non-duplication:** An attestation that the applicant will not knowingly charge the same cost to multiple funders, and that any material changes in concurrent funding affecting this assurance will be reported at the next gate.

**Mode-specific requirements:**

For build-obligation: specify which parts of the deliverable or which development stages this grant covers relative to other funders.

For change-obligation: specify which portion of the intervention pathway (activities, geography, population segment, or time period) this grant is funding relative to other funders.

For retroactive: specify whether the prior contribution has already received retroactive awards from other programs and what forward-facing obligations, if any, this award uniquely creates.

**Token event disclosure:** Token generation events (IDOs, TGEs, ICOs, liquidity bootstrapping pools) and vesting schedules that occurred within the prior 24 months are required disclosures within the concurrent funding field, treated as a form of capital receipt equivalent to grant income. Pending tokens where tokenomics documents or allocation schedules exist must be disclosed as pending TGEs. Non-disclosure of a known past or pending token event is treated as a concurrent funding omission and is investigated as Block J adverse signal.

**IMP Contribution vocabulary (optional framework):** Where the round configuration permits, applicants may structure their additionality declaration using the IMP Contribution vocabulary, which provides three positions:

- Significant improvement: the grant enables an outcome that would not occur without it, representing a qualitative or quantitative improvement over the baseline.
- Prevents deterioration: the grant maintains a current condition that would worsen without the funded work, where the baseline would otherwise decline.
- Helps avoid worse outcomes: the grant reduces the likelihood or severity of a negative outcome that would occur without intervention.

An applicant may claim multiple IMP positions within one application when each is separately delineated with its own scope boundary and counterfactual. Each claimed position requires naming the specific counterfactual: what would happen, to whom, if the grant were not made. A position claim without a counterfactual is an incomplete additionality declaration.

### 2. Outcome Credit Attribution (Completion and Continuation Gates)

Required when concurrent funding is disclosed and outcome or usage evidence is required at a completion verification or continuation gate.

The outcome credit attribution statement must contain:

**Attribution fractions:** A declared percentage allocation of the reported result across all funders that materially contributed to it, including this program. Percentages must sum to 100 percent across named funders and, where relevant, a residual category for un-funded or self-funded contribution.

**Attribution rationale:** A short narrative explaining how the attribution fractions were determined, naming the main factors used (relative funding amounts, timing, specific work packages funded, or other relevant distinctions) and acknowledging material uncertainties.

**Change tracking:** If attribution fractions change between reporting periods for the same indicator, document the reason for the change and its implications for comparability of prior periods.

**Assessment rule:** The failure mode is absence of a declared attribution position where concurrent funding exists, not imprecision in the fractions themselves. Reviewers assess whether an attribution statement is present and coherent with the additionality declaration and the indicator specification.

### 3. Gate-Level Consistency Assessment

Reviewers must assess consistency across all four elements:

- The concurrent funding disclosure (Dimension 4)
- The additionality declaration (Section 1 of this Part)
- The indicator specification (Part VII)
- The outcome credit attribution statement (Section 2 of this Part)

Inconsistencies to flag:

- An additionality declaration asserting unique funding for work that, by the applicant's own description, is also fully funded by another source.
- An outcome credit attribution statement assigning 100% of outcome credit to this funder where multiple concurrent funders are disclosed for the same scope and time period.
- Material changes in attribution fractions across periods without documented rationale.

**Classification:** These are rigor-tier failures, not automatic gate failures. Review committees may request clarification or revision before making a final determination.

---

## Part XIII: Program-Level Theory of Change Architecture

Run when configuring a program-level ToC declaration for a multi-round or multi-stage program. The program-level ToC declaration is recommended but not required for CROSS conformance at the round level. Where declared, these requirements apply.

### Required Elements for Conformant Declaration

A program-level ToC declaration requires: a goal statement, at least one intermediate outcomes register entry, at least one pathway in the pathway registry with a causal mechanism statement and a critical assumptions list, and a round linkage record for each active CROSS round within the program.

### Program Identity Block

Contains: a program name and identifier (stable across all rounds), a domain declaration, a geographic scope declaration, and a program time horizon.

### Goal and Outcome Architecture

Configure the following registers, each with unique identifiers:

**Goal statement:** The ultimate change the program is designed to contribute to. At the population or system level, operating over the full program time horizon.

**Long-term outcomes register (1-4 entries):** Each with a plain-language description and its relationship to the Goal. Long-term outcomes persist after the program's active intervention period ends. Attribution of any single project to a long-term outcome is an argued contribution, not a directly measured one. Evidence at long-term outcome level is appropriate for program-level evaluation, not for individual project completion verification.

**Intermediate outcomes register:** Each with a plain-language description and its declared relationship to one or more long-term outcomes. The primary accountability level for most institutional funders operating within a multi-year program. Typically measurable within the program time horizon but not within a single project cycle.

**Short-term outcomes register:** Each with its declared relationship to one or more intermediate outcomes. The primary accountability level for individual project completion gates in change-obligation rounds. The highest outcome level at which a completion gate can reasonably require outcome evidence rather than output evidence.

**Critical distinction:** A project claiming to produce an intermediate or long-term outcome at completion, without a declared short-term outcome as the measurable step in that direction, is making an attribution claim that exceeds what a single-cycle completion gate can verify.

### Pathway Registry

Each pathway in the registry requires:

- A pathway identifier (stable across rounds).
- A source node identifier and its ToC level.
- A target node identifier and its ToC level.
- A causal mechanism statement (an "if-then" statement declaring how the source produces or contributes to the target).
- A critical assumptions list (conditions external to the program's direct control that the causal claim depends on).
- An external risk list (conditions that could disrupt the pathway external to the funder's control).
- Dependency declarations (a list of other pathway identifiers that this pathway depends on).
- A Theory of Build tag: `build` (Inputs to Outputs) or `change` (Outputs to Outcomes).
- For pathways tagged `build`: an optional intended outcome level field declaring which outcome level the built artifact is designed to enable.
- A causality stance tag: `attribution` or `contribution`. Where a pathway is tagged `attribution`, rounds advancing it should configure completion gates at counterfactual reference level. Where tagged `contribution`, rounds should require the contribution analysis elements. A mismatch between a pathway's causality stance tag and its associated rounds' gate configurations is a conformance flag.
- A specification directionality tag: `planning` (defined starting from the desired target node and working backward) or `delivery` (defined starting from the available source node and working forward). A portfolio in which all pathways are delivery-mode specified will tend to show structural gaps at intermediate and long-term levels. Programs declaring OECD DAC alignment are encouraged to include at least one planning-mode pathway connecting activities to the Effectiveness or Impact criteria.

### Round Linkage Record

Each active CROSS round links to the program-level ToC declaration through a record containing: the primary pathway identifiers the round's projects are designed to advance, the primary ToC level the round operates at, and a portfolio position declaration (initiating, continuation, or convergence round).

---

## Part XIV: Institutional Framework Alignment

CROSS v0.4.7 holds confirmed compatibility with 95+ frameworks. The full corpus is documented in the statements/ directory of the CROSS+WALKRI repository. The CROSS-WALKRI-primitives-framework-index-0_1_0.md maps each underlying measurement primitive to its strongest framework exemplars, enabling classification of new frameworks without requiring individual statements.

When a user asks how CROSS conformance maps to a specific framework, apply the primitive-first approach: identify which primitive the framework exemplifies, then apply the corresponding CROSS gate or field provision. The following subsections provide the most commonly requested mappings. For frameworks not listed here, consult the primitives framework index.

### OECD DAC (DCD/DAC(2019)58/FINAL)

The six criteria map to CROSS gate architecture:

- Relevance: entry specification gate (does this intervention respond to the named FROM state in the defined population?)
- Coherence: coherence disclosure (how does this intervention relate to other known interventions in the same problem area?)
- Effectiveness: progress verification gate (is the intervention producing evidence of movement toward the TO state?)
- Efficiency: data cost estimation field and sustainability plan requirement
- Impact: completion verification gate (does the completion evidence demonstrate that the TO state was reached?)
- Sustainability: continuation specification gate and sustainability plan

A CROSS-conformant program with OECD DAC alignment declared satisfies all six DAC criteria structurally. The criteria are not a separate checklist. All bilateral and multilateral agency frameworks in the corpus (USAID, DFAT, JICA, AFD, GIZ, Global Affairs Canada, SDC, Sida/Norad/Danida, IDRC, World Bank, ADB, AfDB, IDB, EBRD, GCF, GEF, and others) are OECD DAC-aligned and are satisfied by the same structural alignment.

### USAID PIRS (ADS 201)

CROSS Part V's eleven-field indicator specification is a strict superset of the nine PIRS required elements. WALKRI's five data quality standards are structurally identical to USAID's five data quality criteria. A CROSS+WALKRI-conformant program produces PIRS documentation as a structural output. Full field mapping in the published USAID-PIRS-CROSS-WALKRI compatibility statement.

### IRIS+ / IMP Five Dimensions

CROSS's eleven-field indicator specification is a strict superset of IRIS+ indicator metadata requirements. The IMP Five Dimensions (What, Who, How Much, Contribution, Risk) map to CROSS's Theory of Change hierarchy, population scope declaration, indicator specification, causality stance field, and evidence strength taxonomy respectively.

### DAOIP-5 (DAOstar/Metagov)

CROSS round configurations are expressible as DAOIP-5 GrantPool objects. Gate evidence and grantee reports are expressible as DAOIP-5 Attestation objects. Format agnosticism principle governs the record format. Complete interoperability specification in Part IX-A of the standard.

### US Federal Education Evidence Framework (ESSA / WWC / EIR)

ESSA Tier 4 (logic model + ongoing study commitment) is exactly what CROSS's entry specification gate requires: the Theory of Change hierarchy, eleven-field indicator specification, and causality stance declaration all committed before applications open. ESSA Tiers 1-3 map to CROSS's causality stance field: Tier 1 = attribution with RCT design; Tier 2 = attribution with quasi-experimental design; Tier 3 = contribution with comparison group. The EIR Program's Early-to-Mid-Phase continuation gate maps to CROSS's continuation gate configured at the appropriate WWC evidence standard.

### US Federal Workforce and Human Services (WIOA, SNAP-Ed, Head Start, AmeriCorps, CSBG ROMA)

All five frameworks exemplify the pre-specification primitive: indicator sets established nationally before any program year begins, corresponding directly to CROSS's entry specification gate. WIOA's six fixed regulatory indicators are the most fully realized application of this primitive at the workforce system level. SNAP-Ed's four-level ecological structure maps to CROSS's Theory of Change hierarchy. Head Start's ELOF five developmental domains are the entry gate indicator set for child outcomes programs. AmeriCorps's national prescribed output/outcome pairing menu is a Build-plus-Change entry gate applied at the national level. CSBG ROMA's Six National Goals are the Change obligation indicator framework for community action agencies.

### US Federal Health Programs (SAMHSA NOMs, HRSA UDS, Ryan White, LIHEAP)

All four exemplify the pre-specification and disaggregation ratchet primitives at the federal health program level. SAMHSA NOMs' client-level baseline interview is the entry specification gate and disaggregation ratchet applied to behavioral health. HRSA UDS's 16 mandatory clinical quality measures are the pre-specified Change obligation indicator set for Federally Qualified Health Centers. Ryan White HIV/AIDS RSR's eUCI longitudinal linking is the disaggregation ratchet at its most granular. LIHEAP's three statutory measures include the only US human services statutory measure explicitly encoding a counterfactual element (Measure 2: energy crisis prevention), mapping directly to CROSS's causality stance field.

### Environmental and Carbon Finance (IUCN NbS, Verra VCS, REDD+, Gold Standard, GCF/GEF)

All exemplify the causality stance primitive with a mandatory counterfactual baseline. Verra VCS additionality is CROSS's additionality argument applied to carbon credits. REDD+ FREL/FRL is CROSS's counterfactual baseline at national scale. IUCN Global Standard for NbS Criterion 2's biodiversity benchmark maps to CROSS's baseline field and counterfactual specification. Gold Standard's mandatory dual-track reporting (GHG outcomes and SDG co-benefits) maps to CROSS's multi-dimensional outcome declaration capability.

### Islamic and Endowment-Based Giving (AAOIFI, IsDB)

AAOIFI Zakat Standard 35's eight eligible recipient categories are the most historically precedented pre-specified population constraint in any giving tradition, mapping to CROSS's population scope declaration. AAOIFI Waqf Standard 33's perpetuity constraint maps to CROSS's sustainability stance field at its most stringent: corpus principal must be preserved in perpetuity, only income can be disbursed.

### European Philanthropy (ESIF/CPR, EVPA, PHINEO IOOI)

ESIF's EU added value criterion is a regulatory form of CROSS's additionality argument with no equivalent elsewhere: it requires programs to demonstrate what EU-level investment produces beyond what member states would have achieved without EU funding. ESIF's mandatory common indicator sets are the most formally codified pre-specified indicator sets in any regional grant system. PHINEO IOOI (Input-Output-Outcome-Impact) maps directly to CROSS's Theory of Change hierarchy.

### Faith-Based Development (CRS ProPack, World Vision LEAP, USCCB/CCHD)

CRS ProPack's five-step MEAL system design embedded in project design is the functional equivalent of CROSS's entry specification gate at the sub-award partner level. World Vision LEAP's Reflect stage introduces the inter-cycle reflection stage primitive (Runbook 7 in CROSS-runbooks-0_2_0.md), a named programme cycle stage sitting between the completion gate of one cycle and the entry gate of the next. USCCB/CCHD's faith-mission alignment criterion is a WALKRI compliance threshold requirement with no secular parallel.

### Kellogg Logic Model

Activities = CROSS activities tier. Outputs = CROSS outputs tier. Short-term outcomes = CROSS outcome tier. Long-term outcomes/impact = CROSS goal tier. Resources/inputs = concurrent funding disclosure and organizational identity declaration. A CROSS-conformant program naturally produces Kellogg-compatible documentation as a structural consequence.

### New Primitives (v0.4.7)

Four new structural primitives were identified during the v0.4.7 compatibility research and are not yet in the Primitives Foundation. When a program implements one of these, reference the corresponding runbook:

- Inter-cycle reflection stage: a formally required stage between programme cycles for learning institutionalization. Runbook 7.
- Multi-cycle retrospective assessment: a formal evaluation spanning all prior cycles in a multi-year grantee relationship. Runbook 8. Source: NED Cumulative Assessment Report.
- Portfolio-level continuation benchmark applied to funder: a published performance threshold applied to the funder's full program portfolio. Runbook 12. Source: SBIR/STTR statutory benchmarks.
- Beneficiary accountability mechanism as gate element: community feedback and complaint response required as formal gate elements, not optional MEAL add-ons. Runbook 13. Source: CRS ProPack, World Vision LEAP.

---

## Part XV: Recommendation Generation

After completing the gate assessment and all active dimension evaluations, generate a recommendation using only the three canonical terms below.

**Canonical recommendation vocabulary:**

- Fund
- Fund with conditions
- Do not fund

**Recommendation logic:**

**Fund:** Entry specification gate passes. Organizational identity declaration and sufficiency architecture declaration are complete and conformant. All active mandatory dimensions meet requirements. No categorical conflict of interest bars. No undisclosed concurrent funding. No adverse signal suppression. Data quality standards met or proportionate to the rigor tier. All mode-specific requirements are complete.

**Fund with conditions:** The entry specification gate passes. One or more of the following apply: (a) rigor-tier requirements are partially met, with specific named gaps addressable before disbursement; (b) a Tier 2 conflict of interest relationship requires a waiver decision; (c) a specific indicator field is absent but can be supplied; (d) concurrent funding was disclosed but the scope relationship requires clarification; (e) the disbursement structure should be conditioned on milestone delivery or phased disbursement; (f) the organizational identity declaration or sufficiency architecture declaration has a curable gap. Conditions must be specific: not "improve the indicator set" but "supply a named, independently accessible source for Indicator 1 Field 8 before disbursement, verified by [named method]."

**Do not fund:** The entry specification gate fails. Or: a categorical Tier 1 conflict of interest bar is present and cannot be waived. Or: concurrent funding was not disclosed. Or: the organizational identity declaration reveals non-disclosure of a publicly documentable affiliation. Or: the prior work attribution statement reveals the application's track record is built on work performed under a different entity without that entity's endorsement. Or: an adverse signal was suppressed and the suppression is material to the funding decision. Or: the gate passes but no dimension-level requirements are met and the gaps are not addressable through conditions.

**Reasoning structure:** Always accompany the recommendation with structured reasoning.

1. Obligation mode: [build / change / retroactive]
2. Gate finding: [mode-specific gate finding from the canonical vocabulary]
3. Organizational identity declaration finding: [complete and conformant / incomplete: specify missing field / non-conformant: specify violation]
4. Sufficiency architecture declaration finding: [complete and conformant / incomplete: specify missing element]
5. Prior work attribution finding (if prior work cited): [complete / incomplete: specify gap / adverse signal surfaced: describe]
6. Active dimensions: [each active dimension and its finding]
7. Conflict of interest findings: [any classifications and tiers]
8. Data quality finding: [per standard, if indicators were assessed]
9. Recommendation: [Fund / Fund with conditions / Do not fund]
10. If Fund with conditions: named conditions with specific fields and verification methods.

---

## Part XVI: Funder Obligation Compliance Check

Run when evaluating whether a funder has met its CROSS obligations.

### Publication Requirements

Before any round opens, the funder must have published:

- A plain-language applicant-facing summary of the round's requirements, accessible for the full duration of the round.
- The full application question list, publicly accessible without creating an account, starting a submission, or contacting the funder. Must show every question in order, with the response form type and criterion intent for each question.
- The gate configuration for each active gate: evidence scope, evidence strength, causality stance, infrastructure declaration.
- The conflict of interest receiving authority.
- The appeals procedure (what decisions are appealable, the grounds, the time window, and the appeals body).

### Record Maintenance Requirements

The funder must maintain a record of gate configurations, infrastructure declarations, and documented waivers for each round and stage. Gate criteria must be applied consistently with the published configuration. Any deviation must be documented with justification and the authority under which it was made.

### Structured Dataset Publication

At the close of each round, the funder must publish a machine-readable structured dataset containing, for each funded grant: the indicator specification (all fields from Part VII), the obligation mode, the gate configuration applied, the evidence scope and strength at each gate, the causality stance declared, the sufficiency position declared, the sustainability stance at continuation where applicable, and the unintended outcomes disclosed at completion. The dataset must be published in a format that can be ingested by a data analysis pipeline without manual transformation, with field-level schema documentation.

### Redress Mechanisms

An internal clarification mechanism must provide: a named point of contact, a requirement for written response explaining how the decision was consistent with the published gate configuration, and a time-bound response shorter than the round's typical cycle time.

A structured appeals procedure must specify: what decisions are appealable, the grounds for appeal, the time window for filing, a structurally separate appeals body, and a commitment to written determination on each appeal stating whether a funder obligation violation occurred, whether the original decision stands, and what remediation will be offered.

An independent redress mechanism is optional for CROSS conformance. Where a program operates without one, this must be stated explicitly in the published round configuration.

### Violation Classifications

**Funder obligation violation:** Failure to publish the plain-language summary or question list before the round opens. Applying gate criteria inconsistently with the published configuration. Failure to provide written responses through the internal clarification mechanism. These do not automatically invalidate individual awards but create an obligation to remediate where affected applicants or grantees are identified.

**Gate criterion specification failure:** A gate criterion that does not meet WALKRI criterion specification requirements before the round opens. A gate criterion referencing an external standard without a compliance threshold.

---

## Part XVII: Privacy-Sensitive Accommodation

The privacy-sensitive accommodation applies when standard outcome measurement would compromise the safety of the beneficiary population. It is not a general privacy preference. It does not exempt the applicant from obligation.

### Qualification Criteria

**Qualifies:** The beneficiary population faces documented risk from standard data collection methods: populations under state surveillance, populations where participation data could be used for criminalization, populations in active conflict zones where identity disclosure creates physical safety risks.

**Does not qualify:** General organizational preference for privacy. Absence of analytics infrastructure. Discomfort with standard measurement.

### What the Accommodation Requires

When the accommodation applies, two fields are mandatory (clustering rule trigger from Part VII):

1. **Specific harm:** A named, specific harm that standard measurement would create for this population. Not "privacy risk" in general; the specific mechanism (for example: "collection of user location data would create a database that could be subpoenaed under [named legal regime] and used to identify participants in [specific activity]").

2. **Alternative methodology:** A specific alternative measurement approach that provides obligation direction without creating the named harm. Must name an institutional partner or established methodology (for example: Open Observatory of Network Interference-style network measurement, ethics-reviewed study under institutional review board protocols, differential privacy techniques applied to aggregate reporting).

The accommodation substitutes one obligation mechanism for another. It does not reduce obligation. An applicant who invokes it without supplying both mandatory fields has claimed an exemption that does not exist in CROSS.

### Procedure

1. Verify that the qualification criteria are met. If not, standard measurement requirements apply.
2. If qualified, require both mandatory fields before proceeding to indicator assessment.
3. Assess the alternative methodology against the five data quality standards in Part IX. The standards apply to the alternative methodology, not to a lower threshold.

---

## Canonical Finding Vocabulary

Use these terms consistently. Do not invent alternatives.

**Entry specification gate findings:**

Build obligation: Entry specification gate passes / Entry specification gate fails: direction specification without deliverable / Entry specification gate fails: underspecified completion criteria

Change obligation: Specific pass / Specific with minor gap / D1 failure / D2 failure / Insufficient information

Retroactive obligation: Entry specification gate passes / Entry specification gate fails: contribution description absent / Entry specification gate fails: independent evidence absent / Entry specification gate fails: prior award disclosure absent

**Pre-condition findings (organizational identity and sufficiency architecture):** Complete and conformant / Incomplete: [named missing field or element] / Non-conformant: [named violation]

**Prior work attribution findings:** Complete / Incomplete: [named gap] / Adverse signal surfaced: [description]

**Rigor tier (change obligation post-gate):** Tier 1 / Tier 2 / Tier 3

**Dimension findings:** Active, conformant / Active, non-conformant / Active, conditionally conformant (with named conditions) / Not triggered

**Conflict of interest classifications:** Tier 1 bar / Tier 2 disclosure required / Tier 2 waiver required / Tier 3 disclosure encouraged / No conflict of interest finding

**Data quality findings (per standard):** Passes / Fails / Insufficient information to assess

**Gate evidence findings:** Verified / Failed / Conditionally verified pending [named item]

**Causality stance findings:** Attribution stance, counterfactual requirements present / Attribution stance, counterfactual requirements absent / Contribution stance, contribution analysis present / Contribution stance, contribution analysis absent / Causality stance not declared (gate criterion specification failure)

**Recommendation terms:** Fund / Fund with conditions / Do not fund

---

## Relationship to Other Skills

**Frame Language skill:** CROSS is a Frame 2 instrument. The FROM state requirement in change-obligation rounds is a structural application of the Frame Language inheritance principle: naming the actual condition rather than a projected aspiration. D2 failures in the change-obligation gate assessment are the same failure class Frame Language names as "values aspiration without conditions." Use Frame Language terminology when describing failure types in formal evaluation documents.

**Adverse Signal skill:** Dimension 5 of CROSS instantiates the Adverse-Signal Engagement Principle Core Standard. When Dimension 5 is active, the Adverse Signal skill provides the full assessment procedure.

**Information Asymmetry skill:** Dimension 4 of CROSS instantiates the Information Asymmetry Classification Standard omission class. When evaluating whether a non-disclosure constitutes a disqualifier, the Information Asymmetry Classification Standard skill provides the classification structure.

**Regenerative Obligation skill:** Structurally paired with CROSS but independent. Run both skills independently when both apply; do not merge the evaluations.

**Precision-First skill:** The double-negation invariant from the Precision-First Design Standard is the structural rationale for the tiered documentation architecture in CROSS. When a reviewer questions whether a documentation requirement is proportionate, the Precision-First Design Standard skill provides the formal test.

---

## Standing Obligations

Before generating any finding or recommendation:

1. Confirm that both the organizational identity declaration and the sufficiency architecture declaration are present for any entry gate assessment. If either is absent, the submission is incomplete; do not proceed to gate assessment.

2. Confirm the obligation mode from the round specification: build, change, retroactive, or compound. Apply the correct gate procedure from Part III (Section A for build, Section B for change, Section C for retroactive, Section D for compound).

3. Confirm which task is requested and apply the correct procedure in full. Do not abbreviate the procedure because the application appears simple.

4. Use canonical finding vocabulary throughout. Do not introduce synonyms or informal equivalents.

5. Name conditions specifically. "Fund with conditions" without named conditions is not a complete finding.

6. Keep Regenerative Obligation Standard and CROSS evaluations structurally separate. If both apply, run both and report separately.

7. Do not substitute the gate assessment for the rigor tier assessment, or the rigor tier assessment for the gate. They are sequential, not interchangeable.

8. Do not apply change-obligation gate criteria to build-obligation applications, and do not apply build-obligation criteria to compound applications. The Theory of Build is not a failure mode in build-obligation rounds. For compound rounds, the program-level Change assessment and the component-level Build assessments are separate procedures; do not merge them.

9. Apply the causality stance declared in the gate configuration. Do not default to attribution stance when contribution stance is appropriate to the program context.

10. Where prior work is cited as evidence, run the prior work attribution assessment before completing the gate finding. An incomplete attribution statement is an adverse signal requiring resolution before proceeding.

---

## Changelog

| Version | Date | Changes |
|---------|------|---------|
| 0.6.0 | 2026-05-22 | Added compound obligation mode throughout. Part III: added Section D (Compound Obligation Entry Gate) covering program-level Change specification assessment, component-level Build specification assessment, contribution_to_change statement evaluation, and separate evaluation track rule. Runtime Sequence: added operation 25 (compound obligation entry gate assessment). Part X: added CLEAR lifecycle definition (Commit, List, Evaluate, Attest, Register) and canonical round configuration schema reference to Grant Configurator preamble; updated Q2 to include compound mode with component array requirement; updated Q16 to reference CROSS-canonical-round-configuration-schema-0_1_0.md as the canonical format for Commit stage output. Standing Obligations: updated obligation 2 to include compound mode; updated obligation 8 to include compound-specific non-merger rule. Frontmatter: added CROSS-canonical-round-configuration-schema-0_1_0.md to related_documents. |
| 0.5.0 | 2026-05-19 | Major update to encode CROSS v0.4.7. Runtime Sequence: added operations 21-24 covering novel runbook selection (Runbooks 7-13 from CROSS-runbooks-0_2_0.md), portfolio benchmark compliance assessment, beneficiary accountability mechanism assessment, and primitive classification for new frameworks. Part X Q0: expanded to include all thirteen runbooks across both runbook documents, plus program type bundle reference. Part XIV (Institutional Framework Alignment): major expansion from four frameworks to organized coverage of 95+ frameworks organized by primitive; added sections for US federal education (ESSA/WWC/EIR), US federal workforce and human services (WIOA, SNAP-Ed, Head Start, AmeriCorps, CSBG ROMA), US federal health programs (SAMHSA, HRSA UDS, Ryan White, LIHEAP), environmental and carbon finance (IUCN NbS, Verra VCS, REDD+, Gold Standard), Islamic and endowment-based giving (AAOIFI), European philanthropy (ESIF, EVPA, PHINEO IOOI), faith-based development (CRS ProPack, World Vision LEAP, USCCB/CCHD), and new primitives documentation. Version reference updated from 0.3.7 to 0.4.7. |
| 0.4.0 | 2026-05-18 | Major revision to encode CROSS v0.3.5 through v0.3.7. Added Part IVa (Public Benefit Mechanism and Access Condition Declaration Procedure) with four mechanism types, mechanism-evidence scope alignment table, and finding vocabulary. Added Part IVb (Revenue Architecture, Governance Resilience, and Development Stage Procedures) with four revenue architecture types, three governance resilience states, and five development stage classifications with stage-obligation mode and stage-round alignment consistency checks. Added Obligation Fulfillment Record section to Part IV for returning applicants, with three fulfillment states and corroboration note. Added Field 5 (Disbursement Authority Declaration) to Part IV with three disbursement states. Added corroborating evidence requirement to Part V Element 2 (Sufficiency Position) for rounds at independent review evidence strength or above. Added token event disclosure requirement to Part XII Section 1 covering IDOs, TGEs, ICOs, and pending tokenomics. Added IMP Contribution vocabulary to Part XII Section 1 as optional structured additionality framework with three positions and counterfactual requirement. Added operations 21, 22, 23 to Runtime Sequence. Updated Part III First Step preamble to include PBM declaration as third pre-condition. Updated version reference from 0.3.4 to 0.3.7. |
| 0.3.0 | 2026-05-18 | Major revision to encode CROSS v0.3.4. Added Part IV (Organizational Identity Declaration Procedure) and Part V (Sufficiency Architecture Declaration Procedure) as pre-conditions for all entry gate assessments. Added Part VI (Prior Work Attribution Assessment). Added Part XII (Scope Attribution and Outcome Credit), encoding additionality declaration and outcome credit attribution requirements. Added Part XIII (Program-Level ToC Architecture Configuration), encoding the pathway registry, round linkage, and all pathway-level tags. Added Part XIV (Institutional Framework Alignment), encoding OECD DAC, IRIS+, USAID PIRS, and DAOIP-5 mappings including full PIRS field-by-field mapping. Added Part XVI (Funder Obligation Compliance Check), encoding funder publication requirements, record maintenance, structured dataset publication, and redress mechanisms. Expanded Part VIII (Conflict of Interest) to include organizational role conflict, funder-side consulting conflicts with tiered treatment, and attestation integrity provision for both Tier 1 and Tier 2 conflicts. Expanded Part XI (Gate Evidence Assessment) with developmental vs. summative gate function distinction, pre-award indicator confirmation, counterfactual verification procedure, attribution vs. contribution stance distinction, continuation gate procedure, and unintended outcomes disclosure requirement. Added sustainability and transition plan optional field to Part VII. Added on-chain execution and verification instruments sub-specification to Part VII. Added causality stance finding vocabulary to canonical vocabulary. Updated Runtime Sequence to list all 20 operations. Updated Part XV (Recommendation Generation) reasoning structure to include organizational identity, sufficiency architecture, and prior work attribution findings. Updated Standing Obligations to include new pre-conditions. |
| 0.2.0 | 2026-05-14 | Major revision. Added three accountability modes (build, change, retroactive) with mode-specific entry specification gate procedures in Part III. Renamed "Theory of Build Gate" to "Entry Specification Gate." Updated Field 3 from constrained four-option data type list to open measurement form with three-axis classification (source type, measurement form, aggregation type). Added Part X (Gate Evidence Assessment) covering progress verification and completion verification gate assessments. Updated Grant Configurator question sequence to match Configurator v0.2.0 (Q0 runbook selection, Q2 accountability mode, Q5 program-level continuation gate, Q11 gate configuration). Updated recommendation logic for mode awareness. Added retroactive-specific canonical finding vocabulary. Removed "transclusion" language from Part I. Updated related documents to v0.2.0. |
| 0.1.0 | 2026-05-14 | Initial skill encoding. Single change-accountability mode. Theory of Build gate with five-classification FROM state vocabulary. 11 indicator fields. Five data quality standards. Conflict of interest three-tier classification. Grant Configurator 11-question sequence. Three-term recommendation vocabulary. Privacy-sensitive accommodation procedure. |
