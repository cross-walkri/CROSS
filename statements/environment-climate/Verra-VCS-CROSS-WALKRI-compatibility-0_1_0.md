---
title: Verra Verified Carbon Standard (VCS) Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.4 (github.com/CrossWalkri/CROSS), WALKRI v0.1.7 (github.com/CrossWalkri/WALKRI)
references:
  - https://verra.org/wp-content/uploads/2022/02/VCS-Standard_v4.2.pdf
  - https://verra.org/programs/verified-carbon-standard/vcs-program-details/
---

# Verra Verified Carbon Standard (VCS)

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Summary

The Verra Verified Carbon Standard (VCS), current version 4.2 (verra.org), is the primary market standard for carbon credit certification, widely applied to grant-funded conservation, land use, and clean energy projects. Its three structural primitives (additionality as a binary eligibility threshold, mandatory two-stage third-party validation and verification, and registry-based issuance of Verified Carbon Units) correspond to specific CROSS mechanisms across the entry gate, evidence taxonomy, and Attestation Corpus. WALKRI ensures that intake instruments for VCS-linked programs establish monitoring methodology, counterfactual basis, and evidence access paths in operationally defined form before any project enters the registration pipeline.

---

## The VCS's Approach

The Verra Verified Carbon Standard governs the certification of carbon emission reductions and removals for voluntary carbon market participation. It is the dominant standard for this purpose globally, covering projects in agriculture, forestry, and land use; renewable energy; waste management; transportation; and industrial processes. Grant-funded conservation, land-use change, and clean energy projects frequently use VCS certification alongside their development grant frameworks, either because funders require it as a condition of grant eligibility or because projects seek the additional revenue stream that carbon credit issuance provides.

The first distinctive primitive of VCS is additionality. Additionality is a binary eligibility threshold, not a performance metric: either a project produces measurable emission reductions beyond what would have occurred in the absence of the project, or it does not qualify for VCS registration. Additionality assessment is conducted before registration, not after. A project that cannot demonstrate additionality cannot enter the VCS program regardless of how well it subsequently performs against its own targets. The additionality test requires a counterfactual baseline analysis: what would the emissions trajectory have been without the project, and can the project demonstrate that its intervention changes that trajectory in a measurable, attributable way?

The second distinctive primitive is the mandatory two-stage third-party review by an accredited Validation and Verification Body (VVB). The two stages are structurally distinct: validation occurs before implementation, when a VVB reviews the Project Description to assess whether the project design, methodology selection, and additionality argument are valid; verification occurs after monitoring, when a VVB reviews the Monitoring Report to assess whether the data collected, the emission reductions calculated, and the methodology application are accurate. Both stages are conducted by accredited bodies; both produce formal assessment documents; both are required for any project proceeding through the full VCS cycle. The two-stage structure ensures that project design integrity and implementation fidelity are assessed independently and at the appropriate stage.

The third distinctive primitive is registry-based issuance of Verified Carbon Units (VCUs). VCUs are the structured, publicly recorded output of the VCS verification process: each VCU represents one tonne of CO2 equivalent emission reduction or removal, and each is uniquely identified, serialized, and recorded in the Verra registry. The registry is publicly queryable; any VCU's status (issued, retired, cancelled) is visible. This makes the registry a public, persistent record of verified claims, not merely an administrative database.

The VCS project cycle in full: a project developer designs the project using an approved VCS methodology, prepares a Project Description, submits to a VVB for validation, registers the validated project in the Verra registry, implements and monitors according to the approved methodology, prepares a Monitoring Report, submits to a VVB for verification, and receives VCU issuance upon successful verification. Each step produces a formal document; each document is recorded or referenced in the registry.

---

## How CROSS Satisfies the VCS

