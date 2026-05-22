---
title: SROI / Social Value International Principles Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - Social Value International, SROI Principles and Standards, socialvalueint.org
  - Social Return on Investment methodology overview, https://www.betterevaluation.org/methods-approaches/approaches/social-return-investment
  - Social Value International, A Guide to Social Return on Investment, 2nd edition
---

# SROI / Social Value International Principles Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

WALKRI's five pre-publication field requirements address Social Return on Investment (SROI) Principles 2, 4, 5, 6, and 7 structurally, at the collection instrument specification layer. CROSS's obligation architecture, particularly the causality stance field and Theory of Change architecture, addresses Principles 3, 5, and 6 at the program design layer. Together, CROSS and WALKRI provide a specification foundation for SROI-aligned programs that is more rigorous than SROI's own methodology requires at the instrument level.

SROI is a methodology and principles framework for accounting for social value; it was developed by Social Value International and is used by development organizations, impact investors, corporate ESG programs, and nonprofit grant programs. CROSS is an obligation architecture specifying what funded interventions must demonstrate. WALKRI is a specification quality layer governing how collection instruments must be designed. The three are complementary at different layers of the measurement stack: SROI establishes what principles a social value account must satisfy; CROSS and WALKRI determine whether the data underlying that account was produced by a sufficiently specified, auditable process.

---

## What SROI Is

The Social Return on Investment methodology is an approach to measuring, accounting for, and communicating the social, environmental, and economic value created by an organization's activities. It was developed from Social Accounting methods and is maintained by Social Value International. SROI analyses are used by nonprofits, government agencies, impact investors, and corporate social responsibility programs to assess whether interventions produce value commensurate with the resources invested.

SROI analyses follow a structured process: identifying stakeholders whose lives the activity affects, mapping what changes for each stakeholder, valuing those changes using financial proxies where appropriate, assessing materiality (which changes matter enough to include), applying a counterfactual (what would have happened without the intervention), and calculating a ratio of social value to investment. The ratio is not the purpose; the principles-based methodology is.

Social Value International articulates seven principles that SROI analyses and social value accounts must satisfy:

1. Involve stakeholders: base reports on information about and from stakeholders.
2. Understand what changes: articulate, through evidence, how change happens and evaluate this against assumptions.
3. Value the things that matter: use financial proxies to give value to outcomes that do not have market prices.
4. Only include what is material: only include information and evidence that stakeholders and decision-makers would consider important.
5. Do not over-claim: only claim the value that activities are responsible for creating.
6. Be transparent: demonstrate the basis on which analysis may be considered accurate and honest.
7. Verify the result: ensure appropriate independent assurance.

---

## WALKRI and SROI Principles

### Principle 2: Understand What Changes

Principle 2 requires that an SROI analysis articulate, through evidence, how change happens. It is not satisfied by naming outcomes; it is satisfied by showing, with evidence, the causal chain from activities to changes for stakeholders.

WALKRI's criterion intent requirement addresses Principle 2 at the instrument design level. Every field in a WALKRI-conformant instrument must state what it is measuring: not the name of the metric, but the underlying change the metric is intended to track. A field named "open source contributions" with a criterion intent of "individual developer capacity to participate in protocol maintenance" specifies what change is being tracked, for whom, and at what level. Without criterion intent, a field name is a label; with it, a field name is a claim about a specific change. This is Principle 2 applied to instrument design.

### Principle 4: Only Include What Is Material

Principle 4 requires that only information material to stakeholders and decision-makers be included in a social value account. The discipline of materiality prevents SROI analyses from including every positive effect an activity has, regardless of whether those effects matter to the people affected or to the decisions the account is meant to inform.

WALKRI's operational definition requirement implements materiality at the field level. An operational definition specifies what counts as a valid instance of the measured phenomenon and what does not: it includes qualifying examples and non-qualifying examples. A field that measures "community governance participation" with an operational definition that includes only verified deliberative participation in formal decision-making processes, and explicitly excludes passive attendance at informational meetings, has made a materiality decision. It has specified which form of participation is material to the change being tracked. Without this specification, every positive interaction can be counted; with it, only the interactions that match the defined criterion are included. This is materiality implemented at the instrument design level, before data collection begins.

