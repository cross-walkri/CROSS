---
title: Australian DFAT Performance Assessment Framework Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.2 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - https://www.dfat.gov.au/sites/default/files/dfat-aid-evaluation-policy-nov-2016.pdf
  - https://www.dfat.gov.au/sites/default/files/performance-delivery-framework.pdf
---

# Australian DFAT Performance Assessment Framework

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

Australia's Department of Foreign Affairs and Trade (DFAT) applies a three-tier Performance Assessment Framework (PAF) across bilateral and regional programs, with each tier requiring indicator documentation and explicit attributability rules distinguishing directly attributable results from contribution. A climate mainstreaming threshold introduced from 2024-25, rising from 50% to 80% of new bilateral and regional investments, adds a portfolio-level tagging obligation. CROSS gate architecture maps to all three PAF tiers as a layered obligation system, while the CROSS causality stance field satisfies DFAT's attributability distinction requirement. WALKRI supports DFAT's consistent, comparable climate objective data requirement at the measurement instrument level.

---

## The DFAT Framework's Approach

Australia's DFAT Aid Evaluation Policy (2016) and International Development Performance and Delivery Framework (current) together establish a performance management architecture that operates simultaneously at three distinct levels of granularity. This three-tier structure is one of the more formally explicit portfolio management systems among bilateral donors, and it creates compliance obligations that extend beyond individual project documentation into country-program and portfolio-level evidence aggregation.

At tier 3, individual projects must document project-level results against specified indicators. This is familiar territory for grant management: indicator definitions, baselines, targets, collection methods, and periodic reporting against those targets. Most bilateral aid systems operate at this level as their primary performance management requirement.

Tier 2 extends the obligation to country or regional program results. Programs contributing to a bilateral or regional portfolio must document how their project-level results roll up into country or regional program outcomes. This requires that project-level indicators be designed with aggregation compatibility in mind: results documented at tier 3 must be expressible in terms that compose meaningfully into tier 2 statements.

Tier 1 operates at the full portfolio level, requiring aggregate indicators that describe what DFAT's entire development program is achieving across geographies and sectors. This means that results documented at project level must, in principle, be traceable through two levels of aggregation to portfolio reporting. The practical implication for individual grantees is that idiosyncratic indicator designs that work at the project level but cannot be aggregated are systematically incompatible with DFAT's framework, even if they produce valid local evidence.

A second distinctive feature of DFAT's framework is the explicit attributability rule requirement. Programs must specify, at the indicator level, whether a given result is directly attributable to the funded intervention or represents a contribution claim in the presence of other causal factors. This distinction is not left to evaluator judgment at the end of a program cycle; it must be declared in advance as part of indicator documentation. The practical effect is that programs claiming direct attribution must be able to defend that claim against a counterfactual standard, while programs claiming contribution must be able to document their theory of how their intervention contributed within a multi-causal environment.

From 2024-25, DFAT added a climate mainstreaming threshold to its bilateral and regional investment requirements. At least 50% of new bilateral and regional investments above 3 million AUD must have a climate change objective, rising to 80% by 2028-29. This threshold applies at the portfolio level, but satisfying it requires that individual program documentation include climate objective tagging in a form that DFAT can aggregate across investments to assess portfolio-level compliance.

---

## How CROSS Satisfies the DFAT Framework

The three-tier PAF maps directly onto CROSS's layered obligation architecture. CROSS does not operate only at the individual project level; its gate documentation, Cohort Position assessment, and Attestation Corpus together constitute a three-level documentation system.

**Tier 3 (project level).** CROSS gate documentation, including the entry specification gate's eleven-field indicator specifications and subsequent progress, completion, and continuation gate records, constitutes project-level performance documentation. The entry gate's indicator specifications include the elements DFAT requires at tier 3: indicator definitions, units, collection methods, baselines, targets, and reporting frequency.

**Tier 2 (country or regional program level).** CROSS's Cohort Position assessment, conducted across applicants in a given funding round, enables comparison and aggregation of results across programs in a portfolio. Cohort Position documentation provides the tier 2 composition layer: project-level results are assessed relative to the distribution of results across comparable programs, enabling country or regional program-level synthesis statements.

**Tier 1 (portfolio level).** The CROSS Attestation Corpus, accumulating gate documentation across multiple rounds and programs, provides the longitudinal portfolio-level evidence base that tier 1 requires. Corpus records are structured consistently across programs by design, enabling the aggregation that tier 1 analysis demands.

| DFAT PAF Tier | CROSS Structural Element |
|---|---|
| Tier 3: project-level results | Entry gate indicator specs + progress/completion/continuation gate records |
| Tier 2: country/regional program results | Cohort Position assessment across round applicants |
| Tier 1: portfolio-level indicators | Attestation Corpus across rounds |
| Attributability rule declaration | Causality stance field (attribution position declared before applications open) |
| Climate objective tagging | Coherence disclosure with climate-objective tagging |

The CROSS causality stance field satisfies DFAT's attributability rule requirement at the structural level. Rather than leaving attribution versus contribution determination to post-hoc evaluator judgment, CROSS requires that programs declare their causality position before any applications open. A program claiming direct attribution to an outcome must specify its counterfactual reasoning at entry; a program claiming contribution must specify the multi-causal environment at entry. This pre-commitment satisfies DFAT's requirement that attributability rules be declared as part of indicator documentation rather than asserted retrospectively.

For climate mainstreaming, the CROSS coherence disclosure field, which requires programs to document the relationship between their intervention and other interventions in the same problem domain, carries climate-objective tagging. This provides DFAT with the individual program-level climate documentation it needs to aggregate toward portfolio-level climate mainstreaming threshold assessment.

---

## How WALKRI Complements This Alignment

WALKRI's five pre-publication field specification requirements support DFAT's need for consistent, comparable data across its portfolio. The challenge DFAT faces in aggregating from tier 3 to tier 1 is not only conceptual; it is a data quality problem. If individual programs specify their measurement instruments at different levels of precision, or if intake fields collecting comparable concepts use incompatible collection methods, aggregation produces noise rather than signal.

WALKRI requires that each measurement field be specified with instrument type, unit, collection method, verification pathway, and access information before applications open. For programs collecting climate objective data, WALKRI-compliant field specifications ensure that the climate evidence produced at tier 3 is expressed with sufficient methodological consistency to be meaningfully aggregated at tiers 2 and 1. Programs operating under DFAT's framework gain a practical advantage from WALKRI compliance: their instrument-level field documentation reduces the evidence quality variance that makes portfolio-level aggregation unreliable, directly supporting DFAT's climate mainstreaming threshold assessment obligations.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
