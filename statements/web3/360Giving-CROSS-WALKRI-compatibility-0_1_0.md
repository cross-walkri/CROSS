---
title: 360Giving Data Standard Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.2 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - https://standard.threesixtygiving.org/en/latest/
  - https://www.360giving.org/about/data-standard/
---

# 360Giving Data Standard Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

360Giving is a UK charity publishing an open data standard for grant transparency, accepted by over 200 UK funders including Esmee Fairbairn, Nuffield Foundation, Joseph Rowntree Foundation, and the National Lottery Community Fund. Its ten required fields establish the minimum data infrastructure for grant transparency publication. CROSS covers all ten required 360Giving fields as a strict superset; programs using CROSS can generate 360Giving-compliant records as a byproduct of standard gate operations. WALKRI ensures that the grant data published to 360Giving meets the measurement quality standards that 360Giving's optional recommended fields also anticipate.

360Giving represents the UK sector's most widely adopted open data infrastructure for grant-making. Compatibility with the 360Giving standard means that CROSS-conformant funders in the UK context are not required to maintain a separate data pipeline for transparency publication; their CROSS obligation records, properly formatted, satisfy the standard's requirements directly.

---

## The 360Giving Data Standard

The 360Giving standard is published as a JSON Schema with accepted spreadsheet publication formats. Its ten required fields are the minimum necessary for a grant record to be accepted by the 360Giving Data Registry and available through GrantNav, the sector's public grant discovery tool.

The ten required fields are:

1. Identifier: a unique identifier for the grant record.
2. Title: a short title describing the grant or project.
3. Description: a longer description of the purpose and activities.
4. Currency: the currency in which the grant is denominated.
5. Amount Disbursed: the actual amount paid out.
6. Amount Applied For: the amount originally requested by the applicant.
7. Award Date: the date on which the grant was awarded.
8. Planned Dates: start and end dates for the funded activity.
9. Recipient Organization: structured data identifying the receiving organization (name, identifier, address).
10. Funding Organization: structured data identifying the funding organization (name, identifier).

Beyond these ten required fields, 360Giving maintains a set of recommended and optional fields for impact measurement, evaluation, and geographic data. These optional fields anticipate measurement practices that CROSS and WALKRI formalize at the specification layer.

---

## How CROSS Satisfies the 360Giving Standard

CROSS covers all ten required 360Giving fields as structural consequences of gate conformance. No additional fields need to be populated or collected; they are produced by CROSS's entry specification and obligation architecture.

| 360Giving Required Field | CROSS Provision | Notes |
| :-- | :-- | :-- |
| Identifier | Organizational identity anchor (CROSS obligation record identifier) | CROSS requires a persistent identifier for each obligation record. This identifier is the 360Giving grant identifier. |
| Title | Program name field at entry specification gate | CROSS requires a named program or round declaration at entry. This is the grant title. |
| Description | Population scope declaration plus activity scope declaration | CROSS Fields 6 and the activity level of the ToC hierarchy together constitute the grant description: what is being funded, for whom, through what activities. |
| Currency | Concurrent funding disclosure: currency field in the financial transparency dimension | CROSS's financial transparency obligation dimension requires currency declaration as part of the funding relationship record. |
| Amount Disbursed | Milestone gate records: amounts released at each gate | CROSS gate records track disbursement against milestone completion. Amount disbursed is the sum of gate-authorised releases. |
| Amount Applied For | Entry specification gate: requested amount field in the obligation record | CROSS's entry specification requires the applied-for amount as a precondition for activation gate passage. |
| Award Date | Activation gate timestamp | CROSS's gate architecture records timestamps at each gate. The activation gate timestamp is the award date. |
| Planned Dates | Gate configuration: entry and completion gate target dates declared at program activation | CROSS requires planned start and end dates as gate configuration inputs at the entry specification stage. |
| Recipient Organization | Organizational identity fields: legal name, jurisdiction, registration number, address | CROSS requires a structured organizational identity record for the receiving organization as part of the obligation record. This record maps directly to 360Giving's Recipient Organization fields. |
| Funding Organization | Funder-side entry specification fields: funder identity declaration in the program record | CROSS requires the funding organization's identity to be declared in the program-level specification. This maps directly to 360Giving's Funding Organization fields. |

**Result:** CROSS is a strict superset of the 360Giving required fields. Every piece of data 360Giving requires is produced by CROSS's standard gate operations. Programs using CROSS do not need a separate 360Giving data collection process; they need a formatting step to export CROSS obligation records into the 360Giving JSON Schema or spreadsheet format.

---

## CROSS Extensions Beyond 360Giving Scope

CROSS adds substantial structure beyond the 360Giving required fields. The additional CROSS fields, including eleven-field indicator specifications, causality stance declarations, coherence disclosures, independent attestation pathways, and ToC pathway registries, are outside the scope of 360Giving's current required field set. They are, however, consistent with the spirit of 360Giving's optional and recommended fields.

360Giving's optional fields include outcome indicators, evaluation reports, and geographic targeting data. CROSS's indicator specification (Fields 6-11), Theory of Change hierarchy, and continuation gate sustainability stance produce data that populates these optional fields. Funders seeking to publish maximum transparency data through 360Giving, beyond the required minimum, can draw on CROSS gate records to populate the full range of optional fields without additional collection effort.

This means CROSS-conformant programs have a pathway to publishing not only 360Giving-compliant records but 360Giving records that are richer than the sector average, because CROSS requires specification of data that most funders collect informally or not at all.

---

## How WALKRI Complements This Alignment

WALKRI's role in the 360Giving context is not about satisfying the standard's required fields; those are covered by CROSS alone. WALKRI's value is at the quality layer. 360Giving's optional recommended fields for outcomes and evaluation implicitly assume that the underlying measurement instruments are well-designed, but the standard does not specify what well-designed means at the instrument level. WALKRI fills that gap.

When a funder publishes outcomes data to 360Giving, that data is only as good as the instruments that collected it. WALKRI's pre-publication audit, applied before the entry specification gate opens, ensures that the outcome indicators and evidence forms behind the published data meet the same quality standards that WALKRI applies across all CROSS-conformant programs. The result is that 360Giving records produced by CROSS+WALKRI programs carry implicit quality assurance that the sector's current transparency practices do not provide. Grant data published in this way is not only transparent; it is methodologically defensible.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

360Giving Data Standard: https://standard.threesixtygiving.org/en/latest/

360Giving About: https://www.360giving.org/about/data-standard/

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. All ten 360Giving required fields mapped to CROSS provisions. CROSS-as-strict-superset argument stated and documented. Pathway to optional field population via CROSS gate records described. WALKRI quality role in outcomes data publication explained. |
