---
title: OECD Guidelines for Citizen Participation Processes (2022) Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.2 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - https://oecd.org/gov/open-government/oecd-guidelines-for-citizen-participation-processes-f765caf6-en.htm
  - https://www.oecd.org/tax/federalism/participatory-budgeting-note.pdf
---

# OECD Guidelines for Citizen Participation Processes (2022)

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

The OECD published "Guidelines for Citizen Participation Processes" in 2022 (OECD Publishing, DOI 10.1787/f765caf6-en), covering eight methods of citizen participation in public resource allocation, including participatory budgeting, deliberative processes, civic monitoring, and open innovation. These guidelines are formally distinct from OECD DAC evaluation criteria: they apply to participatory processes at the level of public institutions, municipalities, and community organizations rather than to development cooperation contexts. CROSS+WALKRI satisfies the guidelines' requirements for transparency, pre-specification of criteria, outcome reporting, and equity tracking through a set of structural provisions that make compliance independently verifiable rather than self-reported.

---

## The OECD Guidelines' Approach

The 2022 guidelines reflect a decade of growth in citizen participation as a recognized governance modality. Participatory budgeting alone has expanded from a few hundred implementations in the early 2000s to more than twelve thousand implementations globally, spanning municipal governments, school boards, housing authorities, and community organizations. As participation has scaled, so has the demand for accountability standards that distinguish genuine participation, in which citizen input shapes resource allocation outcomes, from consultative exercises that produce the appearance of participation without altering decisions.

The guidelines address this distinction through a set of requirements that apply across all eight participation methods. Participation processes must be transparent: the rules governing the process, including eligibility to participate, criteria for resource allocation, and procedures for counting or weighing citizen input, must be accessible to participants before they engage. Criteria for resource allocation must be specified before participants engage, not established or refined after citizen input reveals what participants prefer. Outcomes must be reported against stated objectives, using the criteria and metrics that were declared at the process's outset. Inclusion and equity must be tracked: disaggregated data on who participates and whose preferences are reflected in final allocations is required to assess whether the process has served the whole community or has systematically advantaged more resourced participants.

A significant feature of the guidelines is their explicit treatment of both prospective and retrospective participation processes. In prospective processes, citizens propose and vote on future uses of funds. In retrospective processes, citizens evaluate and allocate resources to work already completed. The latter model has become increasingly prominent in both civic contexts and in Web3 funding mechanisms; the guidelines recognize its distinct accountability requirements without treating it as a second-class participation form.

The guidelines also specify reporting obligations at the process level, not only at the funder or administrator level. Participants and the broader public should be able to review how the process was conducted, whether its stated criteria were applied, and what outcomes resulted. This creates an accountability loop that closes the gap between process design and process outcomes.

---

## How CROSS Satisfies the OECD Guidelines

CROSS was designed with participatory funding processes explicitly in scope, and its structural provisions map directly to the guidelines' requirements.

The requirement that criteria for resource allocation be specified before participants engage is addressed by CROSS's entry specification gate and round specification pre-commitment. Before any application window opens, the round specification must be published: it defines eligibility, evaluation criteria, gate definitions, evidence requirements, and the population scope of the program. This specification is independently verifiable; it exists as a published record before any participant engages, which is the condition the guidelines specify. The pre-commitment requirement prevents the retrospective adjustment of criteria after participation reveals participant preferences, which the guidelines identify as a failure mode of genuine participation.

The requirement that outcomes be reported against stated objectives maps to CROSS's gate record publication. At each gate, the determination is documented against the pre-committed specification. What was stated as the objective, what evidence was reviewed, and what determination was reached are all recorded and available. Because the gate record references the pre-committed specification, the connection between stated objective and reported outcome is traceable without requiring the reviewing body to reconstruct that connection from separate documents.

The inclusion and equity tracking requirement maps to CROSS's population scope declaration and disaggregation ratchet. Once demographic categories are defined as within scope for a participation process, the ratchet provision ensures those categories cannot be dropped in subsequent rounds. Longitudinal equity tracking, which the guidelines identify as essential for evaluating whether participation processes have been genuinely inclusive over time, is structurally guaranteed rather than dependent on each round's program officers maintaining the practice voluntarily.

The transparency requirement maps to CROSS's Attestation Corpus: a persistent record of gate determinations, pre-committed specifications, and organizational identity claims that supports public accountability over time. The Corpus is designed to persist across rounds and across program cycles, which is the accountability horizon the OECD guidelines specify for ongoing participation processes.

CROSS's Retroactive obligation mode is particularly compatible with the retrospective participation processes the guidelines explicitly recognize. In Retroactive mode, CROSS programs specify evaluation criteria for work already completed, using a pre-committed specification that participants can verify before submitting for evaluation. This is the structural form of the retrospective accountability the guidelines describe; it applies to Optimism Retro Funding, Octant's epoch-based grantmaking, and similar Web3 mechanisms that retrospectively allocate resources to demonstrated contributions.

| OECD Guideline Requirement | CROSS Provision |
|---|---|
| Criteria specified before participation begins | Entry specification gate + pre-commitment |
| Outcomes reported against stated objectives | Gate record publication |
| Inclusion and equity tracked longitudinally | Population scope declaration + disaggregation ratchet |
| Transparency requirement | Attestation Corpus |
| Retrospective process accountability | Retroactive obligation mode |

---

## How WALKRI Complements This Alignment

WALKRI ensures that the intake fields through which citizen participants engage with a participation process are measurement instruments rather than administrative forms. For OECD-aligned processes, this matters because the equity tracking requirement demands disaggregated data that is comparable across rounds. Data collected through intake fields without operational definitions cannot support that comparison: categories that appear identical across rounds may have collected different information if the fields' operational meaning was left implicit.

WALKRI's pre-publication audit also supports the transparency requirement by ensuring that participants can understand exactly what information they are being asked to provide and what it will be used for. A field that collects demographic information without explaining what disaggregation purpose it serves places participants in the position of providing data whose use they cannot evaluate. WALKRI's specification of measurement purpose for each field resolves this by making the use explicit before any participant engages.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
