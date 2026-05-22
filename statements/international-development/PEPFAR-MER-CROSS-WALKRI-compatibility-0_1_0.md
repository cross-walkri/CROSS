---
title: PEPFAR Monitoring, Evaluation, and Reporting (MER) System Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.4 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - https://www.state.gov/wp-content/uploads/2025/01/FY25-MER-v2.8-Indicator-Reference-Guide_508-Compliant.pdf
  - https://help.datim.org/hc/en-us/articles/360000084446-MER-Indicator-Reference-Guides
---

# PEPFAR Monitoring, Evaluation, and Reporting (MER) System

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

The PEPFAR Monitoring, Evaluation, and Reporting (MER) system defines the mandatory HIV/AIDS indicator set and reporting obligations for all PEPFAR-funded implementing partners across 50+ country programs totaling approximately $7 billion per year. CROSS satisfies MER's indicator documentation requirements through its eleven-field indicator specification and enforces the cascade logic that structures MER reporting through its Theory of Change hierarchy. WALKRI ensures that every intake field collecting MER-required disaggregation data functions as a measurement instrument, making operational definitions explicit before any application is submitted.

---

## The PEPFAR MER System's Approach

The MER system governs how all implementing partners collect, report, and submit program data into DATIM (Data for Accountability, Transparency, and Impact), the U.S. government's centralized data platform for PEPFAR. The MER Indicator Reference Guide (v2.8, FY25, January 2025; state.gov) defines the complete required indicator set, the disaggregation categories that must accompany each indicator, and the reporting cycles to which all partners are bound. MER is a system-level standard: it does not govern how individual programs are designed internally, but it does require that any program funded under PEPFAR produces verifiable data against a defined indicator set in a defined format.

The organizing logic of MER is the HIV/AIDS cascade, structured around the 95/95/95 targets: 95% of people living with HIV (PLHIV) know their status; 95% of those who know their status are on treatment; 95% of those on treatment achieve viral suppression. This cascade is not merely aspirational. It is the structural backbone around which all MER indicators are organized. Prevention indicators feed the front of the cascade; testing indicators capture the first 95; treatment indicators capture the second; viral load and viral suppression indicators capture the third. Orphans and vulnerable children (OVC) programming is tracked through a parallel indicator set. Results for each indicator must be disaggregated by age, sex, and key population type (men who have sex with men, people who inject drugs, sex workers, transgender people, and prisoners, depending on context and country).

The disaggregation requirements in MER are mandatory, not optional. An implementing partner cannot report an aggregate figure without the underlying breakdowns. This means that every program, before it begins data collection, must have operational definitions for each disaggregation category, data collection instruments capable of capturing the required breakdowns, and processes for submitting disaggregated data to DATIM on the required schedule. DATIM itself maintains an audit trail of submissions, corrections, and validations.

MER is distinct from PEPFAR SIMS (Site Improvement Through Monitoring System), which is a site-level quality assurance process. It is also distinct from USAID's Program Indicator Reference Sheet (PIRS), which defines indicators one at a time for individual projects. MER defines a system of indicators that together describe the entire HIV/AIDS response, and every funded partner's data becomes part of that system.

---

## How CROSS Satisfies the MER System

CROSS satisfies MER's indicator documentation requirements through its eleven-field indicator specification structure (Fields 1 through 5: indicator name, operational definition, unit of measurement, baseline value, and target value), which maps directly to the documentation components required for each MER indicator. The remaining fields in the CROSS indicator specification address data source, data collection method, disaggregation categories, reporting frequency, responsible party, and verification method, all of which have direct counterparts in MER indicator documentation requirements.

The MER cascade architecture (prevention, testing, treatment, viral suppression) corresponds to the CROSS Theory of Change output-outcome-goal hierarchy. In CROSS, programs are required to specify their Theory of Change before any application opens: what outputs the program will produce, what intermediate outcomes those outputs are expected to achieve, and how those outcomes contribute to the program's goal. Under MER, each step in the HIV/AIDS cascade is a measurable intermediate outcome. A CROSS-compliant program operating in a PEPFAR context would declare the relevant cascade steps as its intermediate outcomes at the entry gate, making the cascade logic explicit before any implementing partner submits an application.

The CROSS disaggregation ratchet provides a structural enforcement mechanism for MER's disaggregation requirements. Once age, sex, and key population disaggregation categories are established at the entry gate for a given reporting period, the ratchet prohibits those categories from being dropped in subsequent reporting periods. This prevents the gradual erosion of disaggregation quality that MER's audit trail is designed to detect. Partners cannot simply stop reporting on key population disaggregation because collection proves difficult; the ratchet records the commitment and holds it.

The CROSS Attestation Corpus retains gate records that correspond to the audit trail DATIM maintains. Where DATIM records submissions and corrections at the platform level, the CROSS Attestation Corpus holds the pre-commitment records: what indicators were specified, what disaggregation categories were declared, and what baselines and targets were established before implementation began. Together, these two record systems provide a complete audit trail from design intent through to reported results.

| MER Requirement | CROSS Mechanism |
|---|---|
| Indicator name, definition, unit | CROSS Fields 1-3 (indicator specification) |
| Baseline and target values | CROSS Fields 4-5 (indicator specification) |
| Disaggregation by age, sex, key population | CROSS disaggregation ratchet (entry gate) |
| Cascade structure (prevention-testing-treatment-suppression) | CROSS Theory of Change output-outcome-goal hierarchy |
| DATIM audit trail | CROSS Attestation Corpus (gate records) |
| Fixed reporting cycle submission | CROSS progress and completion gate sequence |

---

## How WALKRI Complements This Alignment

WALKRI ensures that every intake field used to collect MER-required disaggregation data functions as a measurement instrument with explicit operational definitions, not as a free-text response field. In a PEPFAR context, this means that the intake fields for key population typologies must specify exactly which classifications qualify under each category (for example, what documentary or behavioral evidence establishes that a beneficiary falls within a given key population type), what age bands are used and how they are verified, and what evidence is required for sex disaggregation. WALKRI does not allow a form to ask "What is the beneficiary's key population status?" without an accompanying operational definition specifying what counts as a valid answer.

This is consequential because MER's disaggregation requirements create a downstream compliance obligation: data submitted to DATIM that cannot be traced back to operationally defined intake instruments is vulnerable to audit findings. WALKRI closes this gap by requiring that the operational definitions be established at the intake design stage, before any data collection begins, making MER disaggregation traceable from submission back to the original instrument design.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
