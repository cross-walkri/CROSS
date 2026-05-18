# CROSS: Common Reporting Outcome Standards Schema

Version 0.3.8 | 2026-05-18 | CC0

**Two standards. One problem.**

Most grant programs never write down what grantees must prove to get paid. They have eligibility criteria. They do not have an obligation architecture. Reviewers fill the gap with their own judgment. The data this produces looks structured, but it is not.

CROSS fixes that. It specifies what must be demonstrated at each payment gate, declared before any applicant sees the form, in one of three obligation modes: build something specific, produce a measurable change in the world, or recognize work already done. Every grants program answers these questions implicitly every round. CROSS makes the answers explicit, documented, and auditable.

**CROSS is the first standard that has ever required this decision to be written down before the round opens.**

![GIGO pipeline: obligation never specified and questions not designed to measure enter a funnel, producing data that cannot be compared, aggregated, or trusted. No existing tool touches the source.](assets/cross-walkri-gigo-problem.png)

---

## Two failure modes. One fix.

Comparative examination of grant programs across web3, open source, and institutional contexts surfaces a consistent pattern. The failure locates itself differently depending on the type of program.

In web3 grant programs, the hard part is consistently upstream: at the point of claim specification. Applicants default to aspiration language, naming what they are trying to achieve rather than conditions that can be independently measured. Without a specific measurable baseline there is no measurement instrument, no FROM state, no outcome. Funding decisions are made on the basis of who sounds most plausible, not who has specified what they will actually produce.

In governmental and institutional programs, the hard part tends to locate itself downstream: at reporting and verification. Applications are detailed. Reports arrive on schedule. But the reports describe activity, not outcomes. Grantees learn to write good reports rather than produce measurable results. The evidentiary chain between award and impact exists on paper but not in practice.

CROSS was designed to be portable across both failure modes. It separates the evidentiary structure from the program design and makes both configurable. Programs configure where the evidentiary pressure falls. The gate architecture installs it at the front for programs where baseline specificity is the failure mode, and at the back for programs where outcome verification is the failure mode.

---

## What CROSS specifies

![Three obligation modes: Build, Change, and Retroactive, each shown as a distinct accountability structure with its gate test.](assets/cross-obligation-modes.png)

**Three obligation modes** correspond to three fundamentally different accountability structures.

Build obligation applies where the deliverable is a specific artifact. Gate tests confirm whether the delivered thing matches what was specified. This is the right mode for software tools, research reports, infrastructure deployments, and any work where completion has a clear binary test.

Change obligation applies where the goal is a measurable shift in an external condition. The entry specification gate requires a baseline value, a target in the same units, a defined population, a named data source, and a stated mechanism connecting the intervention to the anticipated shift. This prevents aspiration language from entering the record because a grantee cannot name a FROM state without having diagnosed the problem before designing the solution.

Retroactive obligation applies where work is already done. Gate tests confirm whether the documented impact is credibly attributed to the prior activity. This is the right mode for retrospective public goods funding, recognition of past contributions, and programs where the work precedes the funding decision.

**A four-gate sequence** governs each funding release: entry specification before any funds move, one or more milestone gates during delivery, a completion gate at close, and an optional continuation gate determining whether a grantee enters subsequent rounds. Programs configure which gates apply and at what rigor tier, and publish that configuration before any application opens.

**Eight independent obligation dimensions** can be configured independently within a single round: outcome specificity, evidence quality tier, attribution claim strength, financial transparency scope, organizational disclosure depth, institutional framework alignment, portfolio position declaration, and causality stance. The dimensions do not collapse into a single score because the failure modes they address are structurally distinct.

**Organizational identity** requires five declared fields: legal or registered name, primary operating jurisdiction, primary contact, governance structure type, and organizational history. Version 0.3.8 adds Field 6: an on-chain identity anchor, recording the grantee's verifiable on-chain identifier and linking the declaration to on-chain activity records without requiring that linkage as a condition of participation.

**Two funder-side procedures** were formalized at v0.3.8. The Attestation Corpus query retrieves all prior CROSS declarations associated with a grantee's identity anchor before a funding decision is made; it gives the declaration surface its accountability teeth. The Cohort Position assessment places each applicant's funding request in the context of the full applicant pool, including what each applicant has already received, from which sources, against which declared obligations, and whether the requested amount is sufficient, redundant, or misaligned given that history.

**Theory of Change architecture** in CROSS is not a narrative. It is a structured registry of causal claims at four levels (goal, outcome, output, activity) with named assumptions, stated evidence sources, and declared confidence tiers for each causal link. The architecture follows the Compact Logic hierarchy used by MCC and USAID, making CROSS ToC declarations natively compatible with those frameworks without requiring separate documentation.

