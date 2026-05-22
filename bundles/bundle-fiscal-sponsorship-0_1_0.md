---
title: CROSS+WALKRI Program Bundle - Fiscal Sponsorship
version: 0.1.0
date: 2026-05-19
license: CC0
standards: CROSS v0.4.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
bundle_type: fiscal-sponsorship
---

# CROSS+WALKRI Program Bundle: Fiscal Sponsorship

---

## Overview

This bundle covers grant and funding programs in which a legally recognized nonprofit organization (the fiscal sponsor) holds grants on behalf of a project, initiative, or organization that lacks independent legal status or independent charitable determination. The fiscal sponsorship ecosystem includes comprehensive sponsorship arrangements, pre-approved grant relationships, independent contractor sponsorship, and cross-border arrangements in which a US 501(c)(3) sponsors non-US projects.

Fiscal sponsorship creates a distinctive entity boundary problem that no other bundle in the CROSS+WALKRI corpus addresses: the legal grant recipient (the sponsor) and the operational program (the sponsored project) are different entities with different identities, different accountability structures, and potentially different relationships to the grant funder. CROSS's entity boundary primitive and organizational identity fields were designed with this problem in mind; this bundle specifies how to apply them in fiscal sponsorship contexts.

Four program sub-types operate in this space with materially different legal structures, disbursement authorities, and accountability relationships. This bundle addresses all four and notes where provisions diverge.

**Sub-type A: Comprehensive fiscal sponsorship (NNFS Model A)** places the sponsored project entirely within the sponsor's legal identity. The sponsor is the legal grantee; the sponsored project has no independent legal standing. The sponsor controls all funds, hires project staff as its own employees, and bears full legal responsibility for the project's activities.

**Sub-type B: Pre-approved grant relationship (NNFS Model C)** allows the sponsored project to retain organizational independence. The sponsor does not hold the project's funds directly; instead, it certifies that the project's work qualifies as charitable and stands behind the grant as the IRS-recognized charitable organization. The project receives the funds and manages them independently under a pre-approved grant agreement with the sponsor.

**Sub-type C: Independent contractor sponsorship (NNFS Model L)** structures the sponsored project as a contractor providing services to the sponsor. The sponsor holds the grant and contracts with the project for deliverables; the project is not an employee-team within the sponsor but an external contractor.

**Sub-type D: International fiscal sponsorship** covers arrangements in which a US 501(c)(3) fiscal sponsor holds grants destined for non-US organizations or projects, satisfying US charitable determination requirements while enabling international program delivery.

---

## Part 1: CROSS Runbook

### Obligation Mode Selection

**Sub-type A (comprehensive):** Use Build or Change obligation mode depending on the project's activities. The sponsor selects the obligation mode as part of the grant agreement with the original funder; the sponsored project operates within the obligation mode the sponsor declared. The sponsor is the applying entity for CROSS purposes; the sponsored project's scope is declared within the sponsor's organizational identity fields.

**Sub-type B (pre-approved):** Use Build or Change obligation mode. The sponsored project is the applying entity for CROSS purposes, since it retains independence and manages the funds. The sponsor's role in the CROSS record is the independent verification pathway, not the applying entity.

**Sub-type C (independent contractor):** Use Build obligation mode. The project is contracted for deliverables; the obligation mode is Build because the sponsor-contractor relationship is structured around specific outputs the contractor will deliver.

**Sub-type D (international):** Use Build or Change obligation mode depending on the non-US project's activities. The US sponsor is the legal applying entity; the non-US project's scope and activities are declared within the organizational identity and scope fields.

### Entry Specification Gate

Before any application window opens (or before any grant agreement is executed between a funder and a fiscal sponsor), the following must be committed to in writing and published or recorded in the CROSS attestation corpus:

**Entity boundary declaration:** The primary entry-gate decision in fiscal sponsorship is the entity boundary declaration: which entity is the CROSS+WALKRI applying entity for this grant? The options are: (1) the fiscal sponsor (Sub-types A, D; and Sub-type C where the sponsor holds the grant), or (2) the sponsored project (Sub-type B; and Sub-type C where the project is the contractual party with the funder, which is atypical). This declaration governs which entity's organizational identity fields are completed, which entity's disbursement authority is declared, and which entity's Obligation Fulfillment Record is updated when the grant closes.

