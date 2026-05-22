---
title: Gitcoin Passport Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-16
license: CC0
standards: CROSS v0.3.7 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - Gitcoin Passport (passport.gitcoin.co)
  - Passport API (api.scorer.gitcoin.co)
  - Ethereum Attestation Service on Optimism (attest.sh)
  - Gitcoin (gitcoin.co)
programs: Gitcoin Grants, Octant, and any sybil-resistant Web3 grants program
---

# Gitcoin Passport Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

Gitcoin Passport and CROSS+WALKRI address different problems in the grants accountability stack. Passport is a sybil resistance and identity aggregation system: it aggregates verified credentials from multiple identity providers into a portable identity record and produces a score that programs use to gate participation. CROSS is an obligation architecture standard: it specifies what funded interventions must demonstrate and at which gate. WALKRI is a field specification quality standard: it specifies how collection instruments must be designed before applicants see them.

Passport and CROSS+WALKRI are complementary rather than overlapping. Passport answers the question of whether a participant is a unique, non-duplicate human with verifiable connections to real activity. CROSS answers the question of what that participant must demonstrate once they are accepted into a program. The two systems operate in sequence: Passport addresses the eligibility layer before obligation assessment begins; CROSS addresses the obligation layer once eligibility is established.

---

## What Gitcoin Passport Is

Gitcoin Passport is an identity aggregation system that allows any address-holder to accumulate verified credentials (called stamps) from multiple identity providers and carry them as a portable identity record. The Passport is designed to address sybil attacks in quadratic funding and comparable allocation mechanisms where each participant's unique humanity affects the allocation outcome.

**Stamps** are verifiable credentials issued by identity providers, attesting that the holder has a verified account or real-world connection. Examples include: GitHub account verification (attests developer activity), Twitter/X verification, ENS name ownership, Coinbase account (KYC-adjacent), Google account, Discord activity, proof-of-humanity protocols, and on-chain activity signals. Each stamp contributes a weighted score to the holder's Passport total.

**The Passport score** is the weighted sum of a holder's stamps. Programs set a minimum score threshold for participation. A participant who meets the threshold is treated as a verified unique human for the purposes of the program's allocation mechanism. Programs using quadratic funding weight votes or donations only from participants who meet the threshold.

**On-chain Passport records** are expressed as verifiable attestations anchored on Optimism via the Ethereum Attestation Service. The on-chain record links a wallet address to a score at a point in time and is publicly queryable. Off-chain passport data is also queryable through the Passport API.

**The Passport API** allows programs to query passport scores programmatically without requiring participants to share identity documents. The API returns a score and a breakdown of contributing stamps for any address.

---

## What Gitcoin Passport Does Not Provide

Passport establishes that a participant is a likely unique, non-duplicate human with verifiable real-world connections. It does not specify what that participant must demonstrate once accepted into a program, what evidence standards govern those demonstrations, how reviewers must document their determinations, or what the accountability record of a funded cycle must contain.

This is the boundary where CROSS begins. Passport governs the eligibility gate before obligation assessment. CROSS governs the obligation architecture once a participant is accepted as eligible. A program can run sybil-resistant QF using Passport scoring and simultaneously apply CROSS obligation architecture to the grants it funds. The two systems address consecutive questions rather than overlapping ones.

Passport also does not provide field specification quality for the forms that collect applicant data beyond the sybil resistance layer. The application fields that collect a grantee's proposed indicators, baselines, and evidence plans exist above the Passport layer and are not governed by Passport's stamp system. WALKRI addresses the specification quality of those fields.

---

## Interface Points

### Sybil Resistance as Entry Gate Input

CROSS's entry gate specifies the eligibility criteria an applicant must satisfy before a grant is awarded. Passport score threshold is an appropriate eligibility input at the CROSS entry gate, specifically in programs where unique-human participation is required for the allocation mechanism to function as intended (quadratic funding and comparable participation-weighted allocation).

A CROSS-conformant program incorporating Passport should declare the Passport score threshold in the round configuration as an explicit eligibility criterion: the threshold, the date at which it is measured, the scoring model version used, and the stamps that contribute to threshold eligibility. This makes the eligibility criterion independently verifiable rather than a black-box filter.

Where Passport is used as an entry gate filter, it should be declared in the CROSS round configuration as a sybil-resistance eligibility criterion, not as a measure of impact or obligation fulfillment. Passport score is a proxy for unique humanity; it is not an accountability metric.

### Passport Stamps as Organizational Identity Corroboration

CROSS requires applicants to submit an organizational identity declaration: the legal entity (or individual, for unincorporated contributors), the jurisdiction, the primary representative, and prior round history in this and comparable programs.

Passport stamps provide corroborating evidence for specific elements of this declaration:

