---
title: National Lottery Community Fund and Lottery-Funded Grantmaking Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.2 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - https://www.tnlcommunityfund.org.uk/media/insights/documents/Understanding-Thriving-Communities.pdf
  - https://communityimpacthub.wa.gov.au/media/wbjgexnl/grn214_grant-impact-guides_v7_single-pages.pdf
  - https://otf.ca/our-grants/grant-investment-framework
  - https://www.toteboard.gov.sg/impact/impact-measurement/
  - https://www.communitymatters.govt.nz/lottery-outcomes-framework
---

# National Lottery Community Fund and Lottery-Funded Grantmaking

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

Lottery-funded grantmaking is a global category of public charitable funding with distinct accountability characteristics: funds derive from public gambling revenues, are held by statutory or quasi-governmental bodies, and are deployed through grant programs subject to public accountability requirements. The National Lottery Community Fund (NLCF, formerly Big Lottery Fund; UK) is the largest single body in this category, distributing National Lottery proceeds through its "Thriving Communities" outcomes framework (2018). Major lottery bodies with published measurement frameworks include Lotterywest (Western Australia), Ontario Trillium Foundation (Canada), Singapore Tote Board, and New Zealand Lottery Grants Board. CROSS+WALKRI satisfies the measurement, reporting, and accountability requirements of lottery-funded grantmaking across these frameworks.

---

## The Lottery-Funded Grantmaking Frameworks' Approach

The NLCF Thriving Communities framework organizes grantmaking around four missions: Communities Come Together; Communities Help Children and Young People Thrive; Communities Are Healthier; and Communities Are Environmentally Sustainable. These missions function as goal areas within which grantees declare their intended contributions and against which NLCF measures portfolio-level progress. Grantees receiving over 20,000 GBP for projects lasting two or more years submit annual progress and learning reports documenting achievement against stated outcomes. NLCF publishes grant data to the 360Giving Data Standard, which specifies how grant information should be structured for public transparency and cross-funder comparability.

NLCF's evidence guidance is deliberately flexible: grantees may use qualitative or quantitative evidence, and the choice of evidence modality is the grantee's to make based on what is appropriate for the project's nature and scale. This flexibility reflects an explicit policy decision to reduce grantee reporting burden while maintaining the substance of accountability: NLCF requires evidence that outcomes were achieved, not evidence produced in a particular form.

Lotterywest (Western Australia) publishes a Grant Impact Guide requiring grantees to use a logic model structure connecting inputs to activities to outputs to outcomes. The guide provides practical tools for constructing and validating logic models and for selecting appropriate outcome indicators. Ontario Trillium Foundation (OTF) operates a Grant Investment Framework tied to the Canadian Index of Wellbeing (CIW), using CIW indicator domains to anchor grantee outcome measurement to a validated national benchmark. Singapore Tote Board co-developed an Impact Measurement Framework with the National Volunteer and Philanthropy Centre, providing a public guidebook for grantees on outcome measurement with explicit guidance on qualitative and quantitative methods.

New Zealand Lottery Grants Board (NZLGB), operating under the Community Matters programme from July 2025, uses a Lottery Outcomes Framework with three strategic outcomes covering community wellbeing, participation, and resilience. The NZLGB framework specifies that outcomes evidence should be proportionate to project scale, distinguishing between small community projects and larger strategic grants in the evidence burden it places on grantees.

Across these bodies, several structural requirements recur: grantees must specify intended outcomes before receiving funding; progress must be reported against stated outcomes; evidence must support the outcome claims made; and measurement must be proportionate to program scale. These are the accountability requirements CROSS+WALKRI is designed to satisfy.

---

## How CROSS Satisfies Lottery-Funded Grantmaking Frameworks

CROSS satisfies the outcome specification, progress reporting, and evidence accountability requirements of lottery-funded grantmaking through its gate architecture and indicator specification system.

