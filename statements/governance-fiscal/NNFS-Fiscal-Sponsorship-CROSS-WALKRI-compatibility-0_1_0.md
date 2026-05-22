---
title: NNFS Guidelines for Comprehensive Fiscal Sponsorship Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.3 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - https://www.fiscalsponsors.org/nnfs-guidelines
  - https://s3.amazonaws.com/nnfs/file_assets/d0758100838a/NNFS%20Guidelines%20for%20Comprehensive%20Fiscal%20Sponsorship.pdf
---

# NNFS Guidelines for Comprehensive Fiscal Sponsorship

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

The National Network of Fiscal Sponsors (NNFS; fiscalsponsors.org) publishes the primary professional guidelines for fiscal sponsorship in the United States. Its Guidelines for Comprehensive Fiscal Sponsorship establish requirements for project agreements, fund accounting, organizational oversight, financial audits, and ethics standards applied to hosted projects. CROSS+WALKRI satisfies these requirements structurally: the entry specification gate produces the written project agreement documentation NNFS requires, concurrent funding disclosure corresponds to the line-item fund accounting requirement, and the CROSS organizational identity fields accommodate the complex legal arrangements that fiscal sponsorship creates between sponsors, hosted projects, and funders.

---

## The NNFS Fiscal Sponsorship Framework

The National Network of Fiscal Sponsors publishes Guidelines for Comprehensive Fiscal Sponsorship and separate guidelines for Pre-Approved Grant Relationship Sponsorship, the two primary models of fiscal sponsorship in the United States. In Comprehensive Fiscal Sponsorship, a hosted project becomes a program of the fiscal sponsor with full legal and fiduciary integration: the fiscal sponsor is the legal entity of record, holds all funds, and bears full legal responsibility for the program. In Pre-Approved Grant Relationship Sponsorship, the sponsor exercises "variance power" over grant funds while the hosted project remains a separate legal entity.

The NNFS Guidelines for Comprehensive Fiscal Sponsorship establish several binding requirements for member organizations. Annual financial audits conducted in accordance with Generally Accepted Accounting Principles (GAAP) must be publicly available. All new sponsored projects must receive board-level approval before any funds are accepted. Written project agreements specifying scope and deliverables are required for every hosted project. Fund accounting must isolate each project's finances at the line-item budget level, with project-level financial isolation maintained throughout the grant period. Ethics standards applicable to the fiscal sponsor as an organization must be applied to all sponsored projects.

Fiscal sponsorship is a primary funding mechanism for unincorporated projects, emerging organizations, and early-stage initiatives that lack the legal infrastructure to receive grants directly. In the Web3, public goods, and DAOecosystem contexts where CROSS+WALKRI operates, fiscal sponsorship through Open Collective, Gitcoin Grants Stack, and similar platforms is not an edge case: it is one of the dominant structures through which grant funds flow to projects. Many Octant grantees, for example, operate through fiscal sponsorship arrangements of various kinds. CROSS+WALKRI must accommodate fiscal sponsorship structures rather than treating them as exceptional.

NNFS member organizations signal to funders and hosted projects that their fiscal sponsorship practices meet the published professional standard. For cohort 3 of the grants ecosystem (grant program operators), understanding how CROSS+WALKRI interacts with fiscal sponsorship is essential to correct implementation of the organizational identity and disbursement authority fields.

---

## How CROSS Satisfies the NNFS Framework

CROSS addresses the NNFS requirements through specific field groups and gate requirements that correspond to each published guideline. The table below maps each NNFS requirement to its CROSS mechanism.