### Principle 5: Do Not Over-Claim

Principle 5 requires that social value accounts claim only the value that the organization's activities are responsible for creating. It has two operational dimensions: counterfactual reasoning (what would have happened without the intervention) and scope of attribution (what share of the observed change can be attributed to this specific activity, given other contributing factors).

WALKRI's compliance threshold requirement addresses the over-claiming problem at the measurement level. The compliance threshold specifies when a response is sufficient: it is the minimum standard a measured outcome must meet to count as a valid instance. A compliance threshold that requires a documented, verified change rather than a self-reported intention prevents the inflation of outcome counts that produces over-claiming at the data layer.

CROSS's causality stance field (contribution versus attribution) addresses Principle 5 at the program design level. Programs that declare a contribution stance acknowledge that the observed outcome was produced by multiple factors and that the program contributed to rather than solely caused the change. This declaration, encoded in the obligation record before implementation, bounds the scope of the value claim the program can make in an SROI analysis. It prevents attribution of the full observed change to the program's activity when the causal structure is contributory rather than deterministic.

Together, the compliance threshold (bounding what counts as a valid measurement instance) and the causality stance field (bounding the share of the outcome the program can claim) create a two-layer protection against the over-claiming that Principle 5 prohibits.

### Principle 6: Be Transparent

Principle 6 requires that social value accounts demonstrate the basis on which analysis may be considered accurate and honest. It covers transparency about methods, assumptions, stakeholder involvement, and the limitations of the analysis.

WALKRI's pre-publication audit and conformance record address Principle 6 at the specification layer. A WALKRI-conformant instrument has been through a three-stage review process before any data is collected: criterion intent has been reviewed for clarity and alignment with the measured change, operational definitions have been reviewed for boundary clarity and internal consistency, and evidence forms have been reviewed for independence from beneficiary self-report. The conformance record documents that this review occurred, when, and with what findings.

This is transparency at the instrument design level, before data collection begins. An SROI analysis that references WALKRI conformance records for its collection instruments provides decision-makers with a specification-layer transparency artifact that SROI's own methodology does not require but that Principle 6's intent clearly encompasses.

CROSS's obligation record, as a formally versioned specification of what the program committed to measure and demonstrate, is the program-level transparency artifact. It shows, at the design stage, what the program intended to claim and on what evidentiary basis. An SROI analysis conducted on a CROSS-conformant program can point to the obligation record as the basis for its materiality and scope decisions, which is the program-level expression of Principle 6.

### Principle 7: Verify the Result

Principle 7 requires independent assurance that an SROI analysis is accurate. Social Value International's verification scheme involves external review of the methodology, data, and analysis by a qualified assessor who is independent of the organization producing the account.

WALKRI's evidence form requirement is the instrument-level expression of Principle 7's independence requirement. Every WALKRI-conformant field must specify an evidence form: an artifact that independently verifies the claimed measurement, accessible through a pathway that the reporting entity does not control. A field claiming that 500 developers onboarded to a protocol must specify what artifact demonstrates that onboarding, and the artifact must not be a self-report generated by the entity making the claim.

The independence logic of WALKRI's evidence form requirement and the independence logic of SROI's Principle 7 are structurally identical: both require that verification be accessible to someone other than the party whose performance is being assessed. WALKRI implements this at the instrument design level, building the independence structure into the field specification before data collection begins. This does not replace the independent assurance that Principle 7 requires at the analysis level; it ensures that when an independent assessor reviews the SROI analysis, the underlying measurement records were produced by instruments designed for auditability rather than for self-serving ease of reporting.

---

## CROSS and SROI Principle 3: Value the Things That Matter

SROI's Principle 3 requires that things which matter to stakeholders be given value, using financial proxies where outcomes do not have market prices. This is the monetization principle that distinguishes SROI from other social value frameworks.

