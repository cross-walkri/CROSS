---
title: WIOA Workforce Performance Accountability Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.5 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - Workforce Innovation and Opportunity Act, 20 USC Chapter 32
  - 20 CFR Part 677 (Performance Accountability)
  - DOL/ED Joint Performance Accountability Rule (February 2024 Federal Register)
  - dol.gov/agencies/eta/performance/wioa-performance
  - ecfr.gov/current/title-20/chapter-V/part-677
---

# WIOA Workforce Performance Accountability

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

The Workforce Innovation and Opportunity Act (WIOA), codified at 20 USC Chapter 32 and governed by 20 CFR Part 677, is the primary federal workforce development statute in the United States. It is jointly administered by the Department of Labor (DOL) and the Department of Education (ED) across a network of state and local workforce development boards. WIOA's six primary performance indicators, established nationally before any program year begins, constitute the most fully realized application of CROSS's entry specification gate in the US workforce system: the measurement domain is fixed by regulation, and the only discretion available to states and localities is the numerical target within that domain. CROSS+WALKRI satisfies WIOA's performance accountability requirements structurally, and WALKRI's pre-publication requirements address the primary data quality gap in how participant-level intake instruments are currently specified under the statute.

---

## The WIOA Performance Accountability Framework

WIOA Title I establishes a performance accountability system (20 CFR Part 677) that applies across all core program activities: adult employment and training, dislocated worker services, youth workforce activities, adult education and family literacy, and vocational rehabilitation. The statute requires states and localities to negotiate expected performance levels with DOL and ED before each program year using an objective statistical model that adjusts for economic conditions and participant characteristics.

WIOA's six primary indicators, codified at 20 CFR 677.155, are:

The employment rate in the second quarter after exit, measuring the share of program participants who are employed two quarters after leaving the program. The employment rate in the fourth quarter after exit, measuring sustained employment two years out. The median earnings in the second quarter after exit, capturing wage outcomes. The credential attainment rate, measuring the proportion of participants who obtain a recognized postsecondary credential or secondary school diploma. Measurable skill gains during participation, capturing interim progress for participants who have not yet exited. And the effectiveness in serving employers indicator, finalized in February 2024 in the Federal Register, capturing the workforce system's performance from the demand side of the labor market.

States negotiate expected performance levels with DOL and ED through a regulated formula-based process that itself constitutes a formal requirement: targets cannot be set retrospectively. Local workforce development boards negotiate separate local levels with the Governor and chief elected officials, creating a two-tier accountability structure. Programs that fail to reach 90% of their negotiated targets trigger a required improvement plan; continued failure triggers sanctions including the withholding of funds. States submit quarterly participant-level data covering demographics, services received, and outcomes, providing a longitudinal record of each participant's trajectory through the workforce system.

---

## How CROSS Satisfies the WIOA Performance Accountability Framework

CROSS addresses WIOA's performance accountability requirements at both the structural and field-specification levels.

| WIOA Accountability Element | CROSS Provision |
|:--|:--|
| Six nationally fixed indicator categories | Entry specification gate: measurement domains pre-specified before any program year begins |
| Negotiated performance levels (formula-based, pre-program-year) | Field 5 (target): targets established through a formal process before the program year, not retrospectively |
| Employment rate Q2 and Q4 indicators | Fields 1-5 (name, definition, unit, baseline, target) + Field 6 (timing: second and fourth quarter after exit) |
| Median earnings indicator | Fields 1-5 + Field 7 (data source: unemployment insurance wage records) |
| Credential attainment indicator | Fields 1-5 + Field 10 (causality stance: attribution to program participation) |
| Measurable skill gains indicator | Fields 1-5 + Field 6 (timing: during participation, not after exit) |
| Effectiveness in serving employers indicator | Fields 1-5 + Field 9 (collection method: employer surveys and administrative data) |
| Quarterly participant-level data | Disaggregation ratchet: demographic detail established at enrollment and maintained across reporting quarters |
| 90% threshold improvement plan trigger | Evidence threshold (Field 11): the regulatory performance threshold constitutes the evidence threshold for the accountability cycle |
| Participant demographic disaggregation (gender, race/ethnicity, disability, veteran status) | Disaggregation ratchet: these demographic categories are established at enrollment and cannot be removed from subsequent reporting rounds |
| Two-tier accountability (state and local) | Portfolio aggregation: local recipient outcomes aggregate to state-level outcomes, both pre-specified before program year begins |

WIOA's six-indicator set is the most fully realized example of CROSS's entry specification gate applied at the workforce system level. Where most grant frameworks allow funders or grantees to select indicators from a menu or specify them freely, WIOA eliminates that discretion for the primary performance domain entirely: the indicators are fixed by regulation, and the negotiated performance level process determines only the numerical target, not the measurement domain. This corresponds to CROSS's Field 5 (target) operating within a framework where Fields 1 through 4 (name, definition, unit, baseline) are already satisfied by federal regulation before any state or local plan is submitted.

The quarterly participant-level data submission requirement corresponds directly to CROSS's disaggregation ratchet. WIOA mandates that participant-level data include gender, race and ethnicity, disability status, veteran status, and economic disadvantage status from the point of enrollment. These demographic dimensions cannot be dropped in later reporting quarters; they follow the participant through exit and outcome measurement. CROSS's disaggregation ratchet encodes this principle as a structural requirement: once a demographic dimension is captured at the entry specification gate, it cannot be removed in subsequent rounds.

CROSS's Theory of Change hierarchy maps cleanly to WIOA's logic: program activities (services delivered to participants) produce outputs (participants enrolled, credential hours completed), which produce near-term outcomes (measurable skill gains), which produce medium-term outcomes (employment and earnings at Q2), which produce longer-term outcomes (sustained employment at Q4 and postsecondary credential attainment), which contribute to WIOA's overarching goal of a skilled workforce that meets employer demand.

---

## How WALKRI Complements This Alignment

WALKRI's five pre-publication field requirements address a structural gap in how WIOA participant-level intake instruments are currently specified. The six primary indicators are defined at the regulatory level in 20 CFR 677.155, but the intake instruments through which participant data is collected at local workforce development boards are designed at the local level, and the operational definitions of what documentation qualifies a participant for each status category are not standardized by the regulation.

Consider the credential attainment indicator: 20 CFR 677.155 specifies that a recognized postsecondary credential qualifies, but the operational definition of what documentation a program staff member must examine before marking a participant as having attained a credential, what constitutes verification of a secondary school diploma obtained abroad, and how concurrent enrollment in a credential program is classified at exit are all left to local interpretation. WALKRI's operational definition requirement and evidence form requirement, applied to the intake and exit survey instruments used at local workforce development boards before any participant is enrolled, resolve this at source by specifying what evidence qualifies for each status category before any case is opened.

The same logic applies to the measurable skill gains indicator, which has the most complex definitional structure of the six: it covers multiple gain types (educational functioning level advancement, attainment of a secondary school diploma, passage of a postsecondary licensure examination, and documented measurable skill gain in a training program). WALKRI's criterion intent and response form requirements ensure that the intake instrument specifies which gain type is being measured, what evidence constitutes each type, and what the compliance threshold is, before any participant begins receiving services. Applied across a state workforce system, WALKRI-conformant intake instruments produce participant-level data that is commensurable across local boards within the state and, where state specifications align, across states.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
