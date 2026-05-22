---
title: OECD DAC CRS Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - OECD DAC Creditor Reporting System (CRS), https://www.oecd.org/en/data/insights/data-explainers/2024/10/resources-for-reporting-development-finance-statistics.html
  - IATI Standard v2.03, iatistandard.org
  - CROSS+WALKRI IATI Compatibility Statement v0.1.0
---

# OECD DAC CRS Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

CROSS produces CRS-compatible programmatic metadata structurally. The OECD DAC Creditor Reporting System (CRS) is a statistical reporting framework that all 30-plus bilateral DAC donor countries use to track development finance flows. CRS mandatory fields divide into two categories relative to CROSS scope: programmatic metadata, which CROSS governs and produces, and financial flow data, which CROSS intentionally does not govern.

This statement addresses CRS specifically, not OECD DAC Evaluation Criteria. The DAC Evaluation Criteria (relevance, coherence, effectiveness, efficiency, impact, sustainability) are covered separately. CRS is a statistical reporting obligation about development finance transactions; its compatibility with CROSS rests on the structural overlap between CRS programmatic fields and CROSS's obligation architecture.

A secondary compatibility pathway follows from IATI alignment. Because IATI v2.03 produces CRS-compatible output by design, and because CROSS's IATI compatibility is separately documented, CRS compatibility follows from IATI alignment for programs that have implemented CROSS under that pathway.

---

## What CRS Requires

The CRS collects standardized data on official development assistance and other resource flows from DAC donor countries. Mandatory CRS fields for each reported activity:

1. Reporting country
2. Donor agency code
3. CRS ID
4. Recipient country or region code
5. Sector code (five-digit OECD code list, 60-plus categories)
6. Channel code (bilateral, multilateral, NGO, PPP, or other)
7. Aid type code
8. Flow type
9. Finance type
10. Commitment amount
11. Disbursement amount
12. Project title
13. Project description
14. Expected start date
15. Expected end date

CRS compliance is required for sub-recipient reporting in USAID and FCDO programs. CRS and IATI are bridged by design: IATI v2.03 produces CRS-compatible output, enabling organizations that report to IATI to satisfy CRS requirements through a single reporting workflow.

---

## Layer Distinction: Programmatic vs. Financial Flow

CRS mandatory fields fall into two categories relative to CROSS scope.

Programmatic fields (inside CROSS scope) describe the funded activity: what it is, where it operates, what sector it addresses, and over what timeframe. CROSS governs obligation architecture and indicator specification at this level. Fields in this category: project title, project description, recipient country or region code, sector code, expected start date, expected end date, channel code.

Financial flow and statistical fields (outside CROSS scope) record the transaction, the funding relationship, and the amounts committed and disbursed. These are statistical inputs for DAC aggregate reporting and are managed by the donor agency's financial systems rather than by the recipient program. Fields in this category: reporting country, donor agency code, CRS ID, aid type code, flow type, finance type, commitment amount, disbursement amount.

---

## CRS Field Mapping

| CRS Mandatory Field | CROSS/WALKRI Field | Notes |
| :-- | :-- | :-- |
| Project title | Organizational identity (on-chain identity anchor) | CROSS requires a canonical program name as part of the on-chain identity anchor. Direct correspondence. |
| Project description | Theory of Change declaration, Goal and Outcome levels | CROSS's program-level ToC produces a structured program description that exceeds the narrative depth of a standard CRS project description. The Goal level corresponds to the CRS project description requirement. |
| Recipient country or region code | Population field (Indicator Field 6) | CROSS Field 6 specifies the geographic scope of measurement for each indicator. At the program level, the declared population produces the recipient country or region documentation CRS requires. |
| Sector code | Institutional alignment (Indicator Field 10) | CROSS Field 10 (institutional framework alignment) captures the sectoral context of the program's intended outcomes. Programs that declare OECD DAC alignment in this field produce sector-level documentation that maps to CRS sector codes. |
| Channel code | Organizational identity (on-chain identity anchor) | The channel code identifies whether funding flows bilaterally, through multilateral institutions, through NGOs, or through public-private partnerships. CROSS's on-chain identity anchor captures the organizational type and funding relationship. |
| Expected start date | Gate configuration (activation gate) | CROSS's activation gate documents when program obligations take effect. This corresponds to the CRS expected start date. |
| Expected end date | Gate configuration (continuation gate) | CROSS's continuation gate documents when the obligation cycle closes. This corresponds to the CRS expected end date. |
| Reporting country | No CROSS equivalent | Statistical identifier for the DAC donor country. Managed by the donor agency's financial systems. Outside CROSS scope. |
| Donor agency code | No CROSS equivalent | Statistical identifier for the reporting agency within the donor country. Outside CROSS scope. |
| CRS ID | No CROSS equivalent | Unique transaction identifier assigned by the CRS system. Transactional metadata. Outside CROSS scope. |
| Aid type code | No CROSS equivalent | Classification of the modality of aid (project aid, budget support, technical assistance, etc.). Statistical metadata. Outside CROSS scope. |
| Flow type | No CROSS equivalent | ODA, OOF, private flows, or other. Statistical classification. Outside CROSS scope. |
| Finance type | No CROSS equivalent | Grant, loan, equity, guarantee, or other. Financial transaction data. Outside CROSS scope. |
| Commitment amount | No CROSS equivalent | Financial transaction data. Outside CROSS scope. |
| Disbursement amount | No CROSS equivalent | Financial transaction data. Outside CROSS scope. |

