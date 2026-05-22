---
title: ICMA Harmonised Framework for Impact Reporting for Social Bonds Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - ICMA Harmonised Framework for Impact Reporting for Social Bonds, updated June 2025, https://www.icmagroup.org/sustainable-finance/impact-reporting/
---

# ICMA Harmonised Framework for Impact Reporting for Social Bonds Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

CROSS and WALKRI together address the ICMA Harmonised Framework for Impact Reporting for Social Bonds (updated June 2025) at the indicator documentation and year-over-year comparability layer. ICMA's framework requires annual reporting on quantitative performance indicators against defined target populations, use-of-proceeds documentation, and year-over-year comparability of impact data. CROSS Fields 1 through 6 satisfy ICMA's indicator documentation requirements. CROSS's disaggregation ratchet (Field 8) ensures the year-over-year comparability that the framework requires. Programs within social bond financing structures can use CROSS reporting as the primary data source for their ICMA impact reports.

---

## What the ICMA Harmonised Framework Is

The ICMA Harmonised Framework for Impact Reporting for Social Bonds is part of the ICMA Social Bond Principles ecosystem. It provides issuers of social bonds with a standardized template for annual impact reporting, including recommended indicator categories, reporting formats, and disclosure requirements. The June 2025 update reflects recent market practice and aligns with the ICMA Green and Sustainability Bond impact reporting frameworks for cross-asset comparability.

The framework applies to social bonds whose proceeds finance programs addressing target populations: people living below the poverty line, disadvantaged populations, populations affected by natural disasters, and other defined vulnerable groups. Annual reporting under the framework must include: the amount allocated to each use-of-proceeds category, the estimated or measured impact on target populations, quantitative performance indicators with units and measurement methodology, and year-over-year comparison of impact data where available.

The framework is voluntary guidance rather than a binding standard, but institutional investors increasingly require framework-aligned reporting as a condition of social bond investment. Rating agencies and second-party opinion providers assess issuer reporting quality against the framework's requirements.

---

## Indicator Documentation: CROSS Fields 1-6

ICMA's framework requires impact indicators to be documented with sufficient specificity for an investor to assess measurement quality. Required elements include: indicator name and definition, unit of measurement, baseline data where available, target level, and population scope. These elements correspond directly to CROSS Fields 1 through 6.

Field 1 (indicator name) and Field 2 (indicator definition) satisfy the name and definition requirement. Field 3 (unit of measurement) satisfies the unit requirement. Field 4 (baseline) and Field 5 (target) satisfy the baseline and target requirements. Field 6 (population scope) satisfies the target population requirement: it specifies what population the indicator measures, which is the ICMA framework's primary organizing category for social bond impact.

A CROSS-compliant program within a social bond financing structure has these six fields documented at the entry specification gate before implementation begins. The ICMA reporting obligation, which arises annually after bond issuance, draws directly on the Field 1-6 data without requiring additional specification work. The indicator documentation is already done; the annual report draws on it and supplements it with actuals.

WALKRI's criterion intent and operational definition requirements strengthen Fields 2 and 3: the criterion intent field in WALKRI ensures that the purpose of the measurement is stated explicitly, and the operational definition requirement ensures that Field 2 is specific enough that two independent collectors would apply it consistently. These requirements address a recurring failure mode in social bond impact reporting: indicators whose definitions are ambiguous enough that year-over-year comparisons are unreliable even when the nominal indicator name is unchanged.

---

## Year-Over-Year Comparability: CROSS Disaggregation Ratchet

ICMA's year-over-year comparability requirement is one of the more operationally demanding elements of the framework. Comparability requires that the indicator, its definition, its unit, and its population scope remain stable across reporting cycles. It also requires that disaggregation be applied consistently: a report that disaggregates by gender in year two but not year one is not comparable, even if the aggregate numbers are both present.

CROSS's disaggregation ratchet is the mechanism that enforces this consistency. Once a disaggregation dimension is introduced in an indicator's Field 8 specification, it cannot be removed in subsequent reporting cycles without a formal gate record of the change and its rationale. This ratchet prevents the common reporting practice of introducing favorable disaggregations in good performance years and quietly dropping them in poor performance years. For ICMA compliance, the ratchet ensures that disaggregation applied in the first annual report persists in all subsequent reports, satisfying the framework's consistency requirement structurally.

The ratchet also prevents definition drift: changes to Fields 1 through 6 during implementation require a gate record, which is a formal documentation event rather than a quiet edit. ICMA-aligned programs that use CROSS produce a version history of their indicator specifications, enabling investors to assess whether changes occurred and what their rationale was.

---

## CROSS as ICMA Impact Report Data Source

A program within a social bond financing structure that uses CROSS for its grant cycle management produces, as a by-product of gate compliance, the data that the ICMA annual impact report requires. Gate evidence records contain actuals against pre-specified indicators; the compliance threshold records contain pass/fail assessments against Field 11; the ToC architecture contains the causal logic connecting use of proceeds to social outcomes.

The ICMA annual impact report for a social bond draws on these records directly. The issuer does not need a separate measurement and reporting system for ICMA compliance; CROSS gate records, combined with Field 1-6 indicator documentation, are sufficient to populate the ICMA template. Programs should review ICMA's current sector-specific indicator guidance (available through the ICMA Social Bond Principles secretariat) to confirm that their Field 2 definitions align with recommended indicator wordings for their use-of-proceeds category.

---

## Structural Mapping Table

| ICMA Requirement | CROSS Provision | WALKRI Provision | Coverage |
| :-- | :-- | :-- | :-- |
| Indicator name and definition | Fields 1-2 | Criterion intent and operational definition requirements | Structural: full indicator documentation at entry gate |
| Unit of measurement | Field 3 | Response form requirement (ensures unit matches collection method) | Structural |
| Baseline and target | Fields 4-5 | No direct provision | Structural |
| Target population scope | Field 6 | No direct provision | Structural |
| Year-over-year comparability | Disaggregation ratchet (Field 8); version-controlled indicator specification | No direct provision | Structural: ratchet prevents disaggregation drift across reporting cycles |
| Measurement methodology | Collection methodology (Field 9) | Evidence form and compliance threshold requirements | Structural: methodology documented in indicator specification |
| Annual impact reporting | Gate evidence records as primary data source for ICMA template | No direct provision | Structural: gate records satisfy annual reporting data requirements |

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

ICMA Harmonised Framework for Impact Reporting for Social Bonds: https://www.icmagroup.org/sustainable-finance/impact-reporting/

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. Fields 1-6 mapping, disaggregation ratchet, and CROSS-as-data-source claims documented. WALKRI criterion intent and operational definition contributions analyzed. |