CROSS does not govern monetization; it governs obligation architecture and indicator specification. However, CROSS's Theory of Change architecture at the outcome level produces the structured outcome claims that financial proxy valuation requires as input. An SROI analysis can only monetize an outcome that has been specified precisely enough to identify an appropriate financial proxy. CROSS's eleven-field indicator specification, applied at the outcome level of the ToC, produces outcome specifications with defined populations (Field 6, population scope), defined baselines (Field 4 in CROSS v0.4.0 numbering), and defined measurement methodologies. These specifications are the inputs that outcome-level SROI financial proxy valuation requires.

---

## Summary Mapping Table

| SROI Principle | CROSS Provision | WALKRI Provision | Coverage |
| :-- | :-- | :-- | :-- |
| 1. Involve stakeholders | No direct provision; stakeholder identification is an operational process outside specification scope | No direct provision | Outside specification scope |
| 2. Understand what changes | Theory of Change architecture (causal links and assumptions make change theory explicit) | Criterion intent requirement (every field states what change it tracks) | Structural: specification precondition for understanding change |
| 3. Value the things that matter | Eleven-field indicator specification at outcome level provides inputs for financial proxy valuation; no monetization provision | No direct provision | Partial: specification inputs only, not monetization methodology |
| 4. Only include what is material | Obligation mode and ToC scope constrain which outcomes are within program scope | Operational definition requirement (qualifying and non-qualifying examples implement materiality at field level) | Structural: materiality implemented at instrument design level |
| 5. Do not over-claim | Causality stance field (contribution vs attribution) bounds the share of outcome the program can claim | Compliance threshold requirement bounds what counts as a valid measurement instance | Structural: two-layer protection at program design and instrument levels |
| 6. Be transparent | Obligation record as a formally versioned, pre-specified commitment; coherence disclosure requirement | Pre-publication audit and conformance record; three-stage review process | Structural: specification-layer transparency artifacts |
| 7. Verify the result | On-chain identity anchor provides a verifiable program identity for independent assessors; gate evidence record provides a structured evidence base | Evidence form requirement (every field has an independent verification pathway not controlled by the reporting entity) | Structural: independence architecture built into instrument design |

---

## Adoption Guidance

Organizations conducting SROI analyses or producing social value accounts under Social Value International principles that adopt CROSS+WALKRI should:

1. Apply WALKRI's five field requirements to all collection instruments before beginning data collection for the SROI analysis. The criterion intent, operational definition, and compliance threshold requirements implement Principles 2, 4, and 5 at the instrument level; this substantially reduces the methodological review work required during independent verification.

2. Use CROSS's causality stance field to declare the contribution or attribution stance before implementation. This bounds the scope of the social value claim and makes the Principle 5 counterfactual position explicit in a formally versioned, pre-specified record rather than in a post-hoc analytical memo.

3. Reference the WALKRI conformance record for each collection instrument in the SROI analysis's transparency appendix. This satisfies Principle 6 at the specification layer and gives independent assessors a structured audit trail for the instruments that produced the analysis's underlying data.

4. Use CROSS's ToC outcome level specifications as the input to outcome-level financial proxy selection for Principle 3 monetization. The eleven-field indicator specification provides the population scope, baseline, and methodology specificity that financial proxy valuation requires to be defensible.

5. For programs subject to Social Value International verification, present the WALKRI evidence form specifications to the independent assessor alongside the SROI analysis. The evidence form requirement implements the independence structure that Principle 7 requires; assessors reviewing evidence form specifications can assess instrument-level independence without reconstructing the collection design from scratch.

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

Social Value International: socialvalueint.org

SROI methodology overview: https://www.betterevaluation.org/methods-approaches/approaches/social-return-investment

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. WALKRI analysis for Principles 2, 4, 5, 6, and 7. CROSS analysis for Principles 3, 5, and 6. Principle 1 and Principle 3 monetization scope boundaries established. Full seven-principle mapping table. Adoption guidance. |
