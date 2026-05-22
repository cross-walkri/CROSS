---
title: Optimism Retro Funding Impact Evaluation Methodology Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.5 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - Optimism Retro Funding round documentation (community.optimism.io)
  - optimism.io/retropgf
---

# Optimism Retro Funding Impact Evaluation Methodology (2025)

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

CROSS+WALKRI covers Optimism RetroPGF Rounds 1-4 in a separate compatibility statement. This statement covers the materially revised Retro Funding methodology launched in 2025, which introduced three structural innovations that exceed prior coverage and require independent documentation: a weighted impact metrics formula replacing subjective badge-holder voting; an Impact Chain dependency graph requiring applicants to declare their causal position in an ecosystem impact chain; and a human-in-the-loop override mechanism with published override conditions. Each of these innovations has a direct CROSS or WALKRI structural correspondent. Together they bring Optimism's retroactive funding methodology closer to CROSS conformance than any prior Web3 round design in the corpus.

---

## The 2025 Retro Funding Methodology

Optimism's 2025 Retro Funding methodology departed from the earlier RetroPGF design in three structural respects.

The first is the weighted impact metrics formula. Earlier RetroPGF rounds allocated funding through badgeholder voting, with minimal constraint on voting criteria. The 2025 methodology replaced unconstrained voting with a published quantitative formula that weights multiple impact metrics to produce allocation recommendations. The metric weights and formula structure are published before each round opens and do not change after applications are received. Badgeholders retain input, but the formula is the primary allocation mechanism.

The second is the Impact Chain dependency graph. Each applicant must declare its position in a causal chain showing how its outputs contribute to downstream ecosystem outcomes. The Impact Chain makes explicit the causal pathway between a project's direct deliverables and the broader impact the round is designed to fund. Circular claims (project A contributes to project B which contributes to project A) and unverifiable chains (projects claiming contribution to outcomes with no traceable pathway) are excluded from eligibility.

The third is the human-in-the-loop override. The formula-based allocation can be overridden by a designated committee when the formula produces results that violate the round's stated objectives. Override conditions and the threshold at which committee review is triggered are published before the round opens. The override mechanism is not a discretionary fallback; it is a pre-specified procedure with defined conditions.

---

## How CROSS Satisfies the 2025 Retro Funding Framework

CROSS addresses all three structural innovations in the 2025 methodology, and the retroactive obligation mode in CROSS's Build/Change/Retroactive architecture is directly engaged here in a way that prior RetroPGF coverage did not fully develop.

**Published metrics formula and CROSS's entry specification gate:** The published metrics formula, committed to before applications open and unchangeable after submissions are received, is CROSS's entry specification gate applied as a computational protocol. The entry specification gate requires that gate criteria be declared before any applicant submits. The 2025 methodology operationalizes this as a weighted formula rather than a narrative specification, but the structural requirement is identical: the evaluation standard is fixed before applications open. A CROSS-conformant retroactive round publishes its allocation formula as part of the entry specification gate documentation, making the formula a formal gate criterion rather than an internal scoring tool.

**Impact Chain and CROSS's Theory of Change hierarchy:** The Impact Chain dependency graph is a formal implementation of CROSS's Theory of Change requirement applied at the ecosystem level. CROSS requires that indicators be associated with specific levels of the Theory of Change hierarchy (activities, outputs, outcomes, goals) and that the causal relationship between levels be declared. The Impact Chain requires the same declaration: projects must show the outputs they produced, the outcomes those outputs contribute to, and the goals those outcomes serve within the Optimism ecosystem. Circular and unverifiable chains are excluded because they fail to satisfy CROSS's causality stance field: a project claiming contribution to an outcome without a traceable causal pathway cannot declare a valid causality stance. The Impact Chain requirement makes this failure visible at the application stage rather than at evaluation.

**Human-in-the-loop override and CROSS's completion gate with override mechanism:** CROSS's completion gate is the structured evidence review that determines whether a program produced what it specified it would produce. The human-in-the-loop override, with its published conditions and committee threshold, is CROSS's completion gate with an explicit, pre-specified override mechanism: pre-defined criteria under which the gate determination can be revisited by a designated body. This is the first framework in CROSS+WALKRI's coverage to formalize a completion gate override with published conditions. It is compatible with CROSS's architecture and adds a named override procedure that CROSS does not currently specify. Future CROSS revision may wish to formalize the override mechanism as an optional gate component applicable when formula-based evaluation is used.

**Retroactive obligation mode:** The 2025 Retro Funding methodology operates in CROSS's retroactive obligation mode: evaluation is conducted on work already completed, and the gate sequence is retrospective rather than prospective. The entry specification gate, in retroactive mode, is the publication of the metrics formula and Impact Chain requirements before applications open; it does not specify what applicants will do, but what evidence they must provide about what they have already done. This is a more developed and structural implementation of retroactive obligation mode than any prior Web3 coverage in the corpus.

| 2025 Retro Funding Element | CROSS Provision |
|:--|:--|
| Published weighted impact metrics formula (pre-round) | Entry specification gate (evaluation criteria fixed before applications open) |
| Formula committed to before submissions received | Entry specification gate irreversibility requirement |
| Impact Chain dependency graph | Theory of Change hierarchy (activities, outputs, outcomes, goals; circular chains excluded by causality stance requirement) |
| Exclusion of circular and unverifiable chains | Causality stance field (Field 11) - invalid causality stance is a conformance failure |
| Human-in-the-loop override with published conditions | Completion gate with pre-specified override mechanism (new component; not yet formalized in CROSS) |
| Round-specific impact metrics pre-specified before applications open | Entry specification gate + eleven-field indicator specification |
| Retroactive eligibility scope | Retroactive obligation mode in CROSS Build/Change/Retroactive architecture |

---

## How WALKRI Complements This Alignment

WALKRI's pre-publication requirements apply to the metrics collection layer of the 2025 Retro Funding methodology. The published metrics formula specifies which impact metrics are used and how they are weighted, but it does not necessarily specify, for each metric, what evidence form satisfies the metric, what documentation standard applies to self-reported data, and what threshold distinguishes a valid measurement from an estimate. These are precisely the five pre-publication requirements WALKRI imposes.

For each impact metric in the formula, WALKRI requires: criterion intent (what the metric is designed to measure in the Optimism ecosystem Impact Chain), operational definition (exactly what activity or output counts toward the metric), response form (how the metric value is calculated and reported), evidence form (what on-chain or off-chain documentation is required to substantiate the reported value), and compliance threshold (the minimum documentation standard a project must meet for its metric submission to be counted). Without this specification, the metrics formula may be mathematically precise while operating on inputs of variable quality: a project with rigorous on-chain evidence and a project with informal self-reported estimates may receive the same formula treatment even though the underlying data quality is not equivalent.

The Impact Chain dependency graph creates a specific WALKRI opportunity. The causal pathway each project declares must be verifiable: each link in the chain from outputs to ecosystem outcomes should have an evidence form that can be independently checked. WALKRI applied to the Impact Chain specification means that before any round opens, the Optimism Foundation publishes what evidence form satisfies each claim of causal contribution in the dependency graph, preventing self-reported causal claims from substituting for documented causal pathways.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