The VCS additionality requirement maps to the CROSS causality stance field combined with the additionality argument at the entry gate. Under CROSS, programs must declare their causal position before any application opens: the intervention produces measurable change beyond what would have occurred without it, and the counterfactual basis for that claim is specified. This is the structural equivalent of VCS additionality assessment conducted at entry: the claim is made and documented before any implementation commitment is made, not asserted post-hoc after results are in hand. The CROSS entry gate additionality documentation becomes the pre-commitment record against which the VVB validation review assesses the project's additionality argument.

The VCS third-party VVB validation stage (pre-implementation) maps to the CROSS entry specification gate evidence quality combined with the pre-commitment record. Under CROSS, the entry gate requires that methodology selection, indicator specification, counterfactual baseline, and outcome targets be documented and made publicly available before any application is submitted. This is the same set of design-stage documentation that VVB validation reviews. A CROSS-compliant entry gate produces the documentation that VVB validation requires; the VVB validation is the independent assessment event that moves the entry gate documentation to the independent attestation tier of the CROSS evidence strength taxonomy.

The VCS third-party VVB verification stage (post-monitoring) maps to the CROSS completion gate combined with the independent attestation pathway at the highest evidence strength tier. The completion gate requires structured documentation of what was monitored, against what baseline, using which methodology, with what evidence of results. The VVB verification review is the independent attestation event applied to that completion gate documentation. Together, CROSS completion gate plus VVB verification equals the highest evidence strength tier in CROSS: evidence produced by the program, reviewed and attested by an accredited independent body, with documentation retained in the Attestation Corpus.

The VCS Monitoring Report maps to the CROSS completion gate evidence package: structured documentation of what was monitored (indicator by indicator), against what baseline (the counterfactual established at entry), using which approved methodology, with what quantified result. The CROSS requirement that completion gate evidence specify the methodology used and the baseline against which results are measured is exactly the content of the VCS Monitoring Report.

The Verra registry-based VCU issuance maps to the CROSS Attestation Corpus. Both are persistent, publicly queryable records of verified claims. The Verra registry records the outcome of the VCS verification process; the CROSS Attestation Corpus records the complete gate history from design through to completion gate determination. Together they provide an end-to-end public record: the Attestation Corpus documents the design commitments and intermediate gate decisions; the Verra registry documents the independently verified outcome.

| VCS Requirement | CROSS Mechanism |
|---|---|
| Additionality (binary eligibility threshold, pre-registration) | CROSS causality stance field + additionality argument at entry gate |
| VVB validation (pre-implementation third-party review of design) | CROSS entry gate pre-commitment record + independent attestation pathway |
| VVB verification (post-monitoring third-party review of results) | CROSS completion gate evidence + independent attestation pathway (highest tier) |
| Monitoring Report (structured post-monitoring evidence package) | CROSS completion gate documentation requirements |
| Verra registry (persistent public record of verified claims) | CROSS Attestation Corpus (gate records; persistent and publicly queryable) |
| Approved methodology requirement | CROSS indicator specification Fields 6-7 (data source and collection method) |

---

## How WALKRI Complements This Alignment

WALKRI ensures that intake instruments for VCS-linked programs establish monitoring methodology, counterfactual basis, and evidence access paths as operationally defined measurement instruments before any project enters the VCS registration pipeline. In a VCS context, this is consequential at the validation stage: VVB validators assess whether the project's monitoring plan specifies the methodology clearly enough that verification will be possible after monitoring. A WALKRI-compliant intake instrument does this systematically: for each outcome indicator, it specifies which VCS-approved methodology applies, what monitoring parameters are required, what data sources will be used, what chain of custody applies to monitoring data, and what verification pathway will be used.

This prevents the common failure mode in which projects pass VVB validation with insufficiently specified monitoring plans, then fail VVB verification because the monitoring data produced does not match the methodology's requirements. WALKRI moves the methodology specification upstream, into the intake design stage, so that the gap between validation-approved design and verification-ready data is identified and closed before project registration, not discovered during the verification process when the costs of non-compliance are highest.

---

*Published under CC0. For the current version of CROSS and WALKRI, see github.com/CrossWalkri.*