The NLCF four Thriving Communities missions function as goal-level declarations in CROSS terms. A grantee applying through an NLCF-aligned CROSS program declares at intake which mission their work contributes to, specifies the outcome indicators they will use to measure that contribution, and documents their Theory of Change connecting activities to outcomes to the mission goal. This is the CROSS Theory of Change hierarchy: activities produce outputs, outputs contribute to outcomes, outcomes contribute to goals. When NLCF's mission is the declared goal, the entire CROSS indicator specification structure is anchored to that goal-level accountability.

NLCF's annual progress and learning reports correspond to CROSS's progress verification gate records. At each gate, the grantee documents progress against the outcome indicators specified at intake, using whatever evidence form the NLCF evidence guidance permits (qualitative or quantitative). The gate record is structured documentation: it references the pre-committed specification, records what was achieved against what was stated, and preserves the determination rationale. This is more structured than NLCF's current progress report format, but it satisfies all the same accountability requirements while adding the independently verifiable pre-commitment that CROSS provides.

NLCF's evidence flexibility (grantee choice of qualitative or quantitative evidence) maps to CROSS's evidence form classification. CROSS classifies evidence by scope and strength but does not prescribe evidence modality. A grantee may submit qualitative evidence (case studies, interview summaries, observational documentation) or quantitative evidence (survey data, administrative records, tracked metrics); the WALKRI specification ensures that what type of evidence is expected is clear before submission, without constraining which modality is appropriate.

Lotterywest's Grant Impact Guide logic model requirement (inputs-activities-outputs-outcomes) maps directly to CROSS's Theory of Change hierarchy. CROSS's activities-output-outcome-goal structure is the same logical chain that Lotterywest specifies; a grantee constructing a CROSS Theory of Change is simultaneously constructing a Lotterywest-conformant logic model. No additional documentation is required to satisfy both frameworks simultaneously.

OTF's Canadian Index of Wellbeing indicator domains provide a validated reference set from which grantees may draw outcome indicators. CROSS's eleven-field indicator specification (Fields 1 through 5: name, definition, unit, baseline, target) is directly compatible with CIW indicators: a CIW indicator has a defined name, a published operational definition, a specified unit of measurement, a national baseline value from CIW data, and a target value the grantee sets relative to that baseline. A grantee using a CIW indicator in a CROSS program fills all five fields from the CIW documentation, producing a fully specified CROSS indicator without additional measurement design work.

NZLGB's proportionality requirement (evidence proportionate to project scale) maps to CROSS's proportionality principle, which scales evidence requirements to program type, obligation mode, and gate stage. Small community projects are not required to produce the same evidentiary record as large multi-year strategic grants; this is built into CROSS's gate architecture rather than left to program officer discretion.

| Lottery Framework Requirement | CROSS Provision |
|---|---|
| Outcome specification before funding | Entry gate intake, Theory of Change, indicator Fields 1-5 |
| Progress reporting against stated outcomes | Progress verification gate records |
| Evidence flexibility (qualitative or quantitative) | Evidence form classification without modality prescription |
| Logic model (Lotterywest) | CROSS Theory of Change hierarchy (activities-output-outcome-goal) |
| Validated indicator domains (OTF/CIW) | Eleven-field indicator specification compatible with CIW |
| Proportionate evidence burden (NZLGB) | Proportionality principle (evidence scales to program type) |
| Public transparency (360Giving) | Attestation Corpus (persistent, queryable, publishable) |

---

## How WALKRI Complements This Alignment

WALKRI ensures that intake forms in lottery-funded grantmaking programs specify each field as a measurement instrument before any grantee engages. For NLCF programs publishing data to the 360Giving Data Standard, this matters because 360Giving requires structured, field-by-field grant data whose fields have consistent operational meanings. A WALKRI-conformant intake form produces data that maps cleanly to 360Giving fields because each field's measurement purpose was specified before publication.

WALKRI also addresses a specific risk in lottery-funded programs with flexible evidence guidance: without field-level operational definitions, grantees may interpret outcome fields as asking for aspirational statements rather than measurement commitments. WALKRI's audit procedure identifies fields that would produce this ambiguity and requires resolution before publication. The result is that grantees understand they are committing to measurement, not just to aspiration, which is what lottery accountability bodies require from their progress and learning reports.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
