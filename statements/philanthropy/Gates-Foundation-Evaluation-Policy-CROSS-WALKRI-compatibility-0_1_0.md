---
title: Gates Foundation Evaluation Policy Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.1 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - https://www.gatesfoundation.org/about/policies-and-resources/evaluation-policy
---

# Gates Foundation Evaluation Policy Compatibility - CROSS+WALKRI

## Summary

This statement documents structural alignment between the Gates Foundation's formal evaluation policy, "Learning for Impact," and the CROSS+WALKRI specification standards. This statement is distinct from a separate compatibility statement covering the Gates Open Access Policy, which governs data sharing obligations; that document should be consulted for questions about publication and data access requirements. This statement addresses only the evaluation policy's requirements for planning, execution, and institutional continuity of foundation-funded evaluations.

CROSS v0.4.1 and WALKRI v0.1.6 are both published under CC0 at github.com/CrossWalkri. The Gates Foundation Evaluation Policy is publicly available at gatesfoundation.org/about/policies-and-resources/evaluation-policy.

## The Gates Foundation Evaluation Policy: Core Requirements

"Learning for Impact" establishes six interconnected requirements for foundation-funded evaluation:

First, evaluation planning must be integrated early into the grant proposal process, with measurable outcomes agreed between the foundation and grantees before grants are awarded. Second, the policy organizes evaluations into a three-tier taxonomy: evaluations that strengthen program effectiveness (Tier 1), evaluations that test causal effects (Tier 2), and evaluations that improve institutional performance (Tier 3). Third, all program teams are required to maintain an evaluation plan shared openly with partners. Fourth, all foundation-funded evaluations must be recorded in a central registry for institutional continuity. Fifth, a central Strategy, Measurement and Evaluation team sets standards across the foundation's portfolio. Sixth, the policy espouses an "actionable measurement" philosophy: purpose-driven evaluation rather than adherence to any single method.

## CROSS Alignment in Detail

CROSS's entry specification gate directly implements the first requirement. No funding round may open under CROSS without a published round specification that includes measurable outcome thresholds, milestone plans, and evidence type declarations. This means measurable outcomes are agreed structurally before any application is submitted, not negotiated retrospectively after grants are awarded. The gate is a precondition for the round opening, not a recommendation for good practice.

CROSS's three obligation modes (Build, Change, and Retroactive) correspond structurally to the three-tier evaluation taxonomy. Build obligations apply to programs that are creating new outputs and infrastructure; this maps to Tier 1, where evaluation strengthens program effectiveness by testing whether outputs are being produced as planned. Change obligations apply to programs that are modifying conditions or practices in a system with multiple actors; this maps to Tier 2, where evaluation tests causal or contributory effects on outcomes that cannot be attributed to any single actor. Retroactive obligations apply to programs that are seeking recognition for change already demonstrated; this maps to Tier 3, where evaluation serves institutional learning and performance improvement by examining what has already occurred. The correspondence is structural, not definitional: CROSS does not use the tier language, but the obligation modes address the same underlying distinctions.

CROSS's pre-commitment requirement, which mandates that the round specification be published before applications open, implements the third requirement. Partners, meaning applicants and the broader community, have access to the evaluation plan before they engage with the process. This is not a policy commitment to share evaluation plans; it is a gate condition that makes sharing the precondition for a round opening at all.

CROSS's Attestation Corpus implements the fourth requirement. Each round and each gate decision produces a structured record in the Attestation Corpus. Those records are persistent, referenced by round specification, and accessible across cycles. The Corpus functions as the central registry the policy requires, generated automatically by the gate process rather than maintained as a separate administrative task.

## WALKRI Alignment in Detail

WALKRI's five field requirements implement the "actionable measurement" philosophy at the instrument level. The policy's rejection of adherence to any single method in favor of purpose-driven evaluation requires that measurement instruments be designed around the specific question a program is trying to answer. WALKRI's pre-publication audit enforces exactly this: every field in an intake or update instrument must be specified as a measurement instrument, with its construct, metric, and evidence type declared before data collection begins. A field that is not pre-specified as a measurement instrument is not an instrument; it is a label.

WALKRI also supports the first requirement directly. Because WALKRI requires that measurement instruments be defined before any applicant encounters them, the measurable outcomes agreed at grant entry are operationalized in the intake fields themselves. The agreement is not a text commitment in a grant agreement; it is instantiated in the structure of the data collection instrument.

## Scope and Limitations

This alignment is structural and analytical. The Gates Foundation has not reviewed or endorsed this statement. CROSS+WALKRI does not claim certification against the Gates Foundation Evaluation Policy; it documents how a funder or intermediary implementing CROSS+WALKRI would satisfy the policy's structural requirements. Programs operating under other evaluation frameworks may satisfy the same policy requirements through different mechanisms; this statement addresses only the CROSS+WALKRI pathway.

Readers should not interpret this statement as covering data access, publication, or open-licensing requirements. Those are addressed separately in the Gates Open Access Policy compatibility statement.