---

## Compatibility is the point

![CROSS+WALKRI stack: any form builder or grants platform below, CROSS+WALKRI in the middle providing obligation architecture and field quality, Web3 and institutional standards above. One conformant round, both directions, no extra work.](assets/cross-walkri-compatibility-stack.png)

CROSS sits in the middle of the grants stack, not at the top or bottom. Form builders and grants platforms sit below it and implement it. Programs, institutional reporting, and portfolio intelligence sit above it and build on it.

Below: any form builder producing JSON Schema, which every major form tool already does, is already CROSS-compatible at the field level. Programs do not change their stack. They specify their obligation architecture correctly before publishing the form.

Above: a CROSS-conformant round exports in two directions simultaneously. To the Web3 ecosystem: DAOIP-5 GrantPool objects, W3C Verifiable Credential-compatible gate attestations, and OpenGrants Gateway API interoperability. To the institutional side: OECD DAC evaluation criteria, IRIS+ metadata requirements, and USAID PIRS compliance, all as structural consequences of a correctly configured round, not as separate reporting obligations.

One conformant round. Both directions. No extra work.

Compatibility statements are formally published rather than asserted. CROSS currently holds confirmed compatibility with OECD DAC evaluation criteria, IRIS+ metadata requirements, USAID PIRS, and DAOIP-5. The USAID PIRS statement confirms that CROSS's eleven-field indicator specification satisfies all nine required PIRS elements. A program reporting to USAID that implements CROSS does not need to produce separate PIRS documentation: the CROSS specification produces it as a structural output.

---

## Who this is built for

![Cascade pyramid: Grantees and Reviewers at the base, Operators and Platform Providers, Analysts and Institutional Funders, Strategic Planners at the apex. Smaller decisions with immediate feedback at the base; larger decisions with billions at stake at the top. Strategic level value requires ecosystem-wide adoption to materialise.](assets/cross-walkri-value-cascade.png)

Fixing GIGO at the source produces value that compounds with every layer up the grants ecosystem. Grantees encounter questions that specify what they must prove. Reviewers assess against criteria written before they arrived. Operators run rounds that produce comparable data automatically. Analysts consume structured, aggregated data instead of manually reconciling incommensurable reports. Institutional co-funders receive compliance output as a byproduct of the round being run correctly. Strategic planners, deciding how to allocate billions across sectors and geographies, are currently making those decisions on GIGO. CROSS+WALKRI data, accumulated across programs and rounds at scale, is what eventually gives them something real to work with.

The strategic planning benefit materialises as adoption accumulates. The foundation is correct. The compounding takes time and scale.

---

## What conformant rounds produce

The value CROSS creates is specific to each layer of the grants ecosystem.

**Program operators** gain a published, auditable obligation architecture before any application is submitted. The rubric is not constructed post-hoc to justify decisions already made. It is declared in the round specification, tested against at each gate, and exportable as a DAOIP-5 GrantPool object. Operators can configure exactly where evidentiary pressure falls: at the entry specification gate for programs where baseline specificity is the failure mode, or at the completion and continuation gates for programs where outcome verification is the challenge.

**Reviewers** assess against criteria that existed before anyone applied. The entry specification gate means aspiration language cannot pass a structural test regardless of how compellingly it is written. A reviewer can confirm whether a claimed FROM state specifies a measurable condition in a defined population with a named data source, or flag it as a D2 failure, without exercising subjective judgment. The rubric does the structural work.

**Grantees** know before applying what they must demonstrate at each payment gate. In Change mode, they know they must produce a baseline measurement, a target, a population, and a data source, before writing anything else. In Build mode, they know the deliverable specification is what gets tested, not the aspiration behind it. This protects grantees from vague obligations as much as it protects funders from vague commitments.

**Analysts** gain structurally comparable obligation declarations across programs and epochs. A portfolio of CROSS-conformant rounds can answer questions that currently require months of manual reconstruction: how many programs have Change-mode obligations versus Build-mode? What proportion passed milestone gates at the highest rigor tier? How does the portfolio's attribution stance distribution compare across rounds? These questions cannot be answered at all from incommensurable round records. They answer themselves from CROSS-conformant data.

**Institutional co-funders** receive OECD DAC, USAID PIRS, and IRIS+ compliance as structural outputs of the round being configured correctly. A development agency co-funding a program running CROSS does not need to impose separate reporting requirements or conduct a separate data quality assessment. The Attestation Corpus query and Cohort Position assessment also give institutional funders cross-program grantee history that previously required expensive independent research.

