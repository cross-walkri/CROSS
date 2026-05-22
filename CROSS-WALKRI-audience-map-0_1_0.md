---
title: CROSS+WALKRI Audience Map - Six Cohorts
version: 0.1.0
date: 2026-05-19
license: CC0
standards: CROSS v0.4.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
---

# CROSS+WALKRI Audience Map

## Six Cohorts

---

## Overview

CROSS+WALKRI is a two-standard architecture for grant accountability. CROSS governs the obligation structure of grant programs: what funders commit to specifying, what grantees commit to producing, and how evidence of fulfillment is verified and recorded. WALKRI governs the intake field layer: what every field in every grant application or data collection instrument must specify before any applicant or participant sees it.

Six cohorts interact with this architecture from distinct positions with distinct needs. The cohorts are not organized by who holds the budget; they are organized by what each cohort does in relation to grant programs and what the standards do for them.

---

## Cohort 1: Grantees

Organizations applying for or receiving grants. They experience CROSS+WALKRI primarily through the intake instruments they fill out, the obligation they commit to, the evidence they produce, and the permanent record their fulfillment history creates.

**What CROSS delivers:** Grantees know before they apply what the round requires, what obligation mode applies (Build, Change, or Retroactive), what indicators they will be measured against, and what the completion gate criteria are. All of this is specified before applications open. Grantees assess fit before investing time in an application and face no criteria introduced mid-cycle. The Obligation Fulfillment Record is their permanent verifiable history across rounds: a queryable record of what was delivered and what remains outstanding. Part XI specifies redress rights when a funder changes criteria after applications open or applies gate tests that differ from published specifications.

**What WALKRI delivers:** Every intake field a grantee encounters in a WALKRI-conformant form specifies why the data is collected, what a qualifying response looks like, what format responses must take, what documentation must be provided, and what threshold a response must meet. Grantees know exactly what is required and do not interpret ambiguous questions while hoping their interpretation matches the reviewer's.

**Primary CROSS provisions:** Part IV (entry specification gate, obligation modes, pre-award indicator confirmation), Part V (indicator specification), Part VI (concurrent funding disclosure), Part VII (conflict disclosure), Part XI (redress).

---

## Cohort 2: Reviewers

People evaluating applications and gate evidence at any stage of a grant program. They experience CROSS+WALKRI primarily as the architecture that specifies the criteria they apply, at what precision, and with what procedural protections for consistency.

**What CROSS delivers:** Reviewers assess submissions against criteria that existed before the round opened. They are not asked to construct standards mid-review or apply standards that were not disclosed to applicants. The calibration requirement (Part VII) mandates a calibration exercise with worked examples and an inter-rater consistency check before reviewers assess live applications at independent review level or above. The conflict-of-interest framework specifies exactly what must be disclosed and what constitutes a categorical bar, protecting reviewers from reputational exposure and ensuring grantees are assessed by unconflicted parties.

**What WALKRI delivers:** WALKRI-conformant intake forms carry pre-specified compliance thresholds for every field. Reviewers assess responses against those thresholds rather than determining thresholds independently during review. Consistency across reviewers improves as a structural consequence, because the threshold is embedded in the form specification, not left to individual judgment.

**Primary CROSS provisions:** Part IV (entry gate specification), Part VII (calibration requirement, conflict-of-interest framework), Part VIII (completion gate evidence standards and evidence strength taxonomy).

---

## Cohort 3: Program Operators

Staff and contractors who run grant programs day-to-day: drafting round specifications, configuring intake forms, coordinating reviewers, tracking disbursements, collecting completion evidence, and producing closing documentation. They experience CROSS+WALKRI as the operational architecture that governs every decision in the grant program lifecycle.

**What CROSS delivers:** CROSS provides a structured four-gate lifecycle that makes the program timeline and decision points explicit before the round opens. Each gate has specified inputs and outputs: what must be ready before it opens, what must be produced before it closes. The Grant Configurator architecture (Part IX) provides the implementation model for configuring rounds. Part XI specifies what funders are obligated to publish and maintain, giving program operators a clear compliance checklist.

**What WALKRI delivers:** The pre-publication audit is the primary WALKRI procedure for program operators. Before any intake form is shared with applicants, operators conduct a field-by-field review confirming that each field satisfies all five requirements. WALKRI converts what is otherwise an informal editorial process into a structured audit with a clear conformance standard. The pre-publication audit is the operational procedure that produces WALKRI conformance.

**Primary CROSS provisions:** Part IV (full gate sequence and round specification), Part IX (Grant Configurator), Part XI (funder obligations and published deliverables).
**Primary WALKRI provisions:** All five pre-publication requirements as an operational audit procedure; Part IV pre-publication audit documentation.

---

## Cohort 4: Platform Providers

Organizations building software on top of CROSS+WALKRI: grant management systems, application portals, reviewer dashboards, attestation infrastructure, analytics tools. They experience CROSS+WALKRI primarily as a specification for a data model and workflow architecture.

