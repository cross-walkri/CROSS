---
title: Sport England Evaluation Framework Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.4 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - https://evaluationframework.sportengland.org
  - https://www.sportengland.org/guidance-and-support/evaluation-and-learning
---

# Sport England Evaluation Framework Compatibility - CROSS+WALKRI

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

This statement documents structural alignment between Sport England's tiered Evaluation Framework and the CROSS+WALKRI specification standards. Sport England publishes a three-level evaluation framework that scales measurement requirements proportionally to grant size and program complexity, and integrates the Active Lives survey as the sector's primary population-level measurement instrument. The three evaluation levels correspond directly to CROSS's obligation modes and evidence strength tiers. WALKRI ensures that intake fields at each level specify what counts as participant activity, what comparison group evidence requires, and what outcome indicators are tracked, before any applicant sees a form.

---

## The Sport England Evaluation Framework

Sport England is the UK's primary sports development funder, distributing National Lottery and government funding to organizations that support sport and physical activity in England. Its tiered Evaluation Framework, published at evaluationframework.sportengland.org, is one of the most elaborated public-sector sport grant measurement standards globally, and its proportionality architecture makes it analytically distinctive relative to evaluation frameworks that apply uniform measurement requirements regardless of program scale.

The Framework defines three evaluation levels. Level 1 applies to smaller grants and simpler programs. At Level 1, grantees are expected to describe their activities and produce basic output data: what they did, how many people participated, and what demographic groups were served. No outcome measurement is required at Level 1, and no comparison group is expected. The measurement burden is deliberately minimal, recognizing that smaller organizations often lack the capacity for rigorous outcome evaluation and that the primary funder accountability need at this scale is for activity verification.

Level 2 applies to programs of moderate scale and complexity. At Level 2, grantees are expected to demonstrate outcomes through pre-post comparisons. A theory of change is a required element for Level 2 and above. Grantees must collect baseline data from participants before program activities begin and follow-up data after activities are complete. The comparison is within-participant (the same individuals before and after), not between groups. Level 2 outcome measurement is designed to be feasible for organizations with limited evaluation capacity while still producing evidence that something changed in participants.

Level 3 applies to larger, more complex programs and to programs where the funder has a specific learning agenda related to causal questions. At Level 3, grantees are expected to demonstrate causation through comparison groups or experimental designs. This may mean randomized controlled trials, quasi-experimental designs with matched comparison groups, or natural experiments. The standard of evidence at Level 3 is the highest in the framework, and the methodology must be approved in advance. Theory of change is mandatory, and the evaluation design must be specified before the program begins.

Sport England integrates the Active Lives survey as the sector's primary population-level measurement instrument. Active Lives is published annually and tracks physical activity levels across the English population by demographic group, geography, and activity type. It provides the baseline against which funded programs' outcomes are situated at the population level. This integration means that Sport England can assess not only whether individual programs are producing outcomes but also whether the portfolio of funded activity is moving population-level physical activity trends.

---

## How CROSS Satisfies the Sport England Framework

CROSS's obligation modes and evidence strength tiers map directly to the three Sport England evaluation levels. The correspondence is structural: CROSS's gate architecture implements the same proportionality logic the Sport England Framework uses, calibrating evidence requirements to the scale and complexity of the program.

Level 1 (activities and basic outputs) corresponds to CROSS Build obligation mode plus the completion gate deliverable specification. Under Build obligation, CROSS requires that the outputs to be delivered be specified before the round opens, including what activities will be conducted, what counts as a participating individual, and what evidence verifies output completion. This is the structural equivalent of Level 1's activity description and basic output reporting requirements. The completion gate provides the verifiable evidence base that Level 1 accountability requires.

Level 2 (outcomes with pre-post comparisons) corresponds to CROSS Change obligation mode plus the counterfactual baseline requirement plus completion gate evidence at the pre-post measurement tier. Under Change obligation, CROSS requires that target condition, baseline measurement, target threshold, measurement timing, and the type of comparison be declared before the round opens. For programs equivalent to Level 2, the comparison type is pre-post within participant, and CROSS's evidence strength taxonomy explicitly identifies pre-post measurement as a distinct evidence tier, appropriate for programs where a comparison group is not feasible. The progress verification gate captures the pre-program baseline; the completion gate captures the post-program measurement. Theory of change is a required element of the CROSS entry specification gate for any round operating under Change obligation, satisfying Level 2's mandatory theory of change requirement.

Level 3 (causation via comparison groups or experimental designs) corresponds to CROSS's independent attestation pathway at the highest evidence strength tier, plus the counterfactual baseline requirement with comparison group specification. CROSS's evidence strength taxonomy identifies experimental comparison (randomized) and quasi-experimental comparison (matched or instrumental) as the highest evidence tiers, and requires that the causality stance field declare which evidence architecture the program will use. This is the structural form of Level 3's requirement that causal evaluation designs be specified before the program begins. CROSS's independent attestation pathway at this tier requires that the comparison group design be documented and independently attested before data collection begins.

The Active Lives population measurement integration corresponds to CROSS's population scope declaration and coherence disclosure. CROSS requires that every round specification declare the population the program is intended to affect and situate program outcomes within the broader population-level trend. For Sport England-funded programs, this means the population scope declaration references Active Lives data as the baseline for the physical activity trend the program is contributing to. The coherence disclosure specifies what mechanism connects individual program outcomes to population-level trends in Active Lives indicators.

| Sport England Level | CROSS Mechanism |
|---|---|
| Level 1: activities and basic outputs | Build obligation; completion gate deliverable specification |
| Level 2: outcomes with pre-post comparisons | Change obligation; counterfactual baseline; progress verification gate (pre); completion gate (post); mandatory theory of change |
| Level 3: causation via comparison groups | Independent attestation pathway at highest evidence tier; causality stance field (experimental or quasi-experimental); comparison group specification |
| Theory of change (Level 2 and above) | CROSS entry specification gate Theory of Change architecture (goal, outcome, output, activity) |
| Active Lives population measurement | CROSS population scope declaration + coherence disclosure referencing Active Lives baseline |

---

## How WALKRI Complements This Alignment

WALKRI's five pre-publication field requirements ensure that intake fields at each Sport England level are measurement instruments specifying what counts as participant activity, what comparison group evidence requires, and what outcome indicators are tracked, before any applicant encounters a form. An intake field that asks "how many participants will the program reach?" is not an output measurement instrument unless it specifies what counts as a participant, what counts as a reached individual (one session attended, three sessions attended, program completion), and over what time period the count applies.

At Level 3, WALKRI's audit requirements apply to comparison group specification fields: the field must specify what comparison group design will be used, what the eligibility criteria for the comparison group are, and what data collection timeline ensures that baseline data for both the program group and the comparison group are collected before any program activities begin. These specifications cannot be determined after the intake process is complete; they must be determined before any applicant encounters the form, because the comparison group design must be consistent across all applicants participating in a Level 3 evaluation. WALKRI makes this requirement explicit and auditable before the round opens.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
