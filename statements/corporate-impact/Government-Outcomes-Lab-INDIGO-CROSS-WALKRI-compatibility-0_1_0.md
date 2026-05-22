---
title: INDIGO Data Specification Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - INDIGO Data Specification v0.1, Government Outcomes Lab, Blavatnik School of Government, University of Oxford, https://indigo-standard.readthedocs.io/en/latest/
---

# INDIGO Data Specification Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

CROSS and WALKRI together address the INDIGO Data Specification v0.1 at the results chain, attribution, and evidence specification layer. INDIGO is the open data standard developed by the Government Outcomes Lab at Oxford's Blavatnik School for modeling social impact bonds and outcomes-based contracts. It structures each impact bond as a project with defined outcome metrics, stakeholder roles, payment triggers, and result data fields. CROSS's output and outcome architecture, gate sequence, and causality stance field map to the core structural requirements that INDIGO formalizes for impact bond data. WALKRI's evidence form requirement addresses INDIGO's reproducibility requirements for result data.

This compatibility matters for commissioners designing outcomes-based contracts who want a measurement specification standard that satisfies INDIGO data requirements, for impact bond investors who reference INDIGO records in due diligence, and for evaluators submitting results data to the INDIGO dataset.

---

## What INDIGO Is

INDIGO (Indigo Data Specification) is an open data standard developed by the Government Outcomes Lab at the Blavatnik School of Government, University of Oxford. It provides a structured schema for recording social impact bond transactions, including the parties involved, the outcomes targeted, the financial structure, the payment triggers, and the results achieved. The standard enables cross-jurisdictional comparison of outcomes-based contracts and powers the GOL's international dataset of social impact bonds.

INDIGO models each impact bond or outcomes-based contract as a project record containing: a results chain from inputs through outputs to outcomes; defined outcome metrics with units and baseline data; stakeholder roles (commissioner, service provider, investor, evaluator, and outcomes payer); payment triggers linked to verified outcome attainment; and result data fields recording actuals at specified measurement intervals.

The standard is designed for data publication and aggregation: INDIGO records are intended to be machine-readable, comparable across projects, and sufficient for a third party to understand what was measured, how, and with what result, without requiring access to the underlying project documentation.

---

## Results Chain: CROSS Output and Outcome Architecture

INDIGO's results chain structure (inputs, activities, outputs, outcomes, impact) is the model against which CROSS's ToC architecture maps most directly. CROSS's Theory of Change architecture requires explicit documentation of goals, outcomes, outputs, and activities with named causal links and stated assumptions. Each link in the CROSS ToC is a falsifiable causal claim that can be compared against actuals at the relevant gate.

The CROSS output layer maps to INDIGO's output metrics layer: deliverables produced by the intervention, verifiable without reference to participant response. The CROSS outcome layer maps to INDIGO's outcome metrics layer: changes in participant or community state that constitute the basis for payment or performance assessment. The named causal link between CROSS's output and outcome layers corresponds to the mechanism assumption that INDIGO's results chain requires to be documented but often leaves implicit.

CROSS requires both output and outcome gates in its four-gate sequence, meaning that both layers of INDIGO's results chain have a formal verification moment in the CROSS architecture. A program using CROSS for an outcomes-based contract produces gate evidence at the output layer and separately at the outcome layer, matching the two-tier measurement structure that INDIGO payment trigger logic depends on.

---

## Payment Triggers: CROSS Gate Architecture

INDIGO payment triggers are the contractual events at which outcomes payments are released. They are defined by outcome metric attainment thresholds and verification requirements. The CROSS gate architecture maps to payment trigger logic structurally: each gate is a formal verification event at which evidence is submitted against pre-specified criteria, and gate passage or failure is a binary determination.

CROSS's compliance threshold (Field 11 in the eleven-field indicator specification) is the CROSS equivalent of the payment trigger threshold: it specifies the level of attainment that constitutes satisfactory performance for that indicator. When a CROSS-compliant program uses an outcomes-based contract structure, Field 11 values and payment trigger thresholds should be identical; any divergence between them is a specification inconsistency that the entry gate process surfaces before implementation begins.

CROSS's gate date fields address the timing dimension of payment triggers: each gate has a scheduled date, and late gate submission or evidence insufficiency at a gate creates a formal record of the deviation. INDIGO records payment trigger dates as part of the contract structure; CROSS gate records are the instrument-level evidence base for those payment events.

---

## Attribution: Causality Stance Field

INDIGO records include attribution fields describing how outcome attainment is attributed to the intervention. CROSS's causality stance field is the structural location for this attribution claim: the program must state what attribution logic it is applying, what counterfactual basis it is using, and whether it is claiming contribution or attribution. This field is gate-locked at the entry specification gate and cannot be changed during implementation without a formal gate record.

For INDIGO data quality purposes, the causality stance field ensures that the attribution claim is consistent across reporting cycles and explicit enough to be reproduced by a third-party reviewer. INDIGO's reproducibility requirement is that a reviewer reading the record can understand what the outcome measurement was, how it was conducted, and what attribution logic was applied.

---

## Evidence Reproducibility: WALKRI Evidence Form

INDIGO's reproducibility requirement extends to result data: a reviewer of an INDIGO record should be able to understand how outcome data was collected and verified, not merely what numbers were reported. WALKRI's evidence form requirement addresses this directly. The evidence form field in WALKRI specifies, for every measurement field, what independent verification pathway exists and how a reviewer could access or replicate the verification. Evidence forms must be independent of the reporting party's self-assessment; they must reference a verifiable artifact.

For INDIGO-aligned programs, WALKRI's evidence form entries are the instrument-level documentation that supports the reproducibility of result data fields in the INDIGO record. A WALKRI-compliant measurement instrument produces evidence that is traceable to its source, independently verifiable, and documented before data collection begins. This is the specification-layer precondition for INDIGO data quality.

---

## Structural Mapping Table

| INDIGO Element | CROSS Provision | WALKRI Provision | Coverage |
| :-- | :-- | :-- | :-- |
| Results chain (outputs, outcomes) | ToC architecture with named causal links; output and outcome gate layers | No direct provision | Structural: two-tier results chain with named causal mechanisms |
| Outcome metrics with units and baseline | Fields 1-5 (name, definition, unit, baseline, target) | Criterion intent and operational definition requirements | Structural: eleven-field indicator specification |
| Payment triggers | Gate compliance threshold (Field 11); gate date fields | No direct provision | Structural: threshold and timing logic matches payment trigger structure |
| Attribution claim | Causality stance field | No direct provision | Structural: explicit, gate-locked attribution declaration |
| Reproducibility of result data | Evidence form (Field 10) in indicator specification | Evidence form requirement: independent verification pathway documented pre-collection | Structural: traceable, independent evidence for all measurement fields |
| Stakeholder roles | No direct provision | No direct provision | Outside specification scope |
| Financial structure | Concurrent funding disclosure; financial transparency obligation dimension | No direct provision | Partial: funding relationships documented, not investment structure |

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

INDIGO Data Specification: https://indigo-standard.readthedocs.io/en/latest/

Government Outcomes Lab: golab.bsg.ox.ac.uk

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. Results chain, payment trigger, attribution, and evidence reproducibility mappings documented. Stakeholder roles and financial structure identified as outside specification scope. |