**Platform providers** gain structural comparability across every program running on the platform from a single conformance requirement. Multi-program portfolio analysis, cross-round grantee tracking, and institutional reporting outputs are available without custom integration between programs.

---

## License

CROSS is dedicated to the public domain under **Creative Commons Zero v1.0 Universal (CC0)**. See `LICENSE` for the full dedication.

CROSS is an independently published standard. It is co-released alongside the Coordination Structural Integrity Suite but is not a Suite document and does not carry the Suite's CC BY 4.0 license. Any grants ecosystem can adopt CROSS without adopting the Suite.

---

## What is in this repository

**Main standard**

`CROSS-common-reporting-outcome-standards-schema-0_3_8.md` is the canonical specification. Read this first.

**Companion documents**

`CROSS-runbooks-0_1_0.md` contains six pre-built gate configuration packages for common program types: Discovery Sprint, Staged Development, Community Allocation with Build Obligation, Retroactive Impact, Graduated Evidence, and Institutional Conformance. Each runbook selects an accountability mode, configures gate evidence requirements, and includes a recommended rubric emphasis section. Funders new to CROSS should start with the runbook that best matches their program type.

`CROSS-common-reporting-outcome-standards-schema-guidance-0_3_8.md` contains field-by-field guidance for applicants completing an entry specification under any accountability mode. It covers the three-mode entry specification architecture, the gate framework, field interpretation, and the distinction between D1 (sourcing) and D2 (specification) failures.

`CROSS-common-reporting-outcome-standards-schema-rubric-0_3_8.md` contains the funder-facing assessment rubric, organized by accountability mode. The confirmed rubric block is published before the round opens and loaded by reviewers without modification.

`CROSS-common-reporting-outcome-standards-schema-templates-0_3_8.md` contains submission templates for each accountability mode and gate type, including the gate evidence submission template.

`CROSS-common-reporting-outcome-standards-schema-worked-examples-0_3_8.md` contains six cases demonstrating how the entry specification gate and rigor tier apply across different application types, including boundary cases.

**Skills**

`skills/claude-skill-CROSS-0_3_8.md` is the Claude skill for applying CROSS in an extended AI-assisted session. It encodes the three accountability modes, gate architecture, indicator specification fields, and the full assessment rubric in a format optimized for AI-assisted grant evaluation and program design.

---

## Ecosystem position

Every major tool in the grants stack was examined before CROSS was designed. The table below shows where each sits and what it covers. The pattern is consistent: existing tools manage, format, or document data produced by a grants process. None specify the obligation architecture or field quality that determines whether the data is trustworthy before the process begins.