**Result:** Seven of the fifteen CRS mandatory fields have direct or functional CROSS equivalents. The remaining eight are financial flow and statistical fields that CROSS does not govern. A CRS-reporting program using CROSS produces the programmatic fields of CRS compliance through its standard obligation architecture.

---

## The IATI Bridge

IATI v2.03 was designed to produce CRS-compatible output. The IATI standard includes a CRS++ extension that maps IATI fields to CRS mandatory fields directly. DAC donor countries including USAID, FCDO, and the Netherlands have endorsed IATI as the preferred reporting pathway for CRS-compliant sub-recipient reporting.

CROSS's IATI compatibility is separately documented in the CROSS+WALKRI IATI Compatibility Statement. Programs that have implemented CROSS under the IATI alignment pathway produce CRS-compatible programmatic metadata through that pathway. The CRS compatibility established in this statement reinforces that existing alignment and covers programs that report to CRS directly without routing through IATI.

Programs that are already IATI-reporting under CROSS do not need to take additional steps to satisfy CRS programmatic field requirements. Their IATI reporting workflow produces CRS-compatible output as a structural consequence of the IATI/CRS bridge design.

---

## Sector Code Alignment

CRS sector codes are five-digit identifiers from OECD's DAC list of aid activities. The first three digits identify the sector (education, health, agriculture, economic infrastructure, etc.) and the last two digits identify the sub-sector. There are more than 60 sector categories.

CROSS Field 10 (institutional framework alignment) requires programs to declare the external standards and frameworks to which their indicators are aligned. Programs that declare specific OECD DAC sector references in this field produce sector documentation that maps to CRS sector codes. The declaration is not automatic; it requires the program to identify which CRS sector code applies to each indicator cluster.

Programs with multi-sector portfolios should declare sector codes at the indicator cluster level rather than at the program level, since CRS allows one sector code per reported activity and some programs cover multiple sectors. Disaggregating by sector in CROSS Field 10 preserves the granularity that CRS sector reporting requires.

---

## Adoption Guidance

Programs reporting to DAC donors through CRS that adopt CROSS+WALKRI should:

1. Declare the relevant CRS sector code in Indicator Field 10 (institutional framework alignment) for each indicator cluster. This produces the sector-level documentation CRS requires and makes the sector alignment explicit rather than inferred.

2. Use the program-level ToC declaration to produce the project description required by CRS. The Goal level corresponds to the CRS project description; the Outcome level produces the more detailed narrative that USAID and FCDO sub-recipient reports typically require.

3. Configure activation and continuation gates with explicit dates. These dates produce the expected start and end date documentation CRS mandates.

4. If the program already reports to IATI under the CROSS alignment pathway, no additional CRS-specific steps are required for the programmatic fields. The IATI workflow produces CRS-compatible output for those fields through the IATI/CRS bridge.

Programs reporting through CRS do not need to produce separate programmatic narrative documentation beyond what CROSS conformance produces. Financial flow fields are managed by the donor agency's grants management and financial reporting infrastructure.

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

OECD DAC CRS resources: https://www.oecd.org/en/data/insights/data-explainers/2024/10/resources-for-reporting-development-finance-statistics.html

IATI Standard v2.03: iatistandard.org

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. Fifteen CRS mandatory fields mapped against CROSS fields. Programmatic vs. financial flow layer distinction articulated. IATI bridge pathway documented. Sector code alignment guidance. Adoption guidance for DAC-reporting programs. |
