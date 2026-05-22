---
title: OCHA Country-Based Pooled Funds Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - OCHA Country-Based Pooled Funds Global Guidelines, December 2022, https://www.unocha.org/publications/report/world/country-based-pooled-funds-global-guidelines
---

# OCHA Country-Based Pooled Funds Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

CROSS and WALKRI together address the OCHA Country-Based Pooled Funds Global Guidelines (December 2022) at the results chain, accountability, and institutional alignment layer. CBPF guidelines govern rapid-disbursement emergency grants to UN agencies and NGOs through a five-principle performance framework: inclusiveness, timeliness, flexibility, efficiency, and accountability. CROSS's output and outcome gate architecture satisfies the results-chain requirements that CBPF results monitoring templates encode. CROSS's gate date fields address the timeliness principle. WALKRI's integrity requirement addresses the accountability principle at the instrument layer. CROSS Field 10 (institutional framework alignment) accommodates CBPF sector codes.

The CERF (Central Emergency Response Fund) operates under the same guidelines family. This statement applies to both CBPF and CERF grant structures unless otherwise noted.

---

## What CBPF Is

Country-Based Pooled Funds are multi-donor humanitarian financing mechanisms managed by OCHA. They channel contributions from donor governments to UN agencies and NGOs for rapid humanitarian response, operating in-country under the oversight of the Humanitarian Coordinator. The December 2022 Global Guidelines consolidate performance requirements, results monitoring templates, and accountability obligations across all CBPFs worldwide.

The five-principle performance framework establishes what CBPFs are expected to achieve and how they are assessed: inclusiveness (reaching the most vulnerable), timeliness (rapid disbursement and response), flexibility (adaptive programming), efficiency (value for money), and accountability (transparent reporting and results verification). Each principle has associated performance indicators tracked through the CBPF live data hub and reported in OCHA's annual CBPF global report.

Results monitoring under CBPF requires grantees to submit progress reports against pre-defined output and outcome indicators, following standardized sector reporting templates. The OCHA Grant Management System (GMS) structures the reporting cycle.

---

## Results-Chain Requirements: CROSS Output and Outcome Gates

CBPF results monitoring templates require grantees to report against output indicators (activities completed, people reached) and outcome indicators (conditions changed) at specified reporting intervals. These two layers correspond directly to CROSS's output and outcome gate architecture. CROSS requires separate gate evidence submissions at the output layer and the outcome layer; a grantee using CROSS for a CBPF grant produces gate evidence at the intervals CBPF reporting requires, structured against pre-specified indicators that match the template fields.

CROSS's eleven-field indicator specification (Fields 1-11) is more detailed than CBPF's standard template fields, but is fully compatible: a CROSS-compliant indicator specification satisfies CBPF template requirements and provides additional specificity (operational definition, evidence form, compliance threshold) that CBPF does not require but does not prohibit. Programs using CROSS for CBPF grants can use their CROSS indicator records as the primary specification source for populating CBPF template fields.

---

## Timeliness Principle: CROSS Gate Dates

The timeliness principle concerns both disbursement speed (OCHA-managed) and grantee response speed (program-managed). At the program level, timeliness is assessed through milestone adherence: are activities initiated on schedule, are outputs delivered by committed dates, and are progress reports submitted within required windows.

CROSS's gate date fields address the program-level timeliness dimension structurally. Each gate in the CROSS four-gate sequence has a scheduled date. Late gate submission or evidence gap at a gate creates a formal record of the deviation, with date and reason. For CBPF accountability purposes, this record is the instrument-level evidence of whether the program met its timeliness commitments; it is not a separate document but an artifact of the gate process itself.

---

## Accountability Principle: WALKRI Integrity Requirement

The accountability principle in CBPF guidelines requires transparent and verifiable reporting: grantees must report accurately against their commitments, and the data they submit must be independently verifiable. OCHA's accountability requirements include third-party monitoring for high-value grants and standard verification procedures for all grants.

WALKRI's integrity requirement addresses the accountability principle at the instrument design layer. The requirement specifies that every measurement field's evidence form must be independent of the reporting grantee's self-assessment. Evidence cannot be an artifact produced and controlled by the entity whose performance is being assessed. When WALKRI's integrity requirement is applied to CBPF reporting instruments, the resulting instruments produce data that satisfies OCHA's independent verifiability expectation structurally, before data collection begins, rather than through post-hoc verification alone.

---

## Field 10: CBPF Sector Codes

CROSS Field 10 (institutional framework alignment) is the field in the eleven-field indicator specification that records what external classification systems, codes, or frameworks the indicator is aligned with. CBPF grants are categorized by humanitarian sector (food security, health, shelter, WASH, protection, and others) and reported against sector-specific templates that use CBPF sector codes as organizing categories.

Field 10 accommodates CBPF sector codes by design. A CROSS-compliant grantee records the relevant CBPF sector code in Field 10 for each indicator, establishing a formal, documented link between the CROSS indicator record and the CBPF reporting category. This is not a translation step at reporting time but a specification-layer alignment recorded before data collection begins.

---

## Structural Mapping Table

| CBPF Requirement | CROSS Provision | WALKRI Provision | Coverage |
| :-- | :-- | :-- | :-- |
| Output indicators (results monitoring templates) | Output gate; eleven-field indicator specification | Five pre-publication field requirements | Structural: gate evidence satisfies template reporting requirements |
| Outcome indicators (results monitoring templates) | Outcome gate; Fields 1-5 (name, definition, unit, baseline, target) | Criterion intent and operational definition requirements | Structural: outcome indicator specification satisfies CBPF requirements |
| Timeliness principle | Gate date fields; formal record of late submission or evidence gap | No direct provision | Structural: program-level milestone adherence documented in gate records |
| Accountability principle | Concurrent funding disclosure; obligation architecture | Integrity requirement: evidence independent of grantee self-report | Structural: instrument-level independence from reporting party |
| Sector code alignment | Field 10 (institutional framework alignment) accommodates CBPF sector codes | No direct provision | Structural: sector code recorded in indicator specification |
| Inclusiveness principle | Population scope (Field 6); disaggregation ratchet (Field 8) | No direct provision | Partial: targeting and disaggregation documented, not operational delivery |
| Flexibility principle | Change obligation mode in CROSS three-mode architecture | No direct provision | Partial: gate-locked record of changes and their rationale |

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

OCHA CBPF Global Guidelines: https://www.unocha.org/publications/report/world/country-based-pooled-funds-global-guidelines

OCHA CBPF live data hub: cbpfgms.unocha.org

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. Results chain, timeliness, accountability, and sector code mappings documented. Inclusiveness and flexibility principles assessed as partial scope. CERF applicability noted. |
