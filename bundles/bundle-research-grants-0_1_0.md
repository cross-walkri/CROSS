---
title: CROSS+WALKRI Program Bundle - Research Grants
version: 0.1.0
date: 2026-05-19
license: CC0
standards: CROSS v0.4.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
bundle_type: research-grants
---

# CROSS+WALKRI Program Bundle: Research Grants

---

## Overview

This bundle covers grant and funding programs that support the production, validation, and dissemination of knowledge through systematic investigation. The ecosystem includes basic and applied research (NIH, NSF, Wellcome Trust, ACS, AHA, MRC), comparative effectiveness and patient-centered research (PCORI), open science and replication-focused programs (Arnold Ventures, registered report programs), innovation and technology development programs (SBIR/STTR, ARPA-H, ARPA-E, EIR), and development research with experimental design (J-PAL affiliated programs, IPA, IDRC Research Quality Plus).

Five program sub-types operate in this space with materially different obligation structures. This bundle addresses all five and notes where provisions diverge.

**Sub-type A: Basic and applied research** funds systematic investigation aimed at producing new knowledge (discoveries, methods, models, datasets, reagents, or theoretical frameworks). The output is the knowledge artifact, not a condition change in a population. Build obligation mode is primary.

**Sub-type B: Comparative effectiveness and patient-centered research** funds investigation into which interventions work better for which patients under which conditions, with mandatory patient engagement in study design. Change obligation mode applies because the study is designed to measure a condition difference between comparison groups, and the funder (PCORI) requires pre-specified primary outcome measures.

**Sub-type C: Open science and replication-focused programs** funds research designed with pre-registration, pre-analysis plans, and open data commitments as first-class outputs. Arnold Ventures and registered report programs treat the protocol as the primary deliverable and the subsequent study as an execution of the pre-committed plan. Build mode for the protocol; Build or Change mode for the study execution depending on whether outcomes or artifacts are primary.

**Sub-type D: Innovation and technology development** funds the transition of research findings into deployable technologies or commercial products. SBIR and STTR use a phased gate structure (Phase I feasibility, Phase II development, Phase III commercialization) that maps directly onto CROSS's four-gate sequence. ARPA-H and ARPA-E use payable milestones rather than phase gates. Build obligation mode is primary, with Change mode for the population health or energy transition outcomes that Phase III is designed to produce.

**Sub-type E: Development research with experimental design** funds randomized controlled trials and quasi-experimental studies embedded in development programs. J-PAL affiliated trials, IPA studies, and IDRC Research Quality Plus programs require pre-registration and pre-analysis plans as conditions of funding. Change obligation mode applies because the primary obligation is to produce valid causal evidence about whether an intervention changes a condition in a defined population.

---

## Part 1: CROSS Runbook

### Obligation Mode Selection

**Sub-type A (basic and applied research):** Use Build obligation mode. The primary obligation is the production of a specified artifact: a peer-reviewed publication, a dataset with a described schema and access condition, a research model or code repository, a biological reagent deposited in a named repository, or a theoretical framework documented in a specified format. The artifact is the deliverable. Where the study produces a negative or null result, a null result is a compliant output if it is documented and published; Build mode does not require positive findings, only that the specified artifact be produced.

**Sub-type B (comparative effectiveness and patient-centered research):** Use Change obligation mode. The primary obligation is to produce a valid estimate of the difference in outcomes between the study's comparison conditions. The pre-specified primary outcome measure is the indicator. The target value is the minimum clinically meaningful difference the study is powered to detect. The evidence threshold is the pre-specified alpha level and power. PCORI's Methodology Standards require all of these to be registered before data collection begins.

**Sub-type C (open science and replication-focused programs):** Use Build obligation mode for the protocol and pre-registration; Build or Change obligation mode for the study execution. Arnold Ventures treats the pre-registered protocol as the primary commitment: the funder's obligation is to the pre-commitment to a transparent process, not to a particular result. The protocol is the entry specification gate document; the study is the completion gate artifact.

