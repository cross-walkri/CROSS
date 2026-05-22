---
title: W.K. Kellogg Foundation Evaluation Handbook and Logic Model Guide Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.4 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - https://www.betterevaluation.org/sites/default/files/2022-07/EvaluationHandbook.pdf
  - https://www.betterevaluation.org/tools-resources/wk-kellogg-foundation-logic-model-guide
  - https://www.nj.gov/state/assets/pdf/ofbi/kellogg-foundation-logic-model-development-guide.pdf
---

# W.K. Kellogg Foundation Evaluation Handbook and Logic Model Guide Compatibility - CROSS+WALKRI

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

This statement documents structural alignment between the W.K. Kellogg Foundation's two primary grantee-facing evaluation standards, the Kellogg Foundation Evaluation Handbook and the Logic Model Development Guide, and the CROSS+WALKRI specification standards. The Kellogg five-component logic model is the most widely cited logic model standard in US philanthropy and functions as the sector lingua franca for program planning and evaluation. CROSS's Theory of Change hierarchy directly implements the Kellogg logic model vocabulary. WALKRI ensures that intake fields collecting data at each logic model tier are measurement instruments before any applicant encounters them.

---

## The Kellogg Evaluation Framework

The W.K. Kellogg Foundation has produced two foundational documents that together constitute its primary evaluation standard for grantees and grant applicants.

The Kellogg Foundation Evaluation Handbook was written explicitly for project directors responsible for ongoing evaluation of WKKF-funded projects and for grant applicants preparing evaluation plans. It covers evaluation planning, data collection instrument design, data analysis, and reporting requirements. It does not prescribe a single evaluation method; it provides a framework for selecting methods appropriate to program goals and stakeholder questions. The Handbook treats evaluation planning as an early-stage activity integrated into program design, not as a reporting task initiated after programs are underway.

The Logic Model Development Guide defines the five-component logic model as the required structure for planning and reporting on WKKF-funded programs. The five components are: resources and inputs (what is invested in the program); activities (what the program does with those inputs); outputs (the direct products of the activities, measured in volume and reach); short-term outcomes (changes in awareness, knowledge, skills, and attitudes in target participants and communities); and long-term outcomes and impact (changes in behavior, practice, decision-making, policies, and conditions in the broader system). This five-component vocabulary is the most widely adopted logic model standard in US philanthropy. Hundreds of foundations, public agencies, and nonprofits have adopted it or adapted it as their primary planning and reporting structure.

The Kellogg framework is notable for its explicit distinction between short-term outcomes and long-term outcomes. Short-term outcomes are changes that are plausibly produced by the program within the grant period: participants learn something, acquire a skill, or shift an attitude. Long-term outcomes are changes that occur over a longer time horizon and often require multiple actors and cycles of change: behaviors shift, institutions change practice, policies are enacted, conditions in the community improve. This distinction is analytically important and is not preserved in all logic model adaptations. The Kellogg Guide treats it as a structural distinction, not merely a temporal one.

Grantees formally commit to results measures in grant agreements. The Handbook specifies that data collection instruments and evaluation questions must be developed with the intended learning use in mind, meaning that the choice of what to measure must be grounded in what decision-makers will actually do with the information. This is a principle of evaluation purposiveness that parallels WALKRI's measurement instrument specification requirements.

---

## How CROSS Satisfies the Kellogg Framework

CROSS's Theory of Change architecture directly implements the Kellogg five-component logic model as a pre-award gate structure, not merely as a planning template to be filled in after the round opens.

Resources and inputs map to CROSS's organizational identity fields and concurrent funding declarations. These fields require that the organizations responsible for program delivery be identified, that their capacity be declared, and that other funding sources be disclosed. The CROSS entry specification gate requires this information to be complete before applications open, which means the input side of the logic model is documented as a condition of the round opening.

Activities map to CROSS's activities tier in the Theory of Change. CROSS requires that activities be specified at the round level, not merely at the applicant level. This means the funder has declared what class of activities the round is designed to fund before any application is submitted, and applicants' proposed activities can be evaluated against that pre-specified scope.

Outputs map to CROSS's completion gate deliverable specification, the Build obligation. The completion gate requires that the outputs to be delivered are specified before the round opens: what deliverables are required, what counts as completion, what volume of output is the threshold, and what evidence constitutes output verification. This operationalizes the output tier of the logic model as a measurement commitment rather than a reporting category.

Short-term outcomes map to CROSS's progress verification gate evidence. The progress verification gate is designed to capture intermediate changes, specifically changes in awareness, knowledge, skills, or attitudes, that signal movement toward the longer-term condition the program is designed to affect. These are the changes that are measurable within a grant period and that provide evidence that the program is operating as intended before long-term outcomes can be observed. CROSS requires that the indicators for progress verification be specified before the round opens.

Long-term outcomes and impact map to CROSS's Change obligation target condition and goal-level declaration. CROSS's Change obligation mode, and its goal-tier Theory of Change fields, require that the longer-term condition the program is contributing to be named, that the baseline state of that condition be declared, that the target threshold be specified, and that the time horizon for achieving that condition be stated. This is the structural equivalent of the Kellogg long-term outcome tier, translated from planning vocabulary into pre-award gate requirements.

The distinction between short-term and long-term outcomes, which the Kellogg framework treats as a structural distinction, is preserved in CROSS through the separation between progress verification gate indicators (which capture within-period intermediate changes) and Change obligation completion gate indicators (which capture condition-level changes over the program horizon).

| Kellogg Logic Model Component | CROSS Mechanism |
|---|---|
| Resources/inputs | Organizational identity fields; concurrent funding declarations |
| Activities | Activities tier in Theory of Change; round-level activity scope declaration |
| Outputs | Build obligation completion gate; deliverable specification and evidence type |
| Short-term outcomes | Progress verification gate indicators: awareness, knowledge, skills, attitude changes |
| Long-term outcomes/impact | Change obligation target condition; goal-tier Theory of Change declaration |

---

## How WALKRI Complements This Alignment

WALKRI's five pre-publication field requirements ensure that intake fields at each logic model tier are measurement instruments rather than narrative prompts. An intake field that asks an applicant to describe their expected outputs is not an output measurement instrument unless it specifies what unit of output the funder is tracking, what threshold constitutes a complete output, and what evidence will be accepted. WALKRI requires that the construct, metric, unit, baseline, target, and evidence threshold be specified for every intake field before any applicant encounters it. This ensures that the logic model tiers are operationally defined at the instrument level before data collection begins.

The Kellogg Evaluation Handbook's principle of evaluation purposiveness, that measurement choices must be grounded in what decision-makers will do with the information, is implemented by WALKRI's requirement that every field's measurement purpose be declared. A field without a declared measurement purpose is not a measurement instrument; it is data collection without an evaluation question. WALKRI makes this explicit at the instrument design stage, before any applicant has an opportunity to produce data that cannot be used for the evaluation questions the funder is actually trying to answer.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
