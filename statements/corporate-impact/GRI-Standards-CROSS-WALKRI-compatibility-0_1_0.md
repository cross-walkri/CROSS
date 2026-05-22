---
title: GRI Standards Compatibility - CROSS+WALKRI
version: 0.1.0
date: 2026-05-18
license: CC0
standards: CROSS v0.4.0 (github.com/CrossWalkri/CROSS), WALKRI v0.1.6 (github.com/CrossWalkri/WALKRI)
references:
  - GRI 1: Foundation 2021, https://www.globalreporting.org/standards/
  - GRI 2: General Disclosures 2021
  - GRI 3: Material Topics 2021
  - Global Reporting Initiative Standards Overview, https://www.globalreporting.org/standards/
---

# GRI Standards Compatibility - Partial Alignment

## CROSS+WALKRI Compatibility Statement v0.1.0

---

## Scope and Limitations of This Statement

This statement documents partial alignment between CROSS+WALKRI and the GRI Universal Standards (GRI 1: Foundation, GRI 2: General Disclosures, GRI 3: Material Topics). The alignment is genuine where it exists and is stated precisely. Where GRI and CROSS+WALKRI do not align, this statement says so without hedging.

GRI is primarily an enterprise-level sustainability reporting framework used by more than 14,000 organizations globally. It covers the full scope of organizational impacts: governance, stakeholder engagement, environmental performance (including Scope 1, 2, and 3 emissions), supply chain, labor practices, human rights, and board composition. CROSS+WALKRI governs grant program obligation architecture and indicator field specification at the level of individual grant rounds. These are different objects of disclosure operating at different organizational scales.

Claiming full GRI alignment for a CROSS+WALKRI-conformant grant program would be overclaiming. This statement does not make that claim. It identifies where the two frameworks address the same requirements, states where they diverge, and provides guidance for programs whose funders or grantees are also subject to GRI reporting obligations.

---

## Where Alignment Exists

### GRI 2: Governance and Stakeholder Engagement

GRI 2 requires organizations to disclose governance structure and oversight arrangements, stakeholder identification and engagement methods, and the organization's policies and practices regarding material topics. Three of these requirements have functional equivalents in CROSS.

CROSS's organizational identity declaration (the on-chain identity anchor required at program entry) satisfies GRI 2's requirement for governance structure disclosure at the program level. The identity anchor establishes the canonical organizational identity, the grant authority, and the program's relationship to its administering institution.

CROSS's coherence disclosure requirement, which requires programs to declare how the program relates to other interventions addressing the same problem area, addresses GRI 2's stakeholder engagement dimension at the program level. Programs must map their activities against the broader landscape of related work, which is the analytical basis for the kind of stakeholder and peer-organization engagement GRI 2's disclosure requirements address.

The limits of this alignment should be stated plainly. GRI 2's governance disclosure covers board composition, remuneration, and organizational decision-making structures across the entire organization. CROSS's identity anchor establishes program-level governance documentation. These are not the same scope.

### GRI 3: Material Topics and Double Materiality

GRI 3 requires organizations to conduct a double materiality assessment: identifying which topics are material because they affect the organization financially, and which topics are material because the organization's activities affect the world. Material topics must be clearly defined before data is collected, and the scope and boundary of each material topic must be documented.

WALKRI's criterion intent and operational definition requirements address GRI 3's requirement that material topics be clearly defined before data is collected. A WALKRI-conformant intake field requires a stated criterion intent (why this criterion is being assessed and what decision it informs), an operational definition (the precise boundary conditions of the criterion), and a compliance threshold (the minimum acceptable response). This is the field-level equivalent of GRI 3's material topic definition: scope, boundary, and decision relevance must all be declared before measurement begins.

CROSS's Theory of Change declaration addresses the "impact on the world" dimension of GRI 3's double materiality at the program level. The Theory of Change pathway is a causal argument about how the program's activities produce real-world change; this is the program-level equivalent of the impact materiality assessment GRI 3 requires organizations to conduct across all their activities.

---

## Where Alignment Does Not Exist

The full GRI reporting suite covers organizational-level disclosures that are outside the scope of individual grant rounds and outside the scope of CROSS+WALKRI entirely. These include:

Scope 1, 2, and 3 greenhouse gas emissions (GRI 305). CROSS does not govern environmental impact measurement of the grant administrator's operations.

Supply chain disclosures (GRI 204, GRI 308, GRI 414). CROSS governs program obligations, not procurement relationships or supplier assessments.

Board composition, remuneration, and governance (GRI 2 governance sections). CROSS's organizational identity anchor is program-level documentation, not organizational governance disclosure.

Labor practices and human rights (GRI 400 series). CROSS does not govern employment conditions or human rights due diligence.

These are not gaps in CROSS+WALKRI. They are features of a different object of disclosure. Grant program accountability frameworks and enterprise sustainability reporting frameworks address different questions at different organizational scales.

---

## Using Field 10 for GRI Alignment Declarations

Programs in which the funder or grantee is also subject to GRI reporting can use CROSS Field 10 (institutional framework alignment) to declare GRI alignment and record applicable GRI Standards. Where a program's indicators address topics that are also material under GRI 3, declaring the relevant GRI Standard reference in Field 10 makes that alignment explicit and auditable.

This declaration is a cross-reference, not a compliance claim. It records that the program's indicator addresses a topic that is also a GRI material topic, enabling organizations that report under both frameworks to trace the connection between their program-level accountability and their enterprise-level GRI disclosures.

---

## Partial Alignment Summary

| GRI Requirement | CROSS+WALKRI Provision | Alignment |
| :-- | :-- | :-- |
| GRI 2: Governance structure disclosure | CROSS organizational identity declaration | Partial: program-level only, not organizational governance |
| GRI 2: Stakeholder engagement documentation | CROSS coherence disclosure requirement | Partial: landscape mapping, not full stakeholder engagement process |
| GRI 3: Material topic definition before data collection | WALKRI criterion intent and operational definition | Functional alignment at field level |
| GRI 3: Impact materiality | CROSS Theory of Change declaration | Functional alignment at program level |
| GRI 305: Emissions | No CROSS+WALKRI equivalent | Outside scope |
| GRI 200/400 series: Financial and social enterprise disclosures | No CROSS+WALKRI equivalent | Outside scope |
| GRI 2: Board composition and remuneration | No CROSS+WALKRI equivalent | Outside scope |

---

## Further Information

CROSS: github.com/CrossWalkri/CROSS

WALKRI: github.com/CrossWalkri/WALKRI

GRI Standards: https://www.globalreporting.org/standards/

License: CC0

---

## Changelog

| Version | Date | Summary |
|---|---|---|
| 0.1.0 | 2026-05-18 | Initial draft. Partial alignment documented for GRI 2 governance and stakeholder engagement, and GRI 3 material topic definition. Out-of-scope GRI requirements listed explicitly. Field 10 guidance for cross-reference declarations. Alignment summary table. |