A GitHub stamp attests that the declared primary representative has a verified GitHub account with real activity. For build-obligation grants proposing software development, this is a relevant corroboration of the capability claim embedded in the organizational identity declaration.

A prior Gitcoin Grants participation stamp (where available) provides verifiable evidence of prior program participation, corroborating the prior round history field in the organizational identity declaration.

An ENS name stamp provides a persistent on-chain identity anchor for the representative, which can corroborate the stability and continuity claims in the organizational identity declaration.

These stamps are corroboration, not substitutes for the organizational identity declaration. A Passport score does not replace the obligation to disclose prior round history, legal entity structure, or representative authority. But where stamps are available, they strengthen the independently verifiable basis for the identity claims made in the declaration.

### Passport Score as a WALKRI-Calibrated Field

Where a program's application form collects Passport score as an input field, that field is subject to WALKRI calibration in the same way as any other collection instrument. A WALKRI-conformant Passport score field must specify:

Criterion intent: what the field is intended to measure (sybil resistance as a proxy for unique human participation, not impact or capability).

Operational definition: which Passport scoring model is used, which stamp categories contribute to the score, how the score is computed from stamps, and at what point in time the score is measured.

Response form justification: why a numeric score with a binary threshold is the appropriate form for this criterion (rather than, for example, a stamp-by-stamp disclosure).

Evidence form: how the program verifies the score (API query, on-chain attestation query, or self-reported with verification).

Compliance threshold: the minimum score required and what happens at the boundary (do participants just below the threshold have any remediation path, and if so, what is it?).

Failure to specify these five elements for a Passport score field produces the same data quality problem as any other underspecified field: definitional variance across applications and reviewers, and an accountability record that cannot be independently verified.

---

## The Threshold Logic Comparison

Passport's score threshold mechanism and WALKRI's compliance threshold are structurally similar: both define a quantitative minimum that separates pass from fail. But they operate on different criteria and at different stages.

Passport's threshold governs eligibility before obligation assessment: does this participant meet the sybil resistance bar to enter the program?

WALKRI's compliance threshold governs collection field design before data collection begins: does this criterion specification meet the quality bar to be presented to applicants?

Both are binary gates with a quantitative minimum, but they operate at different layers and should not be conflated. A high Passport score does not relax WALKRI field specification requirements, and a well-specified WALKRI field does not substitute for Passport sybil resistance.

---

## What This Integration Enables

A program using Gitcoin Passport and CROSS+WALKRI together produces a layered eligibility and accountability record:

**Gitcoin Passport provides:** Sybil-resistant eligibility verification that the participant is a likely unique, non-duplicate human with verifiable real-world connections. This layer prevents gaming of participation-weighted allocation mechanisms and provides independently verifiable stamps that can corroborate organizational identity claims.

**CROSS provides:** The obligation architecture governing what applicants must demonstrate once their eligibility is established, what evidence standards apply to those demonstrations, and what the accountability record of the funded cycle must contain. This layer makes funded grants accountable for stated outcomes, not merely eligible to participate.

**WALKRI provides:** The field specification quality layer ensuring that the application forms collecting CROSS-required demonstrations are precisely enough defined to produce reliable, comparable data across the applicant cohort.

Together: Passport establishes who is eligible to participate; CROSS specifies what they are obligated to demonstrate; WALKRI ensures the instruments collecting those demonstrations are reliable. These three questions require different systems and are not interchangeable.

---

## Adoption Guidance

Programs using Gitcoin Passport and adopting CROSS+WALKRI should:

1. Declare the Passport eligibility threshold in the CROSS round configuration as an explicit entry gate criterion. Specify the scoring model version, the threshold value, and the measurement date. This makes the sybil resistance filter independently verifiable and documented in the accountability specification.

2. Do not treat Passport score as an obligation fulfillment metric. A high Passport score is a sybil resistance signal; it does not substitute for the evidence requirements at any CROSS gate. The organizational identity declaration, prior round history, and gate evidence requirements apply to all participants regardless of Passport score.

3. Where the application form collects Passport score as a field, apply WALKRI calibration to that field. Specify criterion intent (sybil resistance, not impact), operational definition (scoring model and stamp composition), evidence form (API or on-chain query), and compliance threshold (minimum score with boundary policy).

4. Use relevant Passport stamps as corroborating sources for the organizational identity declaration. GitHub stamps, prior Gitcoin participation stamps, and ENS name stamps are verifiable independent records that can strengthen the independently verifiable basis for identity claims.

5. Where returning applicants have Passport records from prior rounds, include Passport history as a data point in the continuation gate review. Prior participation stamps and score history provide a publicly verifiable record of ongoing engagement that is relevant to the track record assessment at the continuation gate.

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

Gitcoin Passport: passport.gitcoin.co

Passport API: api.scorer.gitcoin.co

Gitcoin documentation: docs.gitcoin.co

License: CC0
