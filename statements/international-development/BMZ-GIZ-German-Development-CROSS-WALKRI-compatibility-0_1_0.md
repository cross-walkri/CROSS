---
title: German Bilateral Development Cooperation (BMZ/GIZ) Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.2 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - https://www.bmz.de/resource/blob/240112/evaluierungskriterien-en.pdf
  - https://www.giz.de/en/downloads/giz-2023-en-gizs-evaluation-system-basic-aspects.pdf
---

# German Bilateral Development Cooperation (BMZ/GIZ) Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

Germany's BMZ (Federal Ministry for Economic Cooperation and Development) publishes evaluation criteria for German bilateral development cooperation that apply five OECD DAC criteria plus a sixth, coherence, defined as the interaction of the measure with other donors, partner organizations, and international policy frameworks. GIZ (the German development agency) publishes its own evaluation system applying BMZ criteria alongside DeGEval (German Evaluation Society) standards, with a notable knock-out rule: a project scoring 4-6 on GIZ's six-point scale in any of three criteria is automatically rated unsuccessful regardless of other scores. CROSS satisfies BMZ's sixth criterion through a named structural provision. CROSS's gate architecture produces independently assessable criterion determinations that satisfy the GIZ knock-out rule. WALKRI satisfies the DeGEval Accuracy standards that GIZ applies to evaluation evidence.

BMZ and GIZ are among Germany's most significant institutional actors in international development. Organizations receiving German bilateral funding, or seeking GIZ partnership, are expected to meet these evaluation standards at the organizational and program level. CROSS+WALKRI compatibility means that conformant programs are producing the documentation these standards require as a consequence of standard gate operations, not as additional reporting work.

---

## BMZ Evaluation Criteria

BMZ's evaluation criteria apply five OECD DAC criteria (relevance, coherence, effectiveness, efficiency, sustainability) and extend them with a sixth criterion, coherence, redefined in the German bilateral context as the interaction of a given measure with other donors, partner organizations, and international policy frameworks. BMZ's coherence criterion is more operationally specific than the OECD DAC definition: it requires a reasoned assessment of how the program relates to what other actors are doing in the same problem area, including whether the program complements, duplicates, or substitutes for other interventions.

CROSS satisfies the five OECD DAC criteria as structural consequences of conformance, documented in the OECD DAC compatibility statement. This statement addresses the BMZ sixth criterion and the GIZ-specific provisions that go beyond the DAC baseline.

### BMZ Sixth Criterion: Coherence

CROSS's coherence disclosure requirement is the named structural provision satisfying BMZ's sixth criterion. The coherence disclosure, required at the entry specification gate, asks programs to declare how their intervention relates to other known interventions in the same problem area. This declaration must address: which other actors are operating in the same space, what their approaches and scales are, whether the program complements or competes with those approaches, and what substitution or duplication risks exist.

This is precisely the evidence the BMZ coherence criterion requires for evaluation. A BMZ evaluator assessing coherence needs to know what the program's designers knew about the broader landscape of interventions when they designed the program, and how that landscape knowledge shaped the program's positioning and targeting decisions. CROSS's coherence disclosure requirement makes this knowledge a specification-layer declaration rather than a retrospective reconstruction. The disclosure is dated and recorded at the entry gate, before implementation begins, making it a contemporaneous record of the coherence analysis rather than a post-hoc narrative.

---

## GIZ Evaluation System

GIZ's "Evaluation System: Basic Aspects" (2023) applies BMZ criteria alongside DeGEval standards and introduces two features that distinguish GIZ evaluation from the broader OECD DAC baseline: the six-point scale and the knock-out rule, and the participatory evaluation process requirement.

### The GIZ Knock-Out Rule

GIZ evaluates projects on a six-point scale across six criteria. A project scoring 4, 5, or 6 (where 1 is highest performance and 6 is lowest) on any of three criteria, effectiveness, overarching development results, or sustainability, is automatically rated unsuccessful regardless of its scores on other criteria. This knock-out rule means that these three criteria must each be documentable at threshold level independently; strong performance on other criteria cannot compensate for failure on any of the three.

CROSS's gate architecture produces separate, independently verifiable determinations at each level that corresponds to a GIZ knock-out criterion.