**Sub-type D (innovation and technology development):** Use Build obligation mode for Phase I and Phase II. The Phase I deliverable is the feasibility assessment and the Phase II deliverable is the developed technology or prototype at a specified technology readiness level. Use Change obligation mode for Phase III outcomes (commercialization revenue, clinical adoption, energy production) where the program tracks population-level or market-level condition change as the portfolio benchmark. ARPA-H Payable Milestones are Build-mode deliverables specified to the completion criterion field of the CROSS indicator specification.

**Sub-type E (development research with experimental design):** Use Change obligation mode. The primary obligation is to produce a valid causal estimate of the intervention's effect on the pre-specified primary outcome. The causality stance is attribution (Tier 1 under ESSA/WWC standards if the design is a well-implemented RCT, or Tier 2 for quasi-experimental designs). The pre-analysis plan is the entry specification gate document: it commits the researcher to the indicator specification, the analysis method, and the evidence threshold before data collection begins.

### Entry Specification Gate

Before any application window opens, the following must be committed to in writing and published in a verifiable location (the funder's program announcement, a public repository, or, for study-level pre-commitment, an approved registration registry):

**Program specification:**
- Obligation mode (Build, Change, or mixed by component)
- Eligible research areas and study designs
- Pre-registration requirement (whether preregistration at a named registry is required before funding or before data collection)
- Open access and data sharing conditions (NIH data sharing policy level, Wellcome open access mandate, or equivalent)
- Independent review requirements (PCORI protocol registration, Arnold Ventures preregistration mandate, or equivalent)
- For Sub-type D: the phase gate structure, transition criteria from Phase I to Phase II, and the portfolio-level benchmarks (transition rate, commercialization revenue) applied at the program level

**Study-level pre-commitment (Sub-types B, C, and E):** The study protocol is the entry specification gate document at the individual grant level. The protocol must specify the primary outcome measure, the study design, the sample size and power calculation, the comparison condition, the analysis approach, and the pre-analysis plan reference before data collection begins. For registered reports: the protocol must be accepted by a journal or registry before participants are enrolled or data are collected.

**Ethics clearance:** The IRB or ethics committee approval status must be declared. Where approval is pending at the time of application, the requirement to obtain approval before data collection constitutes a condition of the entry specification gate.

### Application Gate

**Primary outcome measure specification:** For Sub-types B, C, and E, the primary outcome measure must be specified to all eleven fields. Fields 1 through 5 establish the indicator's identity: the measure name, its operational definition (the instrument, the scoring convention, and the recall period), the unit (a continuous scale score, a binary event, a rate per thousand), the baseline (the expected value in the comparison condition at the time of measurement), and the target (the minimum detectable effect or the clinically meaningful difference). Fields 6 through 11 establish the measurement architecture: the timing of assessment (enrollment, midpoint, end of intervention, follow-up periods), the data source (primary data collection with a named instrument, administrative records, biological sample), the collection method (self-report survey, clinician assessment, direct observation, assay), the comparison group (concurrent control condition in an RCT, matched comparison group in a quasi-experiment, or historical comparison with justification), the causality stance (attribution at the study level, with the study design as the rationale), and the evidence threshold (the pre-specified alpha level and power, or the minimum effect size the study is designed to detect).

**Pre-registration and pre-analysis plan:** For Sub-types B, C, and E, the preregistration registry name and registration identifier must be provided. Where a pre-analysis plan supplements the registration, the PAP document reference must be provided. The PAP must specify: which analyses are confirmatory (hypothesis tests that the study is powered to adjudicate), which are exploratory (analyses that will be reported as hypothesis-generating), and what the decision rule is for the primary hypothesis (the pre-specified alpha level and the power calculation's assumptions).

**Subgroup analysis plan:** Where the study will analyze outcomes for pre-specified subgroups, the subgroup analysis plan must name the subgroups, the rationale for each, and the analysis method. The disaggregation ratchet applies: a study may add subgroup analyses at completion that were not pre-specified, but it must distinguish pre-specified from exploratory analyses. Subgroup analyses presented as confirmatory that were not pre-specified do not satisfy the completion gate evidence standard for confirmatory inference.

**Data sharing plan:** For funders with data sharing requirements (NIH data sharing policy, Wellcome Trust grant conditions, NSF DMP), the data sharing plan must specify: the repository where data will be deposited, the access condition (open access with a named license, controlled access with a stated access process, or restricted with stated justification), the timeline for deposit after the primary publication, and the documentation that will accompany the data (codebook, data dictionary, analysis code).

### Completion Gate

**Artifact delivery (Sub-types A, C, and D):** The completion gate assessment must confirm that each specified artifact exists at the stated location, satisfies the operational definition stated at the application gate, and meets the access condition declared at the entry gate. For publications: a peer-reviewed paper or preprint at the stated repository. For datasets: a deposited dataset at the named repository with the stated documentation and access condition. For reagents: a deposited reagent at the named biorepository with the stated characterization data. For technologies: a prototype at the stated technology readiness level, assessed against the ARPA-H or SBIR technical criteria.

**Evidence against the primary outcome (Sub-types B, C, and E):** The completion gate assessment must confirm that the study analyzed the primary outcome using the method pre-specified in the registration or pre-analysis plan. Deviations from the pre-specified analysis must be disclosed and justified. The study must report both the effect estimate and its confidence interval at the pre-specified alpha level. A study that reports only statistical significance without the effect size and confidence interval does not satisfy the evidence threshold for confirmatory inference. Null results are compliant if the study was adequately powered and the analysis was conducted as pre-specified.

**Disaggregation at completion:** Subgroup analyses must be reported in the manner declared in the subgroup analysis plan. Pre-specified subgroup analyses must be distinguished from exploratory analyses in the results. Where the study was powered for the primary analysis but not for specific subgroups, this limitation must be stated with the available subgroup estimates.

**Data deposit and open access:** Where the data sharing plan committed to a deposit timeline, the deposit must occur within that timeline. Where open access to the primary publication was committed to, the access condition at the journal or repository must match the declared access condition. A paper published behind a paywall when the funder's policy required open access does not satisfy the access condition at the completion gate.

### Attestation Gate and Corpus

The Attestation Corpus for research grants should be structured to take advantage of scholarly infrastructure identifiers:

- Pre-registration record: the registration at the named registry (ClinicalTrials.gov, OSF Registries, AEA RCT Registry, PROSPERO, or equivalent) with the registration identifier and date; this is the primary attestation of the entry specification gate
- IRB or ethics approval: the approval letter or number, stored in the applicant's institutional record and referenced in the application
- Protocol document: for registered reports, the accepted protocol version with the acceptance date and journal or registry reference
- Primary publication: the DOI or preprint repository identifier, with the open access status confirmed
- Dataset deposit: the repository DOI or accession number, with the deposit date and access condition
- ORCID identifiers: for all named investigators; ORCID is the scholarly identity anchor equivalent to the on-chain wallet address in Web3 programs
- DataCite and Crossref metadata: machine-readable metadata linking the dataset and publication records through the scholarly metadata infrastructure

### Continuation Gate

For multi-phase programs (SBIR/STTR Phase I to Phase II) and for programs with renewal cycles (NIH R01 renewals, Wellcome Investigator Awards):

A continuing grant must demonstrate: delivery of all prior phase commitments (for SBIR/STTR: the feasibility assessment and the technical criteria for Phase II eligibility), resolution of all data sharing commitments from prior funded periods, and updated IRB coverage for any new study activities. For renewal applications: the renewal application must reference the primary publications and dataset deposits from the prior period as the completion evidence.

A continuing program operator (SBIR/STTR program office, NIH study section) must demonstrate: the portfolio-level benchmarks (Phase I-to-Phase II transition rate, commercialization revenue for Phase III companies) are tracked and published, and the transition criteria for phase advancement are stated before Phase I grants close.

---

## Part 2: WALKRI Field Specifications

The following field specifications cover the intake fields most commonly required in research grant programs. Each specification satisfies WALKRI's five pre-publication requirements: criterion intent, operational definition, response form, evidence form, compliance threshold.

---

### Field: Primary Outcome Measure

**Criterion intent:** Establishes the specific measure, instrument, scoring convention, and assessment timing that defines what the study is designed to detect, so that the completion gate can confirm the study was executed as designed and the results can be interpreted against a pre-committed standard.

**Operational definition:** The primary outcome measure is the single pre-specified measure that the study is designed and powered to assess. It is the measure against which the primary hypothesis is tested. For clinical and behavioral studies: the measure must be specified with the instrument name, the subscale or total score used, the scoring convention (higher scores indicate better or worse outcomes), and the recall period for the assessment. For studies using biological endpoints: the assay, the unit, and the detection threshold. For studies using administrative data: the variable name in the administrative system, the definition applied, and the time window.

**Response form:** A primary outcome measure declaration specifying: the measure name, the instrument or assay (with version number if applicable), the subscale or summary score used, the scoring convention, the assessment timing relative to the intervention (baseline, end of treatment, follow-up at a specified interval), and the unit (continuous, binary, or rate). One primary outcome measure per study. Secondary outcomes must be listed separately and are not subject to the same pre-specification requirement as the primary, though they must be distinguished from exploratory analyses.

**Evidence form:** The preregistration record at the named registry, which must include the primary outcome measure specification consistent with the application. Where the registration was filed before the application, the registration identifier is the evidence. Where the registration is a condition to be completed before data collection, the commitment to register constitutes provisional compliance.

**Compliance threshold:** A primary outcome measure declaration that specifies the instrument, scoring convention, and assessment timing with enough precision that an independent reviewer can confirm at completion whether the study analyzed the declared measure. A declaration of "patient health outcomes" without a named instrument does not satisfy this field. A study that analyzed a different primary outcome than declared at registration does not satisfy the completion gate unless a pre-specified deviation procedure was followed and documented.

---

### Field: Pre-registration Registry and Registration Identifier

**Criterion intent:** Establishes the pre-registration record as the verifiable entry specification gate document for the study, providing a time-stamped commitment to the study design, primary outcome, and analysis plan before data collection begins.

**Operational definition:** A pre-registration is a time-stamped record of the study design, hypotheses, primary outcome measures, sample size, and analysis approach, filed at an approved registry before data collection begins. The registration identifier is the unique reference that links all subsequent study documents (publications, datasets, completion reports) back to the pre-committed design. Approved registries include ClinicalTrials.gov (NCT identifier), OSF Registries (OSF DOI), AEA RCT Registry (AEARCTR identifier), PROSPERO (CRD identifier), WHO International Clinical Trials Registry Platform (any ICTRP-affiliated registry), and journal-hosted registered report identifiers.

**Response form:** The registry name and the registration identifier (e.g., NCT04567890, AEARCTR-0009876, OSF.io/abcde). If registration is pending at application because the study design is still being finalized with patient or community partners (as in PCORI studies), the commitment to register before data collection begins, with the intended registry named.

**Evidence form:** The registration record at the named registry, publicly accessible by the identifier. The record must include at minimum: the primary outcome measure, the study design, the sample size, and the planned analysis. The timestamp on the registration (showing it predates data collection) is the critical evidence element for the entry specification gate.

**Compliance threshold:** A valid registration identifier at an approved registry, with a timestamp that predates data collection. A registration filed after data collection has begun does not satisfy the entry specification gate requirement. A registration that omits the primary outcome measure does not satisfy the field. For studies where human subjects participation occurs in design and protocol development (PCORI community engagement studies), the registration must at minimum be filed before the intervention data collection begins.

---

### Field: Pre-analysis Plan Reference

**Criterion intent:** Establishes the complete specification of the planned statistical analyses before data are accessed or outcomes are observed, so that confirmatory results can be distinguished from exploratory results and multiple comparison inflation is controlled.

**Operational definition:** A pre-analysis plan (PAP) is a document that specifies: which hypotheses are confirmatory, what test statistic will be used for each hypothesis, what the decision rule is (the pre-specified alpha level), how multiple comparisons will be handled (Bonferroni correction, family-wise error rate control, or pre-specified secondary analysis designation), what the primary subgroup analyses are and whether they are confirmatory or exploratory, and what will be done about missing data (imputation approach, sensitivity analysis). The PAP must be filed before the researcher has access to the outcome data in a form that allows hypothesis-driven analysis.

**Response form:** A PAP document reference: either the file deposited at the registration registry (as a supplementary document to the preregistration) or a separate document with a DOI or repository URL and a timestamp that predates data analysis. The PAP must specify at minimum: the primary hypothesis test, the test statistic, the alpha level, the power calculation's assumptions, and the distinction between confirmatory and exploratory analyses.

**Evidence form:** The PAP document at the stated location, with a timestamp predating data analysis. For registered reports, the accepted protocol serves as the PAP; the acceptance letter date is the relevant timestamp. Where the PAP was submitted to the funder as part of the grant application and the funder provided approval, the approval date and grant number constitute the timestamp evidence.

**Compliance threshold:** A PAP that covers the primary hypothesis test with a named test statistic and alpha level, filed before data analysis begins. A PAP that specifies only "we will analyze the primary outcome using regression" without naming the covariates, the comparison condition, and the decision rule does not satisfy this field. A PAP filed after the researcher has accessed unblinded outcome data does not satisfy the pre-commitment requirement.

---

### Field: Sample Size and Power Calculation

**Criterion intent:** Establishes that the study is adequately powered to detect an effect of the minimum scientifically and clinically meaningful size, so that the target value for the primary indicator is grounded in a quantitative rationale rather than convenience or resource constraints.

**Operational definition:** A sample size and power calculation specifies: the minimum detectable effect size (the smallest difference between conditions that would be scientifically or clinically meaningful to detect), the assumed standard deviation (for continuous outcomes) or event rate (for binary outcomes) in the comparison condition, the desired statistical power (typically 80% or 90%), the alpha level (typically 0.05 two-tailed), and the total sample size required given these parameters. The sample size is the target value for the primary indicator in the CROSS eleven-field specification: the study must enroll at least this many participants to satisfy the completion gate at the power level declared.

**Response form:** A power calculation declaration specifying: the minimum detectable effect size and the basis for choosing it (prior literature, pilot data, clinical expert consensus, or regulatory standard), the assumed variability parameters, the desired power and alpha level, and the resulting required sample size. If attrition is expected, the inflated enrollment target and the assumed attrition rate must be stated.

**Evidence form:** A power calculation output from a named software tool (G*Power, Stata, R's pwr package, or equivalent) or an analytical derivation with the formula stated. The assumed effect size and variability parameters must cite their source (a specific publication, a pilot study report, or a regulatory guidance document). Where the funder requires a specific effect size benchmark (as in PCORI's clinically meaningful difference requirement), the benchmark must be cited.

**Compliance threshold:** A power calculation that specifies the assumed effect size with a cited rationale, the variability parameters, and the resulting sample size. A power calculation that assumes an effect size without citing a source does not satisfy the evidence form. A study that enrolls substantially fewer participants than the stated sample size without a protocol amendment does not satisfy the completion gate at the declared power level.

---

### Field: Data Sharing Plan

**Criterion intent:** Establishes the specific actions the research team will take to make study data available for replication, secondary analysis, and systematic review, satisfying the funder's data sharing requirements and the broader norm of open science.

**Operational definition:** A data sharing plan specifies: the repository where data will be deposited (a named institutional repository, a domain-specific repository such as ICPSR, NIMH Data Archive, UK Data Service, or OSF, or a funder-designated repository), the access condition under which data will be available (open access with a named license, controlled access with a stated application process, or restricted with a stated justification), the scope of data to be shared (de-identified individual participant data, aggregate results, analysis code, or all of the above), the timeline for deposit relative to the primary publication (simultaneous, within six months, or at grant closeout), and the documentation to accompany the data (codebook, data dictionary, analysis scripts, and any materials required to reproduce the primary analysis).

**Response form:** A data sharing plan document or structured response specifying: repository name, access condition, scope, timeline, and documentation list. For studies where individual participant data cannot be shared due to consent limitations, the plan must state the consent limitation and what can be shared instead (aggregate results, analysis code, or a synthetic dataset). "Data available upon request" does not satisfy any funder's data sharing requirement that specifies repository deposit.

**Evidence form:** At completion: the repository DOI or accession number for the deposited dataset, with the deposit date confirming the timeline commitment was met. For registered reports: the data deposit is often required simultaneously with acceptance for publication; the journal's confirmation of receipt serves as the evidence. For NIH-funded studies: the submission to the NIH-designated repository and the confirmation of data acceptance.

**Compliance threshold:** A data sharing plan that names a specific repository, states a specific access condition, and commits to a specific deposit timeline. A plan that states only a general intention to share data does not satisfy this field. At completion: a dataset deposited at the named repository with the access condition matching the declaration. A publication whose supplementary materials link to a data file hosted on a personal or institutional website (without DOI or persistent identifier) does not satisfy the repository deposit requirement.

---

## Part 3: Compatibility Map

This section maps the research grant program type to the frameworks in the CROSS+WALKRI compatibility corpus that are most directly applicable. The map is organized by primitive.

---

### Pre-specification Primitive

Pre-specification is the central primitive for research grants. The study protocol is the canonical implementation of the entry specification gate document:

- **Arnold Ventures Open Science Guidelines:** preregistration and pre-analysis plan required before funding is released; protocol transparency as a funder condition rather than a voluntary practice; registered reports as a structural implementation of the entry specification gate
- **PCORI Methodology Standards:** protocol registration required before data collection; the PCORI registry serves as the entry specification gate attestation record; the Methodology Standards specify eleven domains that map closely onto the CROSS eleven indicator fields
- **UK Government Evaluation Registry:** pre-registration of government-commissioned evaluations before fieldwork begins; the registry entry serves as the entry specification gate document for publicly funded evaluations
- **CROSS itself:** entry specification gate as the canonical implementation of this primitive

*Compatibility statements:* Arnold-Ventures-Open-Science-Guidelines, PCORI-Methodology-Standards, UK-Government-Evaluation-Registry, AEA-RCT-Registry, OSF-Registries.

---

### Causality Stance Primitive

Research grants have the most rigorous causality stance hierarchy of any program type in the CROSS compatibility corpus:

- **ESSA Tier 1-3 (Every Student Succeeds Act evidence standards):** Tier 1 requires a well-implemented RCT; Tier 2 requires a quasi-experimental design with baseline equivalence; Tier 3 requires a correlational study with statistical controls; the tier is the causality stance declaration for education research grants
- **WWC Standards Handbook (What Works Clearinghouse):** parallel tiered evidence standards for education research; the WWC review process is a form of independent verification of the causality stance claim
- **PCORI Methodology Standards (mandatory patient engagement):** PCORI adds a distinctive requirement: the causality stance declaration must be made in the context of a study design that was developed with patient and stakeholder engagement; the engagement process is itself a pre-specified component of the entry specification gate

*Compatibility statements:* ESSA-Tier-1-3, WWC-Standards-Handbook, PCORI-Methodology-Standards-Causal-Inference-Domain, IDRC-Research-Quality-Plus.

---

### Disaggregation Primitive

The disaggregation ratchet in research grants applies primarily to pre-specified subgroup analyses:

- **PCORI Heterogeneity of Treatment Effects domain:** PCORI's Methodology Standards require pre-specification of subgroup analyses for heterogeneity of treatment effects; a study that conducts subgroup analyses without pre-specification is not compliant with the PCORI HTE standard
- **ESSA disaggregation requirements:** ESSA requires that education research report results for disaggregated student groups (race and ethnicity, disability status, English learner status, income); subgroup analyses must be distinguished from the primary study design question

*Compatibility statements:* PCORI-HTE-Domain, ESSA-Disaggregation-Requirements, NIH-Inclusion-Policy-Women-Minorities.

---

### Independent Verification Primitive

Research grants have distinctive independent verification mechanisms that differ from the third-party evaluation used in development programs:

- **PCORI protocol registration:** the PCORI registry review process constitutes an independent assessment of the study design before data collection; the registered protocol is the pre-committed design against which the study's conduct is assessed
- **Arnold Ventures preregistration mandate:** Arnold's requirement that all funded studies preregister before funding is released constitutes an independent commitment mechanism; the funder's review of the preregistration is a form of independent verification of the entry specification gate
- **Peer review at publication:** journal peer review is the standard independent verification mechanism for research outputs; it confirms that the study was conducted as described and that the conclusions follow from the evidence; CROSS treats publication in a peer-reviewed journal as satisfying the independent verification requirement at the completion gate for Sub-type A

*Compatibility statements:* PCORI-Protocol-Registration, Arnold-Ventures-Preregistration, WWC-Review-Process, Cochrane-Systematic-Review.

---

### Evidence Form Specification Primitive

Research grants have the most precisely specified evidence forms of any program type, because the evidence form is the scientific instrument:

- **PCORI (instrument and scoring convention in registered protocol):** PCORI requires the primary outcome measure instrument and scoring convention to be specified in the registered protocol; this is Field 2 (operational definition) of the CROSS eleven-field indicator specification applied at maximum precision
- **NIH data sharing policy:** NIH requires a data management and sharing plan specifying the repository, access condition, and timeline; the policy has moved from optional to required for all NIH-funded research
- **Wellcome Trust open access policy:** Wellcome requires that all Wellcome-funded research be published open access with a CC BY license; this is the access condition in the CROSS public benefit mechanism declaration applied as a funding condition

*Compatibility statements:* PCORI-Methodology-Standards, NIH-Data-Sharing-Policy, Wellcome-Open-Access-Policy, DataCite-Metadata-Schema, ORCID-Integration-Standards.

---

### Portfolio Benchmarks for Innovation Programs

SBIR/STTR and ARPA programs use portfolio-level benchmarks that aggregate across individual grants, creating a distinct accountability layer above the grant level:

- **SBIR/STTR Phase I-to-Phase II transition rate:** the fraction of Phase I awards that advance to Phase II; this is a portfolio benchmark applied to the funder's full program, not an individual grant metric; programs with low transition rates face additional scrutiny in the next congressional authorization cycle
- **SBIR/STTR commercialization revenue:** revenue generated by companies that received Phase II awards; the commercialization survey tracks this revenue across a cohort; CROSS treats this as a portfolio-level Change indicator measuring the program's economic impact
- **ARPA-H Payable Milestones:** individual project milestones specified as Build-mode deliverables with payment contingent on completion; the milestone payment structure is a direct implementation of CROSS's completion gate applied at each milestone rather than at program end

*Compatibility statements:* SBIR-STTR-Program-Benchmarks, ARPA-H-Payable-Milestones, ARPA-E-Portfolio-Assessment.

---

## New Primitives Relevant to Research Grant Programs

**The registered report as a pre-committed program structure:** The registered report format, pioneered by journals including PLOS ONE, Psychological Science, and Nature Human Behaviour, inverts the traditional publication sequence: a journal accepts a study for publication based on the pre-registered protocol before data collection, committing to publish regardless of the results. This eliminates publication bias at the source. For CROSS purposes, the registered report is the cleanest implementation of the entry specification gate: the protocol is the pre-commitment, the journal's acceptance is the institutional attestation, and the study execution and publication are the completion gate artifacts. Programs building research accountability infrastructure should study the registered report format as a model for the full entry-through-completion cycle.

**Null result as a compliant Build output:** Standard Build obligation mode requires delivery of the specified artifact. In research, a null result (no significant difference between conditions) is a legitimate and compliant output if the study was conducted as pre-specified and the null result is documented and published. CROSS's Build mode does not require positive findings; it requires that the pre-specified artifact (the study and its results, whatever they are) be produced. Programs that disclose this norm explicitly in their entry specification gate documentation reduce applicant confusion about what constitutes a successful grant.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
