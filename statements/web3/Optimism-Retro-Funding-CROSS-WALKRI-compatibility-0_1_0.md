---
title: Optimism Retro Funding Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - Optimism Collective Operating Manual: https://github.com/ethereum-optimism/OPerating-manual
  - Milestones and Metrics Council Charter v0.1: https://github.com/ethereum-optimism/OPerating-manual/blob/main/Milestones%20and%20Metrics%20Council%20Charter%20v0.1.md
  - Retro Funding 4 Impact Metrics specification: https://gov.optimism.io/t/retro-funding-4-impact-metrics-a-collective-experiment/8226
  - Evolution of Retro Funding 2025: https://gov.optimism.io/t/the-evolution-of-retro-funding-in-2025/9414
  - OSO Documentation: https://docs.opensource.observer
---

# Optimism Retro Funding Compatibility

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

The Optimism Collective's Retroactive Public Goods Funding program and CROSS+WALKRI address the same accountability problem from different directions. Optimism's RetroPGF recognizes work that was already done; CROSS provides the obligation architecture that specifies, in advance, what evidence of that past work must satisfy. The two systems are structurally compatible because CROSS's retroactive obligation mode was designed for exactly the pattern RetroPGF embodies: work is completed first, then recognized, with impact evaluated against published criteria rather than prospective commitments.

WALKRI reinforces this compatibility at the field level. The Milestones and Metrics Council's requirements that impact metrics be verifiable and reproducible are satisfied structurally by WALKRI's evidence form requirement, which mandates that every metric include a specified measurement instrument and a documented access path before evaluation opens.

---

## What Optimism Retro Funding Requires

The Optimism Collective's Retroactive Public Goods Funding program, governed by the Operating Manual and administered with technical infrastructure from Open Source Observer (OSO), specifies the following requirements for impact metrics used in evaluation rounds:

Metrics must be verifiable: computed from on-chain data, GitHub activity via OSO, or other independently accessible public signals. Self-reported data is not acceptable as a primary metric.

Metrics must be reproducible: any evaluator with access to the published data sources must be able to recompute the metric and arrive at the same value.

Metric specifications must be published before badgeholder evaluation opens: the Milestones and Metrics Council's charter specifies that metric definitions are fixed at the start of each round, not determined during evaluation.

Projects are evaluated against their on-chain identity: OSO registration anchors project identity to verifiable blockchain addresses, GitHub organizations, and npm packages.

---

## How CROSS Addresses These Requirements

CROSS's retroactive obligation mode governs programs where the funded work precedes the funding decision. This is the structural definition of RetroPGF: the Optimism Collective funds contributions that have already been made to the ecosystem, not contributions that are promised.

In retroactive obligation mode, CROSS's four-gate sequence operates with a modified entry gate: instead of specifying future deliverables, the entry gate specifies the evidence criteria by which past contributions will be assessed. The entry specification gate requires these criteria to be published before applications open. This satisfies the Milestones and Metrics Council's requirement that metric definitions precede evaluation.

CROSS Field 6, the on-chain identity anchor, maps directly to OSO's project registration schema. A project that has declared its on-chain identity anchor in a CROSS-conformant application has already documented the blockchain addresses and GitHub organizations that OSO uses to compute its metrics. The CROSS identity declaration and the OSO project registration are the same underlying data expressed in two formats.

CROSS's Attestation Corpus query retrieves all prior CROSS declarations associated with a grantee's on-chain identity anchor. For Optimism rounds, this cross-references the grantee's OSO registration to confirm that declared GitHub organizations, blockchain addresses, and on-chain activity signals are consistent across systems. Consistency is an independent verification of the organizational identity claim; discrepancies are a flag for review.

CROSS's Cohort Position assessment enables evaluators to compare each applicant's evidence against the distribution of the full applicant cohort. This is the structural equivalent of the badgeholder evaluation model: individual contributions are assessed relative to the other contributions in the same round, not against an absolute threshold.

---

## How WALKRI Addresses These Requirements