| Tool / Standard | Layer | Obligation architecture | Field quality | Web3 output | Institutional output |
|:--|:--|:--|:--|:--|:--|
| **CROSS** | Specification | Three modes, four-gate sequence | n/a (see WALKRI) | DAOIP-5, W3C VCs, OpenGrants | OECD DAC, IRIS+, USAID PIRS |
| **WALKRI** | Specification | n/a (see CROSS) | Five pre-publication field requirements | n/a | USAID data quality criteria |
| [Logframe / LFA](https://www.oecd.org/en/topics/sub-issues/development-co-operation-evaluation-and-effectiveness/evaluation-criteria.html) | Methodology | ToC hierarchy; no gate architecture or obligation modes | n/a | n/a | OECD DAC evaluation criteria |
| [IRIS+](https://iris.thegiin.org/standards/) | Vocabulary | n/a | n/a | n/a | Indicator reference library |
| [DAOIP-5](https://github.com/metagov/daostar/blob/main/DAOIPs/daoip-5.md) | Interoperability | n/a | n/a | Grants data portability | n/a |
| [KarmaGAP](https://docs.gap.karmahq.xyz/) | Post-funding tracking | n/a | n/a | EAS milestone attestations | n/a |
| [EAS](https://docs.attest.org/) | Attestation layer | n/a | n/a | Permissionless schema registry | n/a |
| [Gitcoin Grants Stack](https://github.com/gitcoinco/grants-stack) | Platform | n/a | n/a | DAOIP-5 only | n/a |
| [Hypercerts](https://docs.hypercerts.org) | Post-work | n/a | n/a | Impact certificates | n/a |

---

## Relationship to Logframe / LFA

The Logical Framework Approach (Logframe) is the dominant evaluation methodology in development finance and the UN system. CROSS's Theory of Change architecture is compatible with Logframe and extends it in four specific ways.

**Where they align.** The Logframe hierarchy (Activities, Outputs, Purpose/Outcome, Goal/Impact) maps directly to CROSS's Compact Logic hierarchy (Activity, Output, Outcome, Goal), inverted in presentation direction but identical in causal structure. CROSS's causality stance field (contribution vs attribution) corresponds to the Logframe assumptions column, which specifies external conditions that must hold for causal logic between levels to function. Both operate within the OECD DAC evaluation criteria framework (Relevance, Coherence, Effectiveness, Efficiency, Impact, Sustainability).

**Where CROSS extends Logframe.** The Logframe performs one causal assessment at end-of-project. CROSS specifies four named gates with published evidence requirements before any applicant submits: entry specification gate (baseline and target required before funding), progress verification gates during delivery, completion gate at close, and continuation gate determining whether a grantee enters subsequent rounds. Each gate has configurable evidence scope and strength, declared in the round specification. The Logframe does not specify obligation modes before a round opens, does not distinguish build obligation (artifact delivery) from change obligation (measurable shift) from retroactive obligation (prior work), and does not specify what makes an intake field a measurement instrument. WALKRI addresses that third gap; CROSS addresses the first two.

A CROSS+WALKRI-conformant round satisfies OECD DAC evaluation criteria as a structural consequence of conformance. The formal compatibility statement is in `statements/USAID-PIRS-CROSS-WALKRI-compatibility-0_1_0.md`.

---

## Compatibility references

The compatibility claims in this README are formally published as compatibility statements in the `statements/` directory of the CROSS+WALKRI repository. Specific external documentation:

- [DAOIP-5 GrantPool specification](https://github.com/metagov/daostar/blob/main/DAOIPs/daoip-5.md)
- [W3C Verifiable Credentials Data Model v2.0](https://www.w3.org/TR/vc-data-model-2.0/)
- [OECD DAC Evaluation Criteria](https://www.oecd.org/en/topics/sub-issues/development-co-operation-evaluation-and-effectiveness/evaluation-criteria.html)
- [IRIS+ Standards](https://iris.thegiin.org/standards/)
- [USAID PIRS requirements](https://2017-2020.usaid.gov/sites/default/files/documents/1861/Recommended_PIRS_for_USAID_indicators_0.pdf)

**CROSS indicator specification vs USAID PIRS nine required elements:**

USAID requires nine documented elements per indicator in a Performance Indicator Reference Sheet. CROSS's eleven-field indicator specification satisfies all nine as a structural consequence of conformance.

| USAID PIRS element | CROSS field(s) |
|:--|:--|
| Indicator name | Field 1: Indicator name |
| Definition and unit of measure | Field 2: Definition / Field 3: Unit of measure |
| Disaggregation | Field 6: Population scope |
| Rationale and linkages | Field 11: Causality stance |
| Data acquisition (source, method, frequency) | Field 7: Data source / Field 8: Collection frequency |
| Data quality assessment | WALKRI five field requirements (applied at specification stage) |
| Responsible party | Field 9: Responsible party |
| Baseline value | Field 4: Baseline value |
| Targets | Field 5: Target value |

A program reporting to USAID that implements CROSS does not produce PIRS documentation separately. The CROSS round specification produces it as a structural output.

---

## Relationship to the Coordination Structural Integrity Suite

CROSS inherits requirements from four Suite standards by reference:

- Adverse Signal Engagement Principle Core Standard: disclosure requirements for adverse signals
- Information Asymmetry Classification Standard: omission asymmetry requirements for concurrent funding disclosure
- Precision-First Design Standard: indicator sourcing requirements and the double-negation invariant
- Regenerative Obligation Standard: direction of accountability (what the Suite addresses) as the structural complement to CROSS's destination (what CROSS addresses)

Adoption of CROSS does not require adoption of the Suite. The inherited requirements are fully stated within CROSS.

---

## Version history

| Version | Date | Summary |
|---------|------|---------|
| 0.3.8 | 2026-05-18 | Five organizational identity fields plus on-chain identity anchor (Field 6), Attestation Corpus query procedure, Cohort Position assessment procedure, eight independent obligation dimensions, Theory of Change architecture (Part IX-B), institutional framework compatibility statements (OECD DAC, IRIS+, USAID PIRS, DAOIP-5). |
| 0.2.0 | 2026-05-14 | Three accountability modes, four-gate architecture, program-level continuation gate, open measurement form replacing constrained data type list, runbooks, full companion document suite. |
| 0.1.0 | 2026-05-14 | Initial release. Change accountability mode, Level 1 and Level 2 gate structure. |