| GIZ Knock-Out Criterion | CROSS Provision | Assessment |
| :-- | :-- | :-- |
| Effectiveness | Completion gate: deliverable specification vs. actual evidence; independently attested output-level determination | Full satisfaction. CROSS's completion gate produces an independent determination of whether the program achieved its specified outputs. This is the effectiveness evidence layer: outputs are what the program was supposed to produce; the gate determines whether they were produced. The determination is independently attested, not self-reported. |
| Overarching development results | Change obligation target condition at outcome level; causality stance for outcome-level indicators; Attestation Corpus outcome records | Full satisfaction. CROSS's change obligation target condition at the Outcome level of the ToC hierarchy is the structural location of "overarching development results." The gate records evidence of whether the target condition was reached; the causality stance field declares whether the program claims attribution or contribution for that result. A GIZ evaluator can assess this criterion against CROSS gate records without additional data collection. |
| Sustainability | Continuation gate: three-position sustainability stance (sustained, conditional, dependent); evidence requirement for stance justification | Full satisfaction. CROSS's continuation gate is the structural mechanism for the GIZ sustainability criterion. The three-position sustainability stance requires an explicit judgment, backed by evidence, about whether outcomes will persist after funding ends, under what conditions, and with what support requirements. This is the sustainability determination a GIZ evaluator needs, produced at the gate rather than estimated after the fact. |

**Result:** CROSS's gate architecture produces the three independently verifiable criterion determinations that the GIZ knock-out rule requires. Programs using CROSS are not at risk of failing the knock-out rule for want of documentation; each criterion determination is a gate record in the Attestation Corpus, independently attested and retrievable for GIZ evaluation.

### GIZ Participatory Evaluation Requirement

GIZ requires that evaluation processes be participatory: affected populations must be included in the evaluation design, data collection, and sense-making process, not merely observed. This requirement addresses the legitimacy of evaluation findings: an evaluation conducted entirely by external evaluators without engagement with affected communities may produce technically accurate findings that miss the populations' own understanding of what changed and why.

CROSS addresses this requirement at two points in its architecture. The population scope declaration at the program level and indicator level requires that the affected population be defined as a measurable construct, not a residual category. The evidence form requirement in WALKRI, applied to the indicators that capture change in the affected population, requires that the evidence form be independent of the grantee's self-report; one way to satisfy this requirement is through structured data collection directly from affected community members, which is the instrument-design equivalent of participatory evidence collection.

WALKRI's evidence form requirement does not mandate participatory data collection, but it creates a structural incentive for it. If the evidence form for an outcome indicator must be independent of both the grantee's self-report and the grantee's own measurement instruments, community-sourced evidence is often the most straightforward way to satisfy the independence requirement. Programs that design their evidence forms to collect directly from affected populations are implementing the GIZ participatory evaluation requirement at the instrument design level, not merely describing participatory intention.

---

## DeGEval Accuracy Standards

GIZ applies DeGEval (German Evaluation Society) standards alongside BMZ criteria. DeGEval's standards include Usefulness, Feasibility, Fairness, and Accuracy. The Accuracy standards require that evaluation evidence be methodologically sound: valid, reliable, comprehensive, and based on instruments that are appropriate to the measurement task.

WALKRI's five pre-publication field requirements directly implement the DeGEval Accuracy standards at the intake instrument design level. The criterion intent requirement ensures that every field collecting data for a CROSS gate has a stated, documented purpose that aligns with the measurement task. The operational definition requirement ensures that field boundaries are explicit and that different reviewers applying the definition to the same data will reach the same conclusion. The response form justification requirement ensures that the data collection method is appropriate to the measurement goal and that the appropriateness argument is documented. The evidence form requirement ensures that every indicator has an independent verification pathway. The compliance threshold requirement ensures that the standard for what counts as a valid response is stated before data collection begins.

These five requirements are the instrument-design implementation of what DeGEval means by Accuracy. Programs that have passed WALKRI's pre-publication audit are collecting data through instruments whose accuracy properties are documented, testable, and consistent across the measurement cycle. A GIZ evaluator assessing evidence quality can review the WALKRI audit record as documentation of the measurement system's Accuracy properties, rather than having to reconstruct instrument quality from the data itself.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

BMZ Evaluation Criteria: https://www.bmz.de/resource/blob/240112/evaluierungskriterien-en.pdf

GIZ Evaluation System: https://www.giz.de/en/downloads/giz-2023-en-gizs-evaluation-system-basic-aspects.pdf

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. BMZ sixth criterion (coherence) mapped to CROSS coherence disclosure requirement. GIZ knock-out rule mapped to CROSS gate architecture producing independent criterion determinations at effectiveness, overarching development results, and sustainability levels. GIZ participatory evaluation requirement addressed through WALKRI evidence form independence. DeGEval Accuracy standards mapped to WALKRI five field requirements. |