| NNFS Requirement | CROSS Mechanism |
|---|---|
| Written project agreements specifying scope and deliverables | Entry specification gate: scope and deliverable specification published and independently verifiable before any grant disbursed. The gate record is the structured project agreement. |
| Line-item fund accounting at individual project level | Concurrent funding disclosure: all funders, funding amounts, purposes, and periods documented for the same program, corresponding to the line-item budget and fund isolation requirement. |
| Board-level approval of all new sponsored projects | CROSS organizational identity declaration: governance structure field documents whether a board-level approval mechanism exists and is operative for the hosted project. |
| Independent financial audits (publicly available) | CROSS Attestation Corpus: persistent, publicly accessible record of gate determinations and financial declarations. The Attestation Corpus does not replace a GAAP audit but provides the program-level documentation that audit processes draw on. |
| Ethics standards applied to all sponsored projects | CROSS Part VII conflict of interest provisions: applied at the program level regardless of whether the grantee is the fiscal sponsor, the hosted project, or a hybrid arrangement. |
| Pre-Approved Grant Relationship variance power | CROSS disbursement authority "governed" state: funds controlled by a governance mechanism rather than an individual authority. This accommodates the variance power structure where the sponsor exercises formal control but the project directs operations. |

The project agreement mapping is the most direct. NNFS requires that written project agreements specify scope and deliverables for every hosted project. CROSS's entry specification gate requires that scope and deliverables be documented in a structured, independently verifiable format before any funds are disbursed. The gate record satisfies the NNFS requirement for a written project agreement while adding the additional structural rigor of being machine-readable, timestamped, and included in the Attestation Corpus.

The fund accounting mapping addresses one of the most operationally demanding NNFS requirements. Fund accounting at the individual project level requires that each hosted project's finances be isolated from both the fiscal sponsor's general funds and the funds of other hosted projects. CROSS's concurrent funding disclosure documents all funders, funding amounts, purposes, and periods for a single program, producing exactly the data structure that project-level fund isolation requires. A fiscal sponsor implementing CROSS+WALKRI-conformant programs for all hosted projects has the documentation needed to demonstrate fund isolation for each project individually.

The organizational identity fields require careful implementation in fiscal sponsorship contexts. CROSS Field 6 (on-chain identity anchor) accommodates the wallet addresses associated with fiscal sponsorship arrangements, including multisig wallets where the fiscal sponsor and the hosted project team both hold signing authority. The disbursement authority field distinguishes between: funds controlled by the fiscal sponsor as an organization, funds controlled by the hosted project team directly, and funds controlled by a governance mechanism that includes both parties. These distinctions correspond directly to the difference between Comprehensive Fiscal Sponsorship and Pre-Approved Grant Relationship Sponsorship.

---

## How WALKRI Complements This Alignment

WALKRI's pre-publication audit requirement addresses the written project agreement requirement from the intake side. NNFS requires that written project agreements specify scope and deliverables. WALKRI requires that intake forms collecting scope and deliverable information specify, at the field level, what constitutes evidence of scope completion and how deliverable achievement will be measured.

The connection is structural. A written project agreement that specifies deliverables in prose without defining what evidence would demonstrate completion does not satisfy the NNFS requirement in any operationally useful sense: the agreement exists, but no one can determine whether the deliverables have been met without an interpretive judgment call at closeout. WALKRI closes this gap by requiring that the intake fields collecting scope and deliverable information function as measurement instruments: each field specifies the defined term, unit, baseline, evidence access path, and population before any hosted project responds.

For fiscal sponsorship arrangements specifically, this matters because the fiscal sponsor typically bears full legal responsibility for the hosted project's performance under Comprehensive Fiscal Sponsorship. A WALKRI-conformant project agreement gives the fiscal sponsor board the documentation it needs to exercise meaningful oversight: the deliverables are specified precisely enough that board-level approval of a new project means something, and board-level monitoring of an existing project is based on defined indicators rather than narrative self-report.

In the Web3 and public goods context, where fiscal sponsorship through platforms like Open Collective operates at scale and often without individual written agreements for each small-scale grant, WALKRI conformance provides the field-level precision that substitutes for the detailed written agreements that NNFS guidelines contemplate. The form architecture does the work that a bespoke legal agreement would do in a traditional fiscal sponsorship context.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
