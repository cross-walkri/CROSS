---
title: National Endowment for Democracy Evaluation Framework Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.5 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - NED 2023 Grantmaking Standard Provisions and Appendices (ned.org/publications/2023-grantmaking-standard-provisions-and-appendices/)
  - NED Evaluation Plan requirements (ned.org)
---

# National Endowment for Democracy Evaluation Framework

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

The National Endowment for Democracy (NED) publishes formal grantmaking requirements including a mandatory Evaluation Plan for grantees, governed by its 2023 Grantmaking Standard Provisions and Appendices. Two structural elements distinguish NED's framework from most covered foundation and government grant programs: an Evaluation Plan requirement that explicitly rejects activity completion as a valid evaluation point, requiring outcome-level evidence; and the Cumulative Assessment Report (CAR), a retrospective multi-grant evaluation instrument required of renewed multi-year grantees that assesses accumulated impact and lessons across an entire grant history. The CAR is structurally unique in CROSS+WALKRI's coverage and constitutes a new primitive in the framework map. CROSS satisfies NED's Evaluation Plan requirement through its Theory of Change hierarchy and completion gate architecture, and WALKRI applies to the Evaluation Plan intake at the plan-drafting stage.

---

## The NED Evaluation Framework

NED's evaluation requirements for grantees are governed by its 2023 Grantmaking Standard Provisions and Appendices, publicly available through the NED website. All grantees are required to submit an Evaluation Plan as part of their grant documentation. NED also commissions a minimum of two independent evaluations per year examining subsets of grantees across thematic areas.

Three elements of NED's framework are structurally distinctive within CROSS+WALKRI's coverage.

The first is NED's formal rejection of activity completion as an evaluation standard. The Evaluation Plan requirement states explicitly that grantees must evaluate program outcomes, not merely document that activities were conducted. This is not a preference or a guideline: it is formally stated as a grant condition. Grantees who submit activity documentation in place of outcome evidence do not satisfy the Evaluation Plan requirement. This explicit rejection of activity-level reporting as valid evaluation evidence is unusual in the grant landscape, where most frameworks accept activity completion as at minimum a partial form of evidence.

The second is the Cumulative Assessment Report. For renewed multi-year grantees, NED may require a CAR covering all prior grants in a multi-year sequence. The CAR assesses cumulative impact across the entire grant history and identifies lessons that carry forward. It is not a final evaluation of a single grant cycle; it is a retrospective assessment of accumulated impact and learning spanning multiple cycles. No other framework in CROSS+WALKRI's corpus includes an equivalent instrument.

The third is NED's independent evaluation commissioning. NED commissions at minimum two independent evaluations per year, each examining a thematic subset of grantees. These evaluations are designed and executed by NED rather than by grantees, providing an independent evidence base against which grantee Evaluation Plans can be assessed.

---

## How CROSS Satisfies the NED Framework

CROSS addresses NED's evaluation requirements through its Theory of Change hierarchy and the four-gate sequence, with the CAR creating a new primitive that the current gate architecture does not cover.

**Explicit rejection of activity completion and CROSS's Theory of Change hierarchy:** NED's formal rejection of activity completion as valid evaluation evidence is the regulatory form of CROSS's Theory of Change hierarchy applied as a grant condition. CROSS defines four levels: activities, outputs, outcomes, and goals. The entry specification gate requires that indicators be associated with specific levels and that the causality stance for each indicator be declared. An activity-level indicator (e.g., "workshops held") associated with a causality stance claiming contribution to outcomes fails CROSS's eleven-field specification because the causality stance cannot be supported by activity completion data alone. CROSS and NED are therefore aligned at the structural level: CROSS's indicator specification architecture rules out activity completion as a standalone outcome evaluation, which is exactly the requirement NED's Evaluation Plan imposes as a grant condition.

**Completion gate and NED's Evaluation Plan:** NED's Evaluation Plan requirement maps to CROSS's completion gate: the structured evidence review against pre-specified indicators that determines whether the program produced the outcomes it stated it would produce. A CROSS-conformant grantee submitting an NED Evaluation Plan has already specified, at the entry specification gate, what indicators will be used, what baseline and target values apply, what evidence form will be collected, and what causality stance is claimed. The Evaluation Plan submission under NED is the completion gate record.

**Cumulative Assessment Report as a new primitive:** The CAR does not correspond to any existing CROSS gate. It is neither the completion gate of the most recent cycle nor the entry specification gate of the next cycle. It is a retrospective multi-cycle assessment examining cumulative impact and lessons across an entire grant history. This is a new primitive in the CROSS+WALKRI framework map, here named the multi-cycle retrospective assessment. Whether this should be modeled as a gate type applicable after a defined number of funded cycles, as a protocol required when grant renewal crosses a specified threshold of cumulative investment, or as a funder-initiated review mechanism distinct from the grantee-facing gate sequence is a decision for future CROSS revision. This statement documents the gap and proposes the name.

**Independent evaluations and CROSS's attestation gate:** NED's independently commissioned evaluations provide an external evidence base that operates above the individual grantee's gate sequence. They correspond in function to CROSS's attestation gate at the portfolio level: independent verification that a set of funded programs produced what they stated they would produce, using evidence not generated by the grantees themselves.

| NED Evaluation Element | CROSS Provision |
|:--|:--|
| Explicit rejection of activity completion as evaluation evidence | Theory of Change hierarchy (activity-level indicators cannot satisfy outcome causality stance) |
| Evaluation Plan requirement (outcome-level evidence) | Completion gate (structured evidence review against pre-specified outcome indicators) |
| Evaluation Plan submitted at grant stage | Entry specification gate (indicators, baselines, targets, causality stances declared before activities begin) |
| Cumulative Assessment Report (multi-cycle retrospective) | New primitive: multi-cycle retrospective assessment (not yet in CROSS architecture) |
| NED-commissioned independent evaluations | Portfolio-level attestation (independent verification above individual grantee gate sequence) |
| Thematic subset evaluation | Comparison group field in eleven-field specification (Field 10) |

---

## How WALKRI Complements This Alignment

WALKRI's pre-publication requirements apply to NED's Evaluation Plan at the plan-drafting stage, not at the reporting stage. NED's requirement that grantees specify outcomes rather than activities means that by the time an Evaluation Plan is submitted, the grantee must already know what evidence will constitute proof of the outcomes claimed. WALKRI requires exactly this specification, field by field, before any program activity begins.

For each outcome indicator in an NED Evaluation Plan, WALKRI requires: criterion intent (what the indicator is designed to measure within the democracy-support Theory of Change), operational definition (exactly what counts as evidence of the outcome), response form (how outcome data is collected and recorded), evidence form (what documentation is required to substantiate each data point), and compliance threshold (the minimum standard a data point must meet to count toward the outcome assessment). Without this level of specification at the plan-drafting stage, NED's rejection of activity completion as evaluation evidence cannot be enforced: grantees can claim outcome evidence while collecting data that does not rise to the standard the Evaluation Plan implies.

The Cumulative Assessment Report creates an additional WALKRI obligation for multi-year grantees: indicator specifications from earlier grant cycles must be preserved in sufficient detail to allow cross-cycle comparability. If the operational definition of a key indicator changes between cycles without documentation, the CAR cannot validly aggregate impact data across those cycles. WALKRI's pre-publication audit creates the archival record needed for a valid CAR, because each cycle's indicator specifications are committed to before data collection begins and preserved as part of the cycle's conformance record.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