**What CROSS delivers:** CROSS is a machine-readable obligation architecture. Its four-gate sequence maps to workflow states. Its obligation modes map to program type configurations. Its eleven-field indicator specification maps to a structured data schema for outcome data. Its Attestation Corpus maps to a persistent queryable record. Part IX (Grant Configurator) is the primary implementation target: it specifies what a CROSS-conformant grant configuration tool must capture and publish. Platform providers who implement CROSS produce software that any CROSS-conformant funder can adopt without re-engineering.

**What WALKRI delivers:** WALKRI's five pre-publication field requirements are field-level metadata that form builders must support. Every intake field in a WALKRI-conformant system carries five structured metadata fields alongside the field itself. Platform providers who implement WALKRI produce form builders that generate WALKRI-conformant forms by default, reducing the pre-publication audit burden for program operator customers.

**Primary CROSS provisions:** All Parts as a specification for software implementation; Part IX (Grant Configurator) as the primary implementation target; Part V (indicator specification as data schema).
**Primary WALKRI provisions:** All five requirements as field-level metadata; the pre-publication audit as a system-level procedure that the platform can automate.

---

## Cohort 5: Analysts

Researchers, evaluators, and data practitioners who study grant outcomes across programs, funders, and sectors. They experience CROSS+WALKRI primarily as the architecture that determines whether data from different programs can be compared, combined, and learned from.

**What CROSS delivers:** CROSS's indicator specification requires that every outcome indicator be defined with a name, operational definition, unit, baseline, target, timing, data source, collection method, comparison group, causality stance, and evidence threshold. When two programs both report against a commensurably specified indicator, their data can be compared. When they do not, comparison produces noise. The structured dataset publication requirement (Part XI) mandates that a machine-readable dataset be released at round close, giving analysts programmatic access to outcome data rather than requiring manual extraction from narrative reports. The Attestation Corpus is a public, queryable record of verified performance claims across all CROSS-conformant programs.

**What WALKRI delivers:** The operational definition and evidence form requirements are the two WALKRI fields that most directly determine cross-program comparability. If two programs use the same indicator label but different operational definitions, their data is not comparable. WALKRI's pre-publication audit, applied consistently across programs, produces intake instruments that generate data under consistent definitions. For analysts, WALKRI conformance is the precondition for valid cross-program analysis.

**Primary CROSS provisions:** Part V (indicator specification as the basis for comparability), Part XI (structured dataset publication at round close), Attestation Corpus (public performance record).
**Primary WALKRI provisions:** Operational definition requirement and evidence form requirement as the determinants of cross-program comparability.

---

## Cohort 6: Institutional Funders

Foundations, government agencies, DAOs, and multilateral bodies making strategic decisions about grant program design and adoption of accountability standards. They experience CROSS+WALKRI primarily as the architecture they are considering adopting and the evidence base for why adoption serves their institutional interests.

**What CROSS delivers:** Part XII documents formal structural alignment between CROSS and 95+ institutional frameworks spanning international development, public health, workforce development, environmental finance, education, corporate accountability, Islamic giving, humanitarian standards, and Web3 public goods. An institutional funder whose existing evaluation requirements are addressed in Part XII can adopt CROSS without abandoning its existing framework: CROSS satisfies those requirements structurally. The pre-commitment architecture protects institutional funders from retrospective accountability claims. The portfolio-level reporting structure aggregates program outcomes for institutional learning and external reporting requirements.

**What WALKRI delivers:** The pre-publication audit is an institutional due diligence procedure. Institutional funders who require WALKRI conformance across their grant portfolio ensure that every intake instrument their grantees encounter is specified to a standard that produces comparable, auditable data. For institutional funders who report against mandatory indicator sets (HRSA UDS, SAMHSA NOMs, WIOA, ESSA, and others covered in Part XII), WALKRI conformance at the intake field level is the structural mechanism that ensures reported data satisfies those mandatory indicators reliably.

**Primary CROSS provisions:** Part XII (compatibility with 95+ institutional frameworks), Part IV (pre-commitment mechanism), Part XI (portfolio-level outputs and funder obligations).
**Primary WALKRI provisions:** Pre-publication audit as institutional due diligence; Part X (compatibility with external evaluation standards).

---

## Summary

| Cohort | Primary CROSS Value | Primary WALKRI Value |
|:--|:--|:--|
| 1. Grantees | Obligation clarity before applying; redress rights if criteria shift | Legible intake forms with specified thresholds eliminating interpretation risk |
| 2. Reviewers | Pre-specified criteria; calibration requirement; conflict framework | Compliance thresholds that replace reviewer-level threshold determination |
| 3. Program Operators | Structured four-gate lifecycle; round specification architecture | Pre-publication audit as an operational conformance procedure |
| 4. Platform Providers | Machine-readable obligation architecture mapping to a data model and workflow | Field-level metadata specification enabling WALKRI-conformant form builders |
| 5. Analysts | Commensurably specified indicators; mandatory structured dataset at round close; public Attestation Corpus | Operational definitions and evidence form requirements as the basis for cross-program comparability |
| 6. Institutional Funders | Compatibility with 95+ existing frameworks (Part XII); portfolio reporting structure | Pre-publication audit as institutional due diligence ensuring mandatory indicators are reliably collected |

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
