---
title: Packard Foundation MEL Guiding Principles Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - Packard Foundation Guiding Principles and Practices for Monitoring, Evaluation and Learning, 2019 revision, https://www.packard.org/wp-content/uploads/2019/01/MELGuidingPrinciples.pdf
---

# Packard Foundation MEL Guiding Principles Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

CROSS and WALKRI together address the Packard Foundation "Guiding Principles and Practices for Monitoring, Evaluation and Learning" (2019 revision) at the monitoring loop, intake instrument quality, and proportionality layer. The Packard MEL principles require use of evidence before work begins, proportionality between evaluation rigor and grant size, a learning culture supported by structured reflection, and grantee participation in MEL design. CROSS's gate architecture structures the monitoring and learning loop that Packard requires: entry gates establish what is measured before work begins, and progress gates create the learning loop that feeds adaptive management. WALKRI ensures that the collection instruments used in monitoring are properly specified measurement instruments. CROSS's gate rigor configuration addresses the proportionality requirement.

This compatibility applies to Packard Foundation grantees using CROSS for grant program management and to intermediaries deploying CROSS-based grant facilities that Packard funds.

---

## What the Packard Foundation MEL Principles Are

The Packard Foundation's Guiding Principles and Practices for Monitoring, Evaluation and Learning were revised in 2019 following a comprehensive evaluation of the Foundation's MEL practice conducted by ORS Impact. The revision reflects two decades of grant-making experience and incorporates lessons from the ORS Impact evaluation, particularly around proportionality and grantee burden. The principles apply to all Packard grantees across the Foundation's program areas: conservation science, population and reproductive health, early childhood, arts, and organizational effectiveness.

Four principles govern Packard's MEL approach. The first is use of evidence: grant programs are expected to draw on existing evidence before designing interventions, to specify what new evidence they will generate, and to use findings for adaptation. The second is proportionality: MEL requirements should be calibrated to grant size, program risk, and strategic priority; not all grants require the same rigor of evidence. The third is learning culture: the Foundation expects grantees to treat MEL as a learning tool, not a compliance exercise, and to engage in structured reflection on findings. The fourth is grantee participation: grantees should be involved in designing the MEL approach for their grant, not simply handed a monitoring template.

---

## Use of Evidence Before Work Begins: CROSS Entry Gate

The use of evidence principle has two temporal dimensions: what evidence exists before the program begins (prior evidence review), and what evidence the program will generate during implementation (prospective measurement design). CROSS's entry specification gate addresses the prospective dimension directly. At the entry gate, the program locks its eleven-field indicator specification, Theory of Change, and evidence plan. The gate cannot close until these elements are complete and documented. This means that by the time any grantee activity begins, the program has a documented evidence plan: what will be measured, how, at what frequency, and to what standard.

The ToC architecture in CROSS also addresses the prior evidence dimension at the structural level. The named causal links in the ToC require assumptions to be stated explicitly; assumptions that contradict available evidence are identifiable at the specification stage. While CROSS does not require a formal prior evidence review as a gate condition, the ToC architecture creates the structural space for prior evidence to be incorporated: assumptions can be annotated with their evidence base, and the causal chain can document where evidence supports the links and where it does not.

---

## Learning Loop: CROSS Progress Gates

The learning culture principle requires that MEL be designed as a learning tool, with structured moments for reflection on findings and adaptation of programming. A monitoring system that produces data but has no structured moment at which findings are reviewed and acted upon does not satisfy this principle, regardless of data quality.

CROSS's progress gates are the structural mechanism for the learning loop. Each progress gate requires evidence submission against pre-specified indicators and a formal assessment of whether the program is on track. The gate evidence record and the assessment together constitute the structured reflection moment that Packard's learning culture principle requires. A program using CROSS that misses a progress gate or submits incomplete evidence at a progress gate creates a formal record of that gap, which is itself data for learning: the gate failure is a signal that something in the program's monitoring system or implementation plan needs attention.

The CROSS three-mode obligation architecture also contributes to the learning loop. If a program submits a Change obligation record documenting a programming adaptation, that record is a formal artifact of the learning-and-adaptation cycle: it documents what changed, why, and what evidence triggered the change. Change obligation records are the instrument-level evidence that adaptive management is occurring rather than being claimed.

---

## Proportionality: Gate Rigor Configuration

The proportionality principle is one of the most operationally significant elements of the Packard MEL approach. Not all grants require impact evaluations; not all grants require randomized controlled trials; not all grants justify the time and expense of extensive external evaluation. MEL requirements should be calibrated to the scale of the investment, the strength of prior evidence, the novelty of the approach, and the strategic priority of the program area.

CROSS addresses proportionality through gate rigor configuration. Programs can configure the evidence requirements at each gate to match the grant size and risk profile of the program. A small, short-cycle grant may require only output-level evidence at a single progress gate. A large, multi-year grant in a novel program area may require outcome-level evidence at multiple progress gates with external verification. Gate rigor level is documented in the obligation record and does not change without a formal gate record.

This configuration mechanism is the structural expression of the proportionality principle in CROSS: each program configures its gate architecture to match its evidence burden to its grant characteristics, and the configuration is explicit and documented rather than implicit in reporting templates.

---

## Intake Instrument Quality: WALKRI

Packard's MEL principles do not address instrument specification in detail, but the use of evidence principle implies that the instruments collecting monitoring data must be capable of producing reliable evidence. An indicator that is ambiguously defined, a response form that conflates self-report with administrative data, or an evidence form that cannot be independently verified produces data that cannot support evidence-based adaptation. WALKRI addresses this gap at the instrument specification layer.

WALKRI's five field requirements applied to Packard grantee monitoring instruments ensure that: the purpose of each field is stated (criterion intent), the boundaries of each measurement are explicit (operational definition), the collection method is matched to the measurement goal (response form), every field has an independent verification pathway (evidence form), and the standard for acceptable data quality is explicit (compliance threshold). These five requirements are the quality management system for intake instrument design that the use of evidence and learning culture principles implicitly require.

---

## Structural Mapping Table

| Packard MEL Principle | CROSS Provision | WALKRI Provision | Coverage |
| :-- | :-- | :-- | :-- |
| Use of evidence before work begins | Entry specification gate: indicators, ToC, and evidence plan locked before implementation | Criterion intent and operational definition requirements ensure measurement instruments produce reliable evidence | Structural: evidence plan completed at entry gate |
| Proportionality | Gate rigor configuration per program, matched to grant size and risk | No direct provision | Structural: rigor level explicit in obligation record |
| Learning culture / structured reflection | Progress gates as formal learning loop moments; Change obligation records document adaptations | No direct provision | Structural: gates are structured reflection moments with formal evidence requirements |
| Grantee participation | No direct provision | No direct provision | Outside specification scope: participation is a process design question |
| Prior evidence review | ToC causal assumptions can be annotated with evidence base | No direct provision | Partial: structural space for prior evidence, not a required gate condition |

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

Packard Foundation MEL Guiding Principles: https://www.packard.org/wp-content/uploads/2019/01/MELGuidingPrinciples.pdf

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. Use of evidence, learning loop, proportionality, and WALKRI instrument quality mappings documented. Grantee participation identified as outside specification scope. Prior evidence review assessed as partial. |