WALKRI's evidence form requirement specifies that every intake field must include a documented measurement instrument and an access path. For metrics computed from OSO data, the evidence form is the OSO query: the metric name, the project slug, the time window, and the OSO Data Exchange endpoint from which the value is retrieved. This satisfies Optimism's reproducibility requirement structurally: a WALKRI-conformant evidence form for an OSO-powered metric is, by definition, a reproducible query that any evaluator can run.

WALKRI's validity standard (data quality standard 5.1) requires that the data actually measure what the criterion intends to measure. This is the same requirement Optimism's verifiability standard imposes: on-chain data must correspond to the actual contribution being recognized, not a proxy that could be gamed.

WALKRI's integrity standard (data quality standard 5.2) requires that evidence collection be separated from the entity that benefits from favorable outcomes. For OSO-powered metrics, this is structurally satisfied: OSO is an independent third-party platform that computes metrics from public data without participation by the grantee. Grantees cannot modify their OSO metrics by self-reporting; the data is computed independently.

---

## OSO as the Bridge

CROSS+WALKRI has a published compatibility statement for Open Source Observer (see OSO-WALKRI-compatibility-0_1_0.md in this series). The conclusion of that statement is directly relevant here: a WALKRI-conformant recipient profile that includes the on-chain identity anchor, GitHub URL, and npm package identifiers is directly importable as an OSO oss-directory entry. Because CROSS+WALKRI is already OSO-compatible, Optimism's OSO-powered metrics are inherently CROSS+WALKRI-compatible. Programs that run CROSS-conformant rounds with WALKRI-specified OSO evidence forms produce the exact data infrastructure that Optimism RetroPGF evaluation requires.

---

## Mapping Table

| Optimism Retro Funding Requirement | CROSS Provision | WALKRI Provision |
| :-- | :-- | :-- |
| Metric definitions published before evaluation opens | Entry specification gate: criteria fixed before applications open (retroactive obligation mode) | Pre-publication field requirements: criterion intent, operational definition, and compliance threshold must be declared before the round opens |
| Metrics verifiable from independent public sources | Attestation Corpus query: cross-references on-chain data against declared identity | Validity standard (5.1): data must measure the intended criterion; Integrity standard (5.2): evidence collected independently of the beneficiary |
| Metrics reproducible by any evaluator | Gate configuration includes evidence scope and strength specification | Evidence form requirement: OSO query (metric name, project slug, time window, access path) is the reproducible measurement instrument |
| Project identity anchored to on-chain addresses and GitHub orgs | Field 6: on-chain identity anchor (blockchain address, network, protocol, tag) maps to OSO oss-directory blockchain field | WALKRI recipient profile exportable as OSO oss-directory YAML |
| Evaluation relative to cohort contributions | Cohort Position assessment | Not applicable at the field level |
| Retroactive recognition of past work | Retroactive obligation mode: entry gate specifies evidence criteria for past contributions rather than prospective deliverables | All five WALKRI data quality standards apply to retrospective evidence specification |

---

## The Pre-Funding Specification Layer

A CROSS+WALKRI-conformant Optimism round produces something Optimism's current framework does not require but would benefit from: a pre-funding specification layer that makes the metrics trustworthy before evaluation begins.

The current Optimism process publishes metric definitions before evaluation opens. CROSS+WALKRI extends this by requiring those definitions to meet the WALKRI field specification standard: each metric must have a stated criterion intent, an operational definition that specifies its exact boundary conditions, a documented evidence form with an OSO access path, and a compliance threshold. This elevates the metric definition from a name-and-description pair to a structured, auditable specification.

The result is that badgeholders evaluate contributions against metrics whose measurement instruments are documented in advance, whose access paths are independently verifiable, and whose operational definitions remove ambiguity about what counts. This is the accountability infrastructure that makes retroactive recognition trustworthy rather than discretionary.

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

Optimism Operating Manual: https://github.com/ethereum-optimism/OPerating-manual

Optimism Governance Forum: https://gov.optimism.io

Open Source Observer: https://docs.opensource.observer

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. Retroactive obligation mode alignment with RetroPGF structure. WALKRI evidence form mapped to verifiability and reproducibility requirements. OSO compatibility bridge documented. Mapping table covering entry specification gate, on-chain identity anchor, cohort position assessment, and WALKRI data quality standards. |