**Fiscal sponsorship agreement type:** The NNFS model reference (A, C, L, or other) governs the legal relationship between sponsor and project. This must be declared at the entry gate because it determines: who controls the funds, who is legally responsible for grant compliance, whether the project can represent itself to third parties as operating under the sponsor's charitable status, and what happens to the OFR if the project changes sponsors.

**Disbursement authority declaration:** In comprehensive fiscal sponsorship (Sub-type A), the sponsor controls disbursement; the sponsored project does not have independent disbursement authority. In pre-approved grant relationships (Sub-type B), the project controls disbursement once the sponsor releases funds. This distinction must be declared at the entry gate; it affects the completion gate evidence (who signs off on fund use) and the attestation corpus (which entity's records must confirm expenditure).

**Sponsored project scope:** A separate scope declaration covering the sponsored project's activities within the grant period. For Sub-type A (comprehensive), the sponsored project operates entirely within the sponsor's legal identity; the scope declaration distinguishes the sponsored project's work from the sponsor's other activities. This distinction is required for restricted fund accounting under INPAS and for the funder's project-level tracking.

**Concurrent sponsorship disclosure:** The sponsored project may simultaneously work with multiple fiscal sponsors covering different grant scopes, and the sponsor may hold multiple grants covering adjacent scopes. Both must be disclosed: other fiscal sponsors the project works with (and for what scope), and other grants the sponsor holds that cover the same or adjacent program area. For Sub-type A, the sponsor must also distinguish its own institutional grants from the sponsored project's grants in its financial reporting.

**2 CFR 200 pass-through determination (Sub-type D and federal grants):** For US federal grants passing through a fiscal sponsor to a sponsored project, the sponsor is a pass-through entity under 2 CFR 200. The determination of whether the sponsored project is a subrecipient (receiving federal award funds subject to 2 CFR 200 requirements) or a contractor (providing goods or services to the sponsor) must be made at the entry gate. This determination governs which federal requirements the sponsor must flow down to the project, including audit obligations.

### Application Gate

**Organizational identity of the applying entity:** For Sub-type A (comprehensive), the sponsor completes the full organizational identity declaration including its legal name, EIN, governance structure, current leadership, and prior grant history. The sponsored project's identity is declared within the sponsor's application as a program scope, not as a separate organizational identity.

For Sub-type B (pre-approved), the sponsored project completes the organizational identity declaration, including its own governance structure (even if informal, such as a steering committee or leadership team without independent legal standing) and the name and EIN of the fiscal sponsor standing behind the grant.

**Prior grant and OFR history:** For recurring sponsored projects, the OFR history must be disclosed. A project that has operated under prior fiscal sponsors must carry its OFR history with it; the current sponsor confirms receipt of the prior OFR and its completeness. A project whose prior OFR is incomplete or whose prior sponsor cannot confirm OFR delivery must disclose this gap at the application gate.

**Restricted fund classification at application:** The grant's restriction purpose and period must be declared at application so the sponsor can establish the restricted fund account before any funds are received. For INPAS-compliant financial reporting: the restriction purpose is the sponsored project's scope, the restriction period is the grant period, and the restriction authority is the grant agreement's terms. These three elements constitute the INPAS restricted fund opening record.

**Federal pass-through requirements (Sub-type D, federal grants):** Where the grant carries 2 CFR 200 requirements, the sponsor must list at the application gate all applicable requirements it will flow down to the sponsored project. At minimum: the requirement for the project to maintain financial records per 2 CFR 200 Subpart D, the audit threshold and requirement (Sub-subpart F), the cost principles applicable to the project's entity type, and any award-specific terms included by the federal awarding agency.

### Completion Gate

**Sub-type A (comprehensive):** Completion evidence is provided by the sponsor, who controls all records. The sponsor confirms: funds were expended within the declared project scope, restricted fund accounting maintained the grant restriction throughout the period, all deliverables or outcome indicators declared at the entry gate were achieved or explained, and the sponsored project's activities were within the scope authorized by the original funder. For grants with significant mid-grant changes to the sponsored project's scope or leadership, these changes must be disclosed as part of the completion gate assessment.

**Sub-type B (pre-approved):** Completion evidence is provided by the sponsored project. The sponsor's role at the completion gate is verification: confirming that the project's completion evidence is consistent with what the sponsor certified as qualifying charitable activity at the application gate. A discrepancy between the project's declared activities and the sponsor's certified scope is a completion gate issue that requires resolution before the gate closes.

**Sub-type C (contractor):** Completion evidence addresses the deliverables specified in the contractor agreement. The sponsor confirms that deliverables were received and that the contractor relationship was managed in accordance with the terms of the agreement.

**Sub-type D (international):** Completion evidence must address the equivalency determination (or expenditure responsibility) pathway the sponsor used to confirm the non-US project's charitable status. For expenditure responsibility grants: the sponsor confirms it monitored fund use, received and reviewed progress reports from the non-US project, and maintained the records required by IRS regulations governing expenditure responsibility.

**OFR transfer protocol:** At the completion gate, the OFR status for the sponsored project must be updated by the entity that holds it (the sponsor for Sub-types A, C, D; the project for Sub-type B). If the project is changing sponsors after this grant closes, the outgoing sponsor must confirm that the OFR is complete and available for transfer; the incoming sponsor must confirm receipt before the incoming grant begins.

### Attestation Gate and Corpus

The Attestation Corpus for fiscal sponsorship programs has a distinctive two-entity structure:

- Entity boundary declaration: the decision made at the entry gate identifying the applying entity, the fiscal sponsorship model, and the disbursement authority
- Fiscal sponsorship agreement: the executed agreement between sponsor and project (the NNFS model reference document), retained by the sponsor
- Grant agreement: the executed agreement between funder and sponsor, which defines the grant restriction and scope
- Restricted fund opening record (INPAS): restriction purpose, period, and authority documented before any funds are received
- Disbursement records: for Sub-type A, the sponsor's records of transfers to the project; for Sub-type B, the project's records of expenditure under the grant
- Federal pass-through documentation (where applicable): the sponsor's written communication to the project of all applicable 2 CFR 200 requirements, retained by the sponsor
- OFR: maintained by the entity identified at the entry gate (sponsor or project), updated at each gate, transferred with the project if it changes sponsors
- Completion gate assessment: signed by the applying entity; for Sub-type B, also reviewed by the sponsor as the independent verification pathway

### Continuation Gate

For recurring sponsored projects or multi-year fiscal sponsorship arrangements:

A continuing comprehensive sponsorship (Sub-type A) must demonstrate: prior period restricted fund balance reconciled and closed, OFR complete for the prior grant period, and any changes to the sponsored project's leadership or scope disclosed and updated in the organizational identity declaration for the new period.

A continuing pre-approved grant relationship (Sub-type B) must demonstrate: the sponsored project's prior OFR complete, the sponsor's charitable certification of the project's work renewed or confirmed as still current, and any changes to the project's governance or mission that might affect the sponsor's certification disclosed.

For projects changing sponsors mid-program: an OFR continuity package must be assembled by the outgoing sponsor, covering all gates completed under the prior sponsorship, and transferred to the incoming sponsor before the new grant period begins. The CROSS system treats a sponsor change as a material event requiring disclosure at the entry specification gate of the next grant period.

---

## Part 2: WALKRI Field Specifications

The following field specifications cover the intake fields most commonly required in fiscal sponsorship grant programs. Each specification satisfies WALKRI's five pre-publication requirements: criterion intent, operational definition, response form, evidence form, compliance threshold.

---

### Field: Entity Boundary Declaration

**Criterion intent:** Establishes which entity (fiscal sponsor or sponsored project) is the CROSS+WALKRI applying entity for this grant, resolving the foundational ambiguity in fiscal sponsorship arrangements before any other fields are completed.

**Operational definition:** The applying entity is the entity that signs the grant agreement with the funder and bears legal accountability for grant compliance. In comprehensive fiscal sponsorship (Model A), this is always the sponsor; in pre-approved grant relationships (Model C), this is typically the sponsored project (which signs its own grant agreement with the funder, with the sponsor's certified endorsement); in independent contractor sponsorship (Model L), this is the sponsor (which holds the grant and contracts with the project). The entity boundary declaration must also name the other party: if the sponsor is the applying entity, the sponsored project must be named; if the sponsored project is the applying entity, the sponsor must be named. Both entities' legal identities and EINs (or equivalent for non-US entities) must appear in the declaration.

**Response form:** A declaration stating: (1) the applying entity (sponsor or project), with legal name and EIN; (2) the other party to the fiscal sponsorship arrangement, with legal name and EIN or registration number; (3) the NNFS model reference governing the relationship; and (4) which entity will control disbursement of grant funds.

**Evidence form:** The executed fiscal sponsorship agreement between sponsor and project, which names both parties, identifies the NNFS model, and establishes disbursement authority. For new projects without an executed agreement at the time of application: a draft agreement or letter of intent from the sponsor confirming the relationship and model, with a commitment to execute the agreement before any funds are disbursed. An application that names a fiscal sponsor without an executed or draft agreement does not satisfy this field.

**Compliance threshold:** Both entities named, legal identities confirmed for both, NNFS model identified, disbursement authority established. An entity boundary declaration that names a fiscal sponsor but does not confirm the sponsor's agreement to sponsor this project does not satisfy this field. A declaration that identifies the wrong entity as the applying entity (for example, naming the sponsored project as the applying entity in a Model A arrangement) creates a structural inconsistency in the CROSS record that must be resolved before the grant is committed.

---

### Field: Fiscal Sponsorship Agreement Type

**Criterion intent:** Documents the legal model governing the fiscal sponsorship arrangement, establishing the accountability structure, disbursement authority, and compliance obligations that flow from the choice of model.

**Operational definition:** The NNFS (National Network of Fiscal Sponsors) model taxonomy provides the standard reference for fiscal sponsorship agreement types. Model A (comprehensive): the project is entirely within the sponsor's legal identity; the sponsor employs the project's staff and holds all assets. Model C (pre-approved grant relationship): the project retains independence; the sponsor pre-approves the project's work as qualifying charitable activity and stands behind grants. Model L (independent contractor): the project delivers services to the sponsor under a contractor agreement. Other models exist in practice (Models B, D, E, F, G) for specific situations; if a model outside A, C, and L is used, the agreement must be described in sufficient detail to establish the accountability structure equivalent to an NNFS model reference.

**Response form:** The NNFS model designation (A, C, L, or other with description) and a brief description of the key features of the arrangement as it applies to this grant: who holds the funds, who controls disbursement, who employs the project staff (if any), and what happens to the project's assets if the sponsorship arrangement ends before the grant period closes.

**Evidence form:** The executed fiscal sponsorship agreement, which specifies the model and its key provisions. For Model A arrangements: the agreement should confirm that the project operates as a program of the sponsor, that all assets are held by the sponsor, and that the project staff are employees of the sponsor. For Model C arrangements: the agreement should confirm the pre-approval mechanism, the independence of the project, and the sponsor's certification process. For international fiscal sponsorship (Sub-type D): the agreement must also address the equivalency determination or expenditure responsibility pathway the sponsor will use.

**Compliance threshold:** A named NNFS model (or described alternative) with an executed agreement that confirms the key features of the model. An arrangement described as a fiscal sponsorship that does not conform to any recognized model (and cannot be described with enough specificity to establish the accountability structure) does not satisfy this field. The agreement must be executed before funds are disbursed; a verbal or email-based arrangement without a written agreement does not satisfy this field regardless of the parties' good faith.

---

### Field: Disbursement Authority Confirmation

**Criterion intent:** Establishes who controls the grant funds and under what mechanism funds flow from the holding entity to the operational project, providing the accountability anchor for fund use across the two-entity structure of fiscal sponsorship.

**Operational definition:** Disbursement authority is the power to authorize expenditure of grant funds. In Model A (comprehensive), disbursement authority resides entirely with the sponsor; the sponsored project makes expenditure requests that the sponsor approves and processes through its own financial system. In Model C (pre-approved), disbursement authority resides with the sponsored project once the sponsor has released the grant funds; the project operates its own financial accounts and makes its own expenditure decisions within the scope of the pre-approved grant agreement. In Model L (contractor), disbursement authority resides with the sponsor (who holds the grant), while the contractor invoices for deliverables and is paid as a vendor. For international fiscal sponsorship (Sub-type D): disbursement authority over the initial grant resides with the US sponsor, which then transfers funds to the non-US project through a mechanism (expenditure responsibility or equivalency determination) that satisfies IRS requirements.

**Response form:** A statement identifying: which entity holds disbursement authority, the mechanism through which funds flow from the holding entity to the operational project (reimbursement, advance, direct payment to vendors), the approval process for disbursements, and any spending limits or categories that require special approval. For Model A: the sponsor's financial authorization procedures for the sponsored project. For Model C: the grant release mechanism (when and how the sponsor transfers funds to the project). For international (Sub-type D): the transfer mechanism and the IRS compliance pathway (expenditure responsibility or equivalency determination).

**Evidence form:** The fiscal sponsorship agreement's financial provisions, the sponsor's financial authorization policies (for Model A), or the grant release schedule (for Model C). For federal pass-through grants: the sponsor's written notification to the sponsored project of the disbursement conditions and 2 CFR 200 requirements applicable to fund use.

**Compliance threshold:** A named disbursement authority with a documented transfer mechanism. An arrangement in which funds flow from the sponsor to the project without a documented mechanism or approval process does not satisfy this field. For Model A: the sponsor's financial authorization policies must exist in writing before any funds are received from the funder. For international (Sub-type D): the IRS compliance pathway must be determined (expenditure responsibility vs. equivalency determination) and documented before any funds are transferred to the non-US project.

---

### Field: Sponsored Project Scope

**Criterion intent:** Establishes what work the sponsored project will perform within the grant period, distinguishing the project's activities from the sponsor's other activities and from other grants covering adjacent scopes, providing the basis for restricted fund accounting and grant-specific completion gate assessment.

**Operational definition:** The sponsored project scope is the set of activities, outputs, and outcomes the sponsored project will pursue using the grant funds during the grant period. For Model A (comprehensive): the scope defines the project's work within the sponsor's broader institutional activities; it is the basis for the restricted fund account the sponsor establishes for this project. For Model C (pre-approved): the scope defines what the independent project does that qualifies as charitable under the sponsor's certification; it is the basis for the sponsor's pre-approval and for the funder's project-level tracking. For Model L (contractor): the scope defines the deliverables the contractor will provide to the sponsor; it must be specific enough to support the contractor agreement's deliverable specifications. The scope must be distinct from the sponsor's own institutional programs; a scope that is indistinguishable from the sponsor's general charitable mission does not satisfy this field.

**Response form:** A description of the project's activities during the grant period (what it does), the population served (who benefits), the geography (where activities occur), and the grant-specific outputs or outcomes the project will produce. For Model A: confirmation that the scope is distinct from the sponsor's other programs and a statement of how the sponsor will track the project's expenditure separately from its other restricted funds. For Model C: a statement of what qualifies the project's work as charitable under the sponsor's certification standards.

**Evidence form:** At entry: the scope description in the grant application or fiscal sponsorship agreement. At completion: the final report addressing the scope as declared, with evidence that activities were confined to the declared scope and that the restricted fund account covered only the activities within the scope. Mid-grant scope changes must be disclosed to the funder and documented in the CROSS attestation corpus before additional work outside the original scope begins.

**Compliance threshold:** A scope that is specific enough to distinguish the project's work from the sponsor's other activities, names a population and geography, and specifies at least one output or outcome. A scope described only as "general charitable activities within [sponsor's mission area]" does not satisfy this field because it cannot be distinguished from the sponsor's general operations. Scopes that expand mid-grant without funder approval and documentation do not satisfy this field at the completion gate.

---

### Field: Concurrent Sponsorship Disclosure

**Criterion intent:** Documents other fiscal sponsors the project works with and other grants the sponsor holds covering the same or adjacent scope, preventing double-counting of the same project work across multiple funders and enabling assessment of additionality.

**Operational definition:** Concurrent sponsorship exists when a sponsored project works with more than one fiscal sponsor for different grants covering different (or overlapping) scopes simultaneously. Concurrent grant scope overlap exists when the sponsor holds multiple grants (from different funders) covering activities that could be mistaken for the same work. Both situations require disclosure. For Model A (comprehensive): the sponsor must also distinguish between grants held by the sponsor for its own programs and grants held on behalf of sponsored projects; the disclosure covers both. For Model B (pre-approved): the sponsored project must disclose other fiscal sponsors it works with and other independent grants it holds that cover the same programmatic area. For international (Sub-type D): the US sponsor must disclose any other US or non-US funders supporting the same non-US project through the same or parallel grant pathways.

**Response form:** A list of other fiscal sponsors the project works with (if any), specifying the sponsor name, the scope of the sponsored work, and the grant amount. A list of other grants the sponsor holds covering the same or adjacent program area, specifying the funder, the scope, and the grant period. An explicit statement that no concurrent sponsorships or overlapping grants exist if none are present.

**Evidence form:** The disclosure itself is the evidence at the application gate. Funders may cross-reference grant databases and public financial filings (Form 990) to verify completeness. For federal grants: 2 CFR 200 requires disclosure of other federal awards; the concurrent sponsorship disclosure satisfies this requirement for the fiscal sponsorship dimension of the federal award.

**Compliance threshold:** A disclosure that names all concurrent fiscal sponsors and overlapping grants for the declared scope. A disclosure that omits a known concurrent sponsorship arrangement is a material omission that triggers a completion gate review. "None" is a compliant response only when the project has no other fiscal sponsors and the sponsor holds no other grants covering the declared scope. For international fiscal sponsorship (Sub-type D): disclosure must cover US and non-US funding sources for the non-US project.

---

### Field: Pass-Through Requirements

**Criterion intent:** Documents which 2 CFR 200 requirements the fiscal sponsor is flowing down to the sponsored project as a pass-through entity for federal grants, ensuring that the sponsored project is aware of and compliant with applicable federal requirements.

**Operational definition:** Under 2 CFR 200, a pass-through entity is a non-federal entity that receives a federal award and subawards a portion of those funds to a subrecipient. If the sponsored project is a subrecipient (not merely a contractor), the sponsor must flow down all applicable federal requirements. Required pass-through information includes: the federal award identification number and date, the applicable CFDA number, all federal requirements imposed by the federal awarding agency on the award, and the indirect cost rate applicable to the project. The distinction between subrecipient and contractor (determined at the entry gate) governs which requirements apply: subrecipients are subject to 2 CFR 200 requirements; contractors are subject only to the contractor agreement terms.

**Response form:** For grants subject to 2 CFR 200: a list of the federal requirements flowed down to the sponsored project, including the audit threshold and requirement, the cost principles applicable to the project's entity type, reporting requirements, and any award-specific terms. For grants not subject to 2 CFR 200 (private foundation grants, corporate grants): a statement confirming that this field does not apply and identifying the grant source.

**Evidence form:** The sponsor's written notification to the sponsored project of applicable federal requirements, typically in the subaward agreement or pass-through letter. For model A (comprehensive): the sponsor bears all federal compliance obligations internally and is not flowing requirements down to a separate entity; this field is marked as not applicable with an explanation that the project operates entirely within the sponsor's legal identity. For model C (pre-approved): the pass-through requirements must be communicated in writing before any project expenditure begins.

**Compliance threshold:** For grants subject to 2 CFR 200: a written notification to the sponsored project of all applicable requirements, executed before any subaward funds are disbursed. An oral communication of federal requirements, or a communication that omits the audit threshold or cost principles, does not satisfy this field. For grants not subject to 2 CFR 200: a confirmation that this field does not apply with the grant source identified. A blank field without explanation does not satisfy this field.

---

### Field: Obligation Fulfillment Record Ownership

**Criterion intent:** Establishes which entity maintains the Obligation Fulfillment Record for this grant and what happens to the OFR if the project changes sponsors, ensuring continuity of accountability across the lifecycle of the sponsored project.

**Operational definition:** The OFR is the cumulative record of a program's completion of gate requirements across all its grant periods. In fiscal sponsorship, OFR ownership follows the applying entity: the sponsor holds the OFR for Sub-type A (comprehensive), C (contractor), and D (international) grants; the sponsored project holds the OFR for Sub-type B (pre-approved) grants. When a project moves between sponsors, the OFR must move with it: the outgoing sponsor's completed gates become part of the project's accountability history, and the incoming sponsor must receive, review, and confirm the OFR before the new grant period begins. A project whose OFR cannot be transferred because the outgoing sponsor is defunct, unresponsive, or in dispute with the project must disclose this gap at the entry gate of the next grant period.

**Response form:** A declaration of which entity holds the OFR for this grant (sponsor or project), the current status of the OFR (gates completed, gates pending, any open items from prior grant periods), and the transfer protocol if the project changes sponsors before the grant period closes. For new projects without prior OFR history: a statement confirming this is the first grant period for this project under this sponsor.

**Evidence form:** The OFR itself, maintained by the declared holding entity and available for review by the funder upon request. For Sub-type B (pre-approved): the project's OFR may be held in formats ranging from a formal CROSS-compliant record to a grant report archive; whatever format is used, the record must cover all prior grant periods and all gates completed. For projects changing sponsors: the outgoing sponsor's signed transfer confirmation and the incoming sponsor's signed receipt.

**Compliance threshold:** A named holding entity, a current OFR status, and a transfer protocol for sponsor changes. An OFR ownership declaration that cannot identify the holding entity or cannot produce the OFR record upon request does not satisfy this field. For projects with prior grant history: the OFR must cover all prior periods; gaps in prior OFR coverage must be disclosed and explained. A project that has completed prior grant periods but has no OFR records (because prior funders did not require them) may establish a retrospective OFR summary, but must disclose that the prior periods were not recorded contemporaneously.

---

### Field: Restricted Fund Classification

**Criterion intent:** Documents the INPAS restricted fund classification for this grant at the point of recognition, establishing the restriction purpose, period, and documentation required for INPAS-compliant financial reporting by the fiscal sponsor.

**Operational definition:** Under INPAS (International Non-Profit Accounting Standard), a restricted fund is a fund in which resources are designated for a specific purpose, period, or both by an external authority (typically the grant agreement). Fiscal sponsorship grants are typically restricted: the funder restricts the funds to the sponsored project's scope (purpose restriction) and the grant period (period restriction). The sponsor recognizes the restricted fund at grant execution, not at receipt of funds: the obligation is created when the grant agreement is signed. The restricted fund account must track expenditure separately from the sponsor's general funds and from other restricted funds (including other sponsored projects). At grant close, the restricted fund is released to unrestricted status if all grant conditions are met and all funds are expended; unexpended funds are returned to the funder or re-restricted per the grant agreement's terms.

**Response form:** A declaration of: (1) the restriction purpose (the sponsored project's scope as defined in the grant agreement); (2) the restriction period (the grant start and end dates); (3) the restriction authority (the grant agreement, with the agreement date and funder identified); and (4) the fund code or account identifier the sponsor will use in its financial system to track this restricted fund. For Sub-type B (pre-approved): the restricted fund is held by the sponsored project, not the sponsor; the project's response covers the same four elements in the project's own financial system.

**Evidence form:** The grant agreement's terms (confirming the restriction purpose, period, and authority), the sponsor's chart of accounts showing the fund code established for this grant, and the sponsor's or project's financial statements for the grant period (confirming that restricted fund accounting was maintained and that the grant funds were not commingled with unrestricted funds). For federal grants: the restricted fund classification must also comply with 2 CFR 200 Subpart D financial management requirements (separate identification of federal funds).

**Compliance threshold:** A restriction purpose matching the declared sponsored project scope, a restriction period matching the grant period, a named restriction authority (the grant agreement), and a fund code established in the financial system before funds are received. A grant treated as unrestricted revenue by the sponsor or project when the grant agreement contains purpose or period restrictions does not satisfy this field; it constitutes an INPAS classification error that must be corrected before the completion gate closes.

---

## Part 3: Compatibility Map

This section maps the fiscal sponsorship program type to the frameworks in the CROSS+WALKRI compatibility corpus that are most directly applicable. The map is organized by primitive.

---

### Entity Boundary Primitive

The entity boundary primitive requires programs to declare which entity bears accountability when the legal recipient and the operational program are different. Fiscal sponsorship is the primary domain in which this primitive applies:

- **NNFS National Network of Fiscal Sponsors Guidelines**: the most formally published standard addressing the entity boundary problem; provides the model taxonomy (A, C, L, and others) that distinguishes the sponsor's legal identity from the project's operational identity.
- **2 CFR 200 pass-through entity provisions**: the federal regulatory definition of the entity boundary between pass-through entity (fiscal sponsor) and subrecipient (sponsored project); the most legally consequential entity boundary standard in the US nonprofit sector.
- **CROSS entity boundary primitive**: the canonical implementation of this primitive across all program types; fiscal sponsorship is the test case that most fully exercises the primitive.

Compatibility statements: NNFS Fiscal Sponsorship Guidelines (3rd ed.), 2 CFR 200 (Subparts A and D), GFGP ARS 1651 (organizational capacity as applied to the sponsor's capacity to manage multiple projects).

---

### Organizational Identity Anchor Primitive

The organizational identity anchor primitive requires programs to declare a verifiable, stable organizational identity. In fiscal sponsorship, the identity anchor is the sponsor's legal identity for most sub-types:

- **NNFS Model A (comprehensive)**: the sponsor is the legal identity anchor; the project's identity exists only within the sponsor's organizational structure. The sponsor's EIN and IRS determination letter are the identity anchor documents.
- **GFGP ARS 1651**: organizational capacity standard applicable to the sponsor as the legal grantee; covers governance, financial management, and program delivery capacity at the institutional level.
- **NNFS Model C (pre-approved)**: the sponsored project provides the operational identity; the sponsor provides the charitable certification that makes the project's work grantable. Both identities are present in the CROSS record; the project's identity is the operational anchor and the sponsor's identity is the verification anchor.

Compatibility statements: NNFS Fiscal Sponsorship Guidelines, GFGP ARS 1651, GPC Grant Professional Certification Standards (grant professional's responsibility for entity identity accuracy).

---

### Disbursement Authority Primitive

The disbursement authority primitive requires programs to declare who controls the grant funds. CROSS's Part IV sixth organizational identity field is most directly relevant to fiscal sponsorship's authority delegation:

- **Model A disbursement authority**: sponsor controls all disbursements; project makes expenditure requests. The sponsor's financial authorization procedures are the disbursement authority documents.
- **Model C disbursement authority**: project controls its own expenditure once the sponsor releases the grant. The grant release schedule in the fiscal sponsorship agreement is the disbursement authority document.
- **2 CFR 200 pass-through provisions**: the federal regulatory framework for disbursement authority in federal pass-through grants; subaward agreements are the disbursement authority documents.

Compatibility statements: NNFS Fiscal Sponsorship Guidelines, 2 CFR 200 (Subpart D financial management), CROSS Part IV (organizational identity, sixth field).

---

### Restricted Fund Accounting Primitive

The restricted fund accounting primitive requires programs to classify grant funds correctly as restricted or unrestricted at recognition. Fiscal sponsorship is the primary context in which this primitive is exercised at the entity boundary:

- **INPAS International Non-Profit Accounting Standard**: restricted fund classification at grant recognition; fund accounting as the basis for nonprofit financial reporting. Fiscal sponsorship grants are the canonical restricted fund case: purpose-restricted, period-restricted, held by an entity that is not the operational program.
- **2 CFR 200 Subpart D financial management requirements**: separate identification and tracking of federal award funds; the federal regulatory parallel to INPAS restricted fund accounting.
- **GFGP ARS 1651**: financial management capacity standard covering restricted fund tracking as an organizational capability.

Compatibility statements: INPAS International Non-Profit Accounting Standard, 2 CFR 200 Subpart D, GFGP ARS 1651.

---

### Independent Verification Primitive

The independent verification primitive requires that completion gate evidence be confirmed by a party independent of the applying entity. In fiscal sponsorship, the sponsor serves as the independent verification pathway for the sponsored project's work:

- **Model C (pre-approved)**: the sponsor is the independent verification pathway for the sponsored project; the sponsor's certification of the project's work as qualifying charitable activity is the independent verification at the application gate, and the sponsor's review of the project's completion evidence is the independent verification at the completion gate.
- **International fiscal sponsorship (Sub-type D)**: the US sponsor's equivalency determination or expenditure responsibility oversight is the independent verification pathway for the non-US project's work; the IRS requires this verification as a condition of maintaining the US sponsor's charitable status.
- **CROSS independent verification principle**: the requirement that at least one gate assessment per grant period involve evidence reviewed by a party independent of the applying entity.

Compatibility statements: NNFS Fiscal Sponsorship Guidelines (Model C certification role), IRS Expenditure Responsibility regulations, CROSS independent verification principle.

---

### Portfolio Aggregation at the Sponsor Level

The sponsor-level portfolio of sponsored projects creates a distinctive form of portfolio aggregation: the sponsor holds accountability for multiple projects simultaneously, each with its own restricted fund account and OFR:

- **NNFS portfolio management**: fiscal sponsors managing multiple projects must maintain separate accounting for each; the NNFS guidelines address portfolio management at the sponsor level.
- **CROSS portfolio aggregation mechanism**: applied at the sponsor level, the portfolio consists of all sponsored projects and the sponsor's own programs; the mechanism tracks obligation completion across the portfolio.
- **PMD Pro/FMD Pro**: project management and financial management standards for development projects within sponsored structures; provides tools for multi-project tracking within a single organizational entity.

Compatibility statements: NNFS Fiscal Sponsorship Guidelines, CROSS portfolio aggregation mechanism, PMD Pro (project management for development), FMD Pro (financial management for development), GPC Grant Professional Certification Standards.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
