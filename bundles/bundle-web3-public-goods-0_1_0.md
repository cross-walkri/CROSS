---
title: CROSS+WALKRI Program Bundle - Web3 and Public Goods Funding
version: 0.1.0
date: 2026-05-19
license: CC0
standards: CROSS v0.4.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
bundle_type: web3-public-goods
---

# CROSS+WALKRI Program Bundle: Web3 and Public Goods Funding

---

## Overview

This bundle covers grant and funding programs that distribute resources from protocol treasuries, DAO governance mechanisms, quadratic funding pools, and retroactive public goods funding systems. The ecosystem includes direct grants (Ethereum Foundation ESP, Arbitrum DAO grants, protocol treasury allocations), quadratic funding rounds (Gitcoin Grants, Octant), and retroactive public goods funding (Optimism RetroPGF, Optimism Retro Funding 2025, Protocol Guild).

Three program sub-types operate in this space with materially different obligation structures. This bundle addresses all three and notes where provisions diverge.

**Sub-type A: Prospective grants** distribute funds before work begins against a specified deliverable or outcome (Ethereum Foundation ESP early grants, Gitcoin Grants project rounds, protocol treasury grants).

**Sub-type B: Retroactive funding** rewards demonstrated past contribution assessed after the fact (Optimism RetroPGF Rounds 1-4, Protocol Guild, Gitcoin retroactive rounds).

**Sub-type C: Quadratic funding** matches community contributions using a mathematical formula that weights the number of contributors rather than only total contribution volume (Gitcoin QF rounds, Octant allocation mechanism, clr.fund).

---

## Part 1: CROSS Runbook

### Obligation Mode Selection

**Sub-type A (prospective grants):** Use Build obligation mode if the grant funds a specified deliverable (a piece of software, a piece of infrastructure, a defined artifact). Use Change obligation mode if the grant funds a program designed to shift a measurable condition in the ecosystem (developer adoption rates, protocol usage, user count). Most Web3 prospective grants are Build: they fund the creation of a specific tool, codebase, or piece of infrastructure.

**Sub-type B (retroactive funding):** Use Retroactive obligation mode. The obligation object is prior contribution assessed against published criteria. The entry specification gate must specify: which time period the retroactive assessment covers, which categories of contribution are eligible, and which impact metrics will be used to assess those contributions. These specifications must be committed to before any application or nomination opens.

**Sub-type C (quadratic funding):** Use Build or Change obligation mode for the individual grants that the QF mechanism allocates. The QF mechanism itself (the matching pool formula, the round categories, the eligibility rules) constitutes the entry specification gate: it must be published and committed to before any contributor makes a contribution that will affect matching allocation.

### Entry Specification Gate

Before any application window opens, the following must be committed to in writing and published in a verifiable location (on-chain, on the funder's governance forum, or in a public repository with a commit hash):

**Round specification:**
- Obligation mode (Build, Change, or Retroactive)
- Total funding pool size and currency denomination
- Eligible program or project categories (scope)
- Eligibility criteria (who may apply or be nominated)
- Impact metrics that will be used at the completion gate or retroactive assessment
- Time period covered (for retroactive rounds)
- Matching formula and parameters (for QF rounds)

**On-chain identity anchor:** Every applicant must declare a primary wallet address that controls the funds if awarded. For DAOs and multi-sig structures, the governance mechanism controlling the wallet must be named and the current key holders or governance threshold stated. An application without a declarable on-chain identity anchor cannot satisfy the organizational identity declaration.

**Concurrent funding disclosure:** Web3 programs have funding sources that traditional grant frameworks do not anticipate. All of the following must be disclosed:
- Other protocol grants currently active or pending for the same scope
- Token Generation Events (TGEs), IDOs, or liquidity bootstrapping pools: any event in which the applying project has issued or plans to issue a token with an allocation to founders, contributors, or early investors constitutes a funding event requiring disclosure
- Investor funding rounds (SAFE, equity, convertible note)
- Vesting schedules and cliff dates for prior token allocations
- Pending token events with existing tokenomics or allocation schedules, even if not yet executed, are required disclosures; non-disclosure is treated as concurrent funding omission

**Public benefit mechanism:** Projects applying for public goods grants must declare which public benefit mechanism applies:
- Output production (the project produces an output available to the ecosystem without access restriction)
- Access provision (the project provides access to a service or infrastructure the ecosystem could not otherwise access)
- Condition change (the project is designed to shift a measurable ecosystem condition)
- Ecosystem shift (the project creates infrastructure that enables other public goods to be produced)

For output production and access provision claims, the access condition must be declared: the SPDX license identifier for software outputs; the access terms for non-software outputs. All-rights-reserved copyright is not compatible with a public goods claim.

### Application Gate

**Deliverable specification (Sub-type A):** Each deliverable must be specified with: a name, an operational definition of what the deliverable is, a unit of measurement (binary: delivered or not; or measurable: lines of code, test coverage, user count), a target value, and completion criteria specifying what independent confirmation of delivery looks like. Vague deliverables ("build the protocol," "improve UX") fail the specification requirement.

**Impact claim specification (Sub-type B):** Each impact category used in retroactive assessment must specify: what counts as a qualifying contribution in this category, what evidence is required to document the contribution, and what weight or scoring applies. If a metrics formula is used (as in Optimism Retro Funding 2025), the formula and all input weights must be published before the assessment period opens.

**Team identity:** All named contributors must be identified by their primary public identity in the ecosystem: GitHub handle, ENS name, or equivalent pseudonymous identity with a public contribution history. Where contributors choose full pseudonymity, the wallet address serves as the identity anchor. Contributors who exit the applying project after a grant is awarded, and whose contribution constitutes the basis of the application, must be named and the transition disclosed.

### Completion Gate

**Sub-type A:** Completion evidence is the delivered artifact. The review must confirm: the artifact exists at the specified location (repository, deployment address, documentation URL), its access condition matches the declared license, and it satisfies the operational definition stated at the entry gate. Artifacts that ship substantially different from the specification require a declared scope change before the completion gate assessment.

**Sub-type B:** Completion evidence is the documented prior contribution. Evidence must be independently verifiable: on-chain transaction records, public GitHub commit history, protocol deployment records, published documentation. Self-reported contribution claims without independent verifiability do not satisfy the completion gate.

**Sub-type C:** Completion evidence for QF rounds is the matching allocation calculation. The calculation must demonstrate that the formula committed to at the entry gate was applied without modification to the contribution data collected during the round.

### Attestation Gate and Corpus

The Attestation Corpus for Web3 grants should be structured to take advantage of on-chain verifiability:

- Round specification: committed on-chain or to a public repository with a timestamped commit hash before the round opens
- Application record: stored on-chain or in a public repository with content hash
- Completion gate determination: recorded on-chain or in a signed attestation from the review committee
- Disbursement: on-chain transaction record constitutes the final disbursement attestation

Where on-chain attestation is not available, a public governance forum post with a stable URL and timestamp serves as the minimum attestation record.

### Continuation Gate

For programs that fund recurring or multi-round grantees:

A continuing grantee must demonstrate: delivery of all prior round commitments, resolution or disclosure of all outstanding concurrent funding disclosures, and updated on-chain identity confirmation (wallet address is still under the same control mechanism as declared).

A continuing program operator must demonstrate: the entry specification gate for the new round is published before the previous round closes, and the attestation corpus for the previous round is complete and publicly accessible.

---

## Part 2: WALKRI Field Specifications

The following field specifications cover the intake fields most commonly required in Web3 and public goods grant programs. Each specification satisfies WALKRI's five pre-publication requirements: criterion intent, operational definition, response form, evidence form, compliance threshold.

---

### Field: Primary Wallet Address

**Criterion intent:** Establishes the on-chain identity anchor for the applying entity; the address that will receive grant funds if awarded and that serves as the verifiable accountability anchor throughout the grant period.

**Operational definition:** A wallet address is the cryptographic public key representation of the entity's on-chain identity. For individual contributors: the address they primarily use for on-chain activity in this ecosystem. For teams: the multi-sig or DAO governance-controlled address through which the team's treasury operates. For legal entities with on-chain operations: the address associated with the entity's primary on-chain presence.

**Response form:** A valid wallet address in the relevant chain's format (e.g., 0x... for Ethereum-compatible addresses). One primary address required. Secondary addresses (for multi-sig participants, contributor wallets) may be listed but are not required.

**Evidence form:** The address must be demonstrably controlled by the applicant: either a transaction signed from that address as part of the application process, or a public attestation linking the address to the applicant's public identity (ENS name resolution, GitHub verification, or equivalent).

**Compliance threshold:** A valid address format that is demonstrably controlled by the applicant. Addresses for which no control evidence is provided do not satisfy this field. Exchange or custodial wallet addresses that the applicant does not control do not satisfy this field.

---

### Field: Concurrent Funding Sources

**Criterion intent:** Documents all funding the applying entity or project has received or applied for that covers the same scope as this application, enabling assessment of additionality and preventing double-counting of the same work across multiple funders.

**Operational definition:** A concurrent funding source is any grant, investment, token allocation, or funding event that provides resources to the applying entity for work that overlaps with the scope of this application. This includes: other protocol treasury grants, ecosystem fund grants, accelerator investments, SAFE or equity investments, TGEs with founder or contributor token allocations, vesting schedules from prior token issuance, and any pending funding application for the same scope at another program.

**Response form:** A list of concurrent funding sources, each specifying: source name, amount or token allocation, currency or token denomination, scope of funded work, and current status (active, pending, completed). If no concurrent funding sources exist, an explicit declaration of this fact.

**Evidence form:** No external documentation required for the disclosure itself. The applicant's declaration is the evidence. Funders may cross-reference on-chain records for TGEs and token allocations to verify completeness. Non-disclosure discovered after award is treated as a material omission.

**Compliance threshold:** A disclosure that names all concurrent funding sources for the declared scope, including pending applications. A disclosure that omits a known token allocation or pending TGE does not satisfy this field. "None" is a compliant response only when the applicant has no funding sources covering the declared scope.

---

### Field: Public Benefit Mechanism and Access Condition

**Criterion intent:** Establishes what type of public benefit the project produces and under what terms the benefit is accessible to the ecosystem, enabling the funder to assess whether the public goods claim is substantive.

**Operational definition:** The public benefit mechanism is the structural means by which the project delivers benefit to the ecosystem: output production (a published artifact), access provision (an available service), condition change (a measurable ecosystem shift), or ecosystem shift (infrastructure enabling other public goods). The access condition is the terms under which the benefit is available: the SPDX identifier for software licenses, the access terms for services, or the measurement protocol for condition claims.

**Response form:** Selection of one public benefit mechanism from the four options, followed by the access condition specific to that mechanism. For output production: the SPDX license identifier (e.g., MIT, Apache-2.0, GPL-3.0) for the primary output. For access provision: the access terms (free, permissioned, or metered). For condition change or ecosystem shift: the indicator that will measure the condition.

**Evidence form:** For software outputs: the license file in the repository. For services: a terms of service or access policy document. For condition claims: a specified measurement source (on-chain analytics, user counts, developer adoption metrics).

**Compliance threshold:** A mechanism selection with a corresponding access condition that is specific enough to verify. "Open source" without a named SPDX identifier does not satisfy this field. "Public good" without a named mechanism does not satisfy this field. All-rights-reserved copyright is not compatible with a public goods output production claim.

---

### Field: Prior Work and Impact Evidence (Sub-type B: Retroactive)

**Criterion intent:** Documents the contribution being assessed for retroactive recognition, with enough specificity and verifiability that independent reviewers can confirm the contribution occurred and assess its impact.

**Operational definition:** Prior work is any contribution to the ecosystem made during the declared assessment period that falls within the eligible contribution categories published in the round specification. Impact evidence is independently verifiable documentation of the contribution and its use or adoption by the ecosystem.

**Response form:** A structured description of the contribution(s) including: what was built or contributed, when it was produced (dates and version history), where it can be found (repository URL, deployment address, documentation link), and who uses it or has used it (usage metrics, dependency counts, downstream projects). For each contribution, the applicant identifies which eligible category it falls under per the round specification.

**Evidence form:** On-chain records (deployment transaction hashes, protocol interaction counts), public GitHub commit history (repository URL with specific commits), published documentation (URL with date), protocol analytics (Dune Analytics queries, Etherscan data, or equivalent), or public forum posts and governance participation records. Self-reported impact claims without at least one independently verifiable evidence source do not satisfy this field.

**Compliance threshold:** At least one independently verifiable evidence source per claimed contribution. Evidence must correspond to the declared assessment period. Contributions made outside the assessment period do not qualify regardless of their quality. Impact evidence must demonstrate use by parties other than the applicant's own team (ecosystem adoption, not self-use).

---

### Field: Deliverable Specification (Sub-type A: Prospective)

**Criterion intent:** Specifies what the grant will produce with enough precision that completion can be independently confirmed, preventing vague deliverables from being substituted for specific commitments.

**Operational definition:** A deliverable is a specific artifact, codebase, document, or measurable outcome that will exist or be achieved by the end of the grant period. Each deliverable must be distinguishable from the general work of the project and specifically attributable to this grant's funding.

**Response form:** One or more deliverables, each specifying: a name, a description (what it is, what it does, what it is not), a location (where it will be found: repository URL, documentation site, deployed contract address), a completion criterion (how an independent reviewer can confirm it exists and meets the specification), and a target date.

**Evidence form:** At completion: the artifact at the specified location, demonstrably matching the specification. For software: a repository at the stated URL with a commit from within the grant period. For deployed contracts: a verified contract at the stated address. For documentation: a published document at the stated URL with a publication date within the grant period.

**Compliance threshold:** Each deliverable must exist at the specified location and match the operational definition stated at application. A deliverable that ships with materially reduced scope (core features absent, documentation missing, deployment not completed) does not satisfy this field without a prior scope change declaration.

---

## Part 3: Compatibility Map

This section maps the Web3/public goods program type to the frameworks in the CROSS+WALKRI compatibility corpus that are most directly applicable. The map is organized by primitive.

---

### Pre-specification Primitive

The pre-specification primitive requires that indicators, criteria, and impact metrics be committed to before any applicant submits. Web3 programs that implement this primitive:

- **Optimism Retro Funding 2025**: metrics formula and all input weights published before the assessment period opens; formula cannot change after applications are received
- **Gitcoin Grants QF rounds**: matching formula, round categories, and eligibility criteria published before the contribution window opens
- **Ethereum Foundation ESP**: assessment criteria published in grant program documentation before applications open
- **CROSS itself**: entry specification gate as the canonical implementation of this primitive

*Compatibility statements:* Optimism-Retro-Funding-Impact-Evaluation, DAOIP-5, 360Giving Data Standard, Nesta Challenge Prizes.

---

### Retroactive Obligation Mode

The retroactive obligation mode assesses past contribution rather than specifying future deliverables. Web3 programs that implement this mode most fully:

- **Optimism RetroPGF (Rounds 1-4)**: badge holder voting on demonstrated past impact
- **Optimism Retro Funding 2025**: formula-based assessment replacing subjective voting
- **Protocol Guild**: ongoing retroactive recognition of core Ethereum contributors
- **Gitcoin retroactive rounds**: community-assessed past contribution

*Compatibility statements:* Optimism-Retro-Funding-Impact-Evaluation, prior Optimism-Retro-PGF statement (Rounds 1-4).

---

### On-chain Identity Anchor

The on-chain identity anchor primitive requires a verifiable wallet address as the accountability subject. Relevant frameworks:

- **DAOIP-5**: DAO identity specification; wallet-anchored organizational identity
- **CROSS Part IV**: on-chain identity anchor as sixth organizational identity field
- **Optimism Retro Funding**: wallet address as identity anchor; attestation corpus linked to address

*Compatibility statements:* DAOIP-5, CROSS itself.

---

### Public Benefit Mechanism and Access Condition

The public benefit mechanism primitive requires a structural declaration of how public goods are produced and on what access terms. Relevant frameworks:

- **360Giving Data Standard**: machine-readable grant data as output production with open access condition
- **Open Source Observer (OSO)**: OSS contribution measurement as public goods evidence
- **CROSS Part II**: public benefit mechanism and access condition as universal required declarations

*Compatibility statements:* 360Giving, OSO-WALKRI, DAOIP-5.

---

### Quadratic Funding as Portfolio Aggregation

QF mechanisms aggregate individual contributions into a matched pool allocation using a formula that weights contributor count. This is a specific form of the portfolio aggregation primitive applied at the matching layer. Relevant frameworks:

- **Gitcoin QF**: canonical QF implementation; matching formula published before round opens
- **Octant**: ETH staking rewards converted to QF-eligible pool; OADE mapping published separately
- **clr.fund**: on-chain QF with zk-proof anonymity for contributor privacy

*Compatibility statements:* Optimism-Retro-Funding-Impact-Evaluation, relevant OADE documentation.

---

### Concurrent Funding Disclosure for Token Ecosystems

Token Generation Events, vesting schedules, and investor funding rounds are forms of concurrent funding that standard grant frameworks do not address. The CROSS concurrent funding disclosure requirement covers all of these. No external framework currently specifies this at the same level of detail; CROSS is the primary reference.

*CROSS provisions:* Part VI (concurrent funding disclosure), Part VI-A (additionality declaration for commercial and hybrid revenue architectures), Part VII-A (token generation events as required disclosure items).

---

### Portfolio-level Learning in Web3

Web3 public goods programs are still developing portfolio-level learning infrastructure. The closest exemplars outside Web3:

- **Walton Family Foundation SLED**: portfolio-level learning agenda with individual grant measures contributing to portfolio questions
- **CGIAR MELIA**: systematic learning across a distributed research portfolio
- **SBIR/STTR**: portfolio-level benchmarks applied to the funder's full program (transition rate, commercialization revenue)

These provide reference architectures for Web3 programs building toward portfolio-level impact assessment.

---

## New Primitives Relevant to Web3 Programs

**Impact Chain dependency graph (Optimism Retro Funding 2025):** Projects must declare their position in a causal chain showing how outputs contribute to downstream ecosystem outcomes. This is a specific implementation of the Theory of Change hierarchy primitive applied at the ecosystem level and enforced computationally. Programs building retroactive funding infrastructure should study this implementation.

**Human-in-the-loop override with published conditions:** The 2025 Retro Funding methodology pre-specifies conditions under which the formula-based allocation can be overridden by a committee, with override conditions published before the round opens. This is CROSS's completion gate with a pre-specified override mechanism. This pattern is new in the corpus.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
