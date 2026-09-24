# DPGs for DPI — Technical Criteria

**Status:** Published · **Version:** 1.0
**Co-stewards:** Digital Public Goods Alliance (DPGA) Secretariat, [Co-Develop](https://www.codevelop.fund/), and the [Center for Digital Public Infrastructure (CDPI)](https://cdpi.dev/).

> See [`CHANGELOG.md`](./CHANGELOG.md) for version history and the pull request thread for the discussion that produced it.

---

## Purpose

This document defines and aligns the technical criteria that help identify digital public goods (DPGs) that enable digital public infrastructure (DPI). It also establishes a shared understanding and process for determining which DPGs are included in the DPGs for DPI Collection.

The Collection brings together open-source solutions that function as foundational building blocks for DPI — the shared digital systems that enable governments and markets to operate at population scale. Unlike broader DPGs, solutions in this collection are specifically designed to be reusable across sectors, interoperable by open standards, and deployable at a national scale. The Collection exists to help countries identify trusted, proven open-source software options for their core digital public infrastructure — covering identity, payments, data exchange, registries, and trust services — reducing the need to build from scratch and accelerating safe, inclusive digital transformation.

The public collection is available in the [DPG Registry](https://www.digitalpublicgoods.net/collections/coll-dpi).

### Definitions

| Term | Definition | Source |
| :-- | :-- | :-- |
| Digital Public Infrastructure (DPI) | Foundational, digital building blocks designed for the public benefit. Systems built as DPI can comprise digital software, platforms, APIs, and services, along with their related legal and regulatory frameworks, standards, policies, and processes. | [World Bank, 2025](https://documents.worldbank.org/en/publication/documents-reports/documentdetail/099031025172027713) |
| Digital Public Good (DPG) | Open-source software, open data, open AI models, open standards, and open content that adhere to privacy and other applicable laws and best practices, do no harm by design, and help attain the SDGs. | [DPGA / UN Secretary-General's Roadmap for Digital Cooperation](https://digitalpublicgoods.net/standard) |
| Building Block | A reusable software component that provides a key digital functionality and can be used across multiple use cases and sectors. | Adapted from GovStack / World Bank |

### Co-stewards

- [Digital Public Goods Alliance](https://digitalpublicgoods.net/) — ecosystem alignment for DPGs and DPI.
- [Co-Develop](https://www.codevelop.fund/) — funding for DPGs for DPI.
- [CDPI](https://cdpi.dev/) — technical advisory for DPI design and implementation.

---

## How these criteria work

This document is a **supplementary lens** applied on top of the frameworks DPGs are already expected to comply with. It does **not** re-assess what those frameworks already cover; each criterion specifies only the *additional, DPI-specific* expectation.

| Framework | What it covers | Obligation |
| :-- | :-- | :-- |
| [DPG Standard](https://digitalpublicgoods.net/standard/) | Open licensing, SDG relevance, ownership, platform independence, documentation, data extraction, privacy & applicable laws, open standards, do no harm | **Prerequisite** — must be met before applying these criteria |
| [DPG Maturity Model](https://github.com/ricardomiron/dpg-maturity-indicators/blob/main/indicators/core-indicators.md) (self-assessment) | Governance, community, QA, security, deployment readiness, documentation, accessibility, interoperability, support, adoption | **Complementary** — assessed separately to track growth |
| Validation and enrichment of DPG deployment data | Independently validating and enriching DPG Registry deployment data (see [Related workstream](#related-workstream-deployment-data-validation)) | **Complementary** — validated independently for research purposes |

These criteria ask one focused question:

> *Does this DPG function as a building block for digital public infrastructure — or is it general-purpose govtech?*

---

## Layer 1 — Prerequisite: Recognized Digital Public Good

The solution must be a recognized DPG in the [DPG Registry](https://www.digitalpublicgoods.net/registry). **DPG Standard compliance is a precondition** for inclusion in this collection.

---

## Layer 2 — DPI Relevance

Refers to solutions that enable the effective provision of population-scale functions and services usable across both the public and private sectors.

Drawing on the [World Bank DPI framework](https://documents.worldbank.org/en/publication/documents-reports/documentdetail/099031025172027713) and aligned with [Co-Develop](https://www.codevelop.fund/insights-1/what-is-digital-public-infrastructure) and [CDPI](https://docs.cdpi.dev/the-dpi-wiki/dpi-overview) definitions, DPGs must provide functionalities central to one or more of the following DPI domains:

| Domain | What it includes | Examples |
| :-- | :-- | :-- |
| **Core domains** | | |
| **Digital Identity** | Identity management, authentication, authorization, ID verification, eKYC, single sign-on | MOSIP |
| **Digital Payments** | Payment orchestration, instant payments, P2P/P2M/G2P transfers, core banking, mobile money interoperability | Apache Fineract, Mojaloop |
| **Data Exchange** | Information mediation, secure data sharing between systems, data gateways, API gateways | X-Road |
| **Technology enablers** | | |
| **Foundational Registries** | Civil registries, population registries, social protection registries, functional registries, beneficiary management | OpenCRVS, OpenG2P |
| **Trust Infrastructure** | e-Signatures, Public Key Infrastructure (PKI), verifiable credentials, consent management, digital wallets | Inji, CREDEBL |

> **What is NOT in scope:** Sector-specific applications (e.g. a health records app, a learning management system, a tax filing portal) are valuable DPGs but are not foundational DPI building blocks unless they also expose infrastructure-layer capabilities reusable across sectors. A solution that only serves a single sector without providing cross-cutting, reusable capabilities is general-purpose govtech, not DPI.

**All three of the following must be true to proceed to Layer 3:**

1. **Domain fit.** The solution provides functions and services in at least one of the five DPI domains above.
2. **Cross-sector reusability.** The solution's core capabilities can be used by multiple sectors, departments, or actors (public and private) without requiring sector-specific modifications to its core.
3. **Population-scale intent.** The solution is designed to operate at national or population scale, rather than for a specific project, pilot, or institution.

---

## Layer 3 — DPI Architecture Alignment

Refers to the solution's architecture aligning with the technical principles that distinguish DPI from conventional digitization, drawn from [CDPI's DPI architecture principles](https://docs.cdpi.dev/the-dpi-wiki/dpi-tech-architecture-principles) and [Co-Develop's work](https://www.codevelop.fund/insights-1/what-is-digital-public-infrastructure).

Where the criteria below overlap with the DPG Standard or Maturity Model, the requirement specifies the **additional, DPI-specific expectation** beyond what those frameworks already require. **All five criteria (A–E) are required.**

### A. Interoperability through open specifications

*Can other systems connect to yours without modifying your core, using documented open standards?*

| # | Requirement | Evidence |
| :-- | :-- | :-- |
| **A1** | Externally accessible APIs documented using a standard specification (e.g. OpenAPI, AsyncAPI) | Link to API documentation |
| **A2** | Use of domain-relevant open standards, protocols, and specifications (e.g. OAuth 2.0, OpenID Connect, FIDO2, ISO 20022, HL7 FHIR, W3C Verifiable Credentials, SCIM, X-Road protocol) | List of standards adopted, with links |
| **A3** | Data exchanged in open, non-proprietary formats (e.g. JSON, XML, CSV) with published schemas | Link to data schemas or format documentation |

> *Beyond DPG Standard/Maturity:* The DPG Standard (Indicator 8) requires adherence to open standards generically. The Maturity Model (4.1, 4.2) assesses standards adoption and integration readiness. This criterion raises the bar for DPI by requiring *externally published API specifications* that enable third parties to integrate without coordination with the product owner — a necessary condition for functioning as shared infrastructure.

### B. Minimalist and reusable building block design

*Is your solution designed as a modular building block that does one thing well, rather than a monolithic platform?*

| # | Requirement | Evidence |
| :-- | :-- | :-- |
| **B1** | Modular architecture that allows components to be deployed, updated, or replaced independently (e.g. microservices) | Architecture documentation or diagram |
| **B2** | Clear separation between the infrastructure layer (the reusable building block) and any application layer built on top | Documentation distinguishing core vs. application components |
| **B3** | Configuration-driven adaptability — deployable in different country contexts without forking the codebase | Configuration/customization documentation |

> *Beyond DPG Standard/Maturity:* The Maturity Model (2.3) assesses architecture and extensibility. This criterion adds the DPI-specific expectation of *minimalist design* — the solution should do one foundational thing well and expose it for reuse, rather than bundling many features into an all-in-one platform.

### C. Ecosystem enablement

*Does your architecture actively enable a diverse ecosystem of public and private actors to build on top of it?*

| # | Requirement | Evidence |
| :-- | :-- | :-- |
| **C1** | Third-party developers or organizations can build services on top of the solution using documented extension points, APIs, or SDKs | Developer documentation, SDK, or sandbox/testing environment |
| **C2** | At least one documented instance of an external organization integrating with or building on the solution | Case study, partner reference, or integration example |
| **C3** | No architectural constraints that restrict use to a single implementing organization or vendor | Statement or evidence of multi-actor deployability |

> *Beyond DPG Standard/Maturity:* The Maturity Model (6.2) tracks the vendor/implementer ecosystem as an optional indicator. For DPI, ecosystem enablement is not optional — it is a defining characteristic. A system that can only be used by its creator is not functioning as infrastructure.

### D. Federation and decentralization readiness

*Can your solution operate in distributed or federated deployment models appropriate for national-scale infrastructure?*

| # | Requirement | Evidence |
| :-- | :-- | :-- |
| **D1** | Supports federated, distributed, or multi-instance deployment rather than requiring a single central instance | Architecture documentation describing deployment topology |
| **D2** | Data sovereignty: data can remain within jurisdictional boundaries as required | Documentation on data residency options |
| **D3** | High-availability configurations that avoid single points of failure | Deployment guide or infrastructure documentation |

> *Beyond DPG Standard/Maturity:* Neither the DPG Standard nor the Maturity Model specifically addresses federation or decentralization. This is a DPI-specific architectural requirement reflecting that national infrastructure must respect jurisdictional boundaries and avoid centralizing all data or control in a single node.

### E. Security and privacy at infrastructure scale

*Does your solution meet the elevated security and privacy requirements appropriate for population-scale infrastructure?*

| # | Requirement | Evidence |
| :-- | :-- | :-- |
| **E1** | Security practices appropriate for national-scale deployment: encryption at rest and in transit, role-based access control, and audit logging | Security documentation or `SECURITY.md` |
| **E2** | Published vulnerability disclosure process and evidence of regular security assessments | Link to security policy and/or audit reports |
| **E3** | Privacy by design: data minimization, consent mechanisms, and support for applicable data protection regulations across jurisdictions | Privacy documentation or data protection impact assessment |

> *Beyond DPG Standard/Maturity:* The DPG Standard (Indicators 7, 9) covers privacy, applicable laws, and do-no-harm. The Maturity Model (2.2) assesses security practices. This criterion specifies the *infrastructure-grade* expectations: audit logging for accountability at population scale, cross-jurisdictional regulatory adaptability, and evidence of proactive security assessment — not just reactive vulnerability handling.

---

## Summary self-assessment checklist

Use this checklist to evaluate a solution's eligibility for the DPGs for DPI collection.

**Layer 1 — Recognized DPG**

- [ ] Solution is a recognized Digital Public Good in the DPG Registry

**Layer 2 — DPI relevance** *(all required)*

- [ ] Provides capabilities in at least one DPI domain (Identity, Payments, Data Exchange, Registries, Trust Infrastructure)
- [ ] Core capabilities are reusable across sectors without sector-specific core modifications
- [ ] Designed for national or population-scale operation

**Layer 3 — DPI architecture alignment** *(all required)*

- [ ] **A. Interoperability:** externally documented APIs using open specifications; domain-relevant standards adopted; open data formats with published schemas
- [ ] **B. Minimalist/reusable:** modular architecture; clear core vs. application separation; configuration-driven country adaptability
- [ ] **C. Ecosystem enablement:** third-party buildability via APIs/SDKs/extension points; at least one external integration; no single-vendor architectural lock-in
- [ ] **D. Federation ready:** supports distributed/federated deployment; respects data sovereignty; avoids single points of failure
- [ ] **E. Security & privacy at scale:** infrastructure-grade security practices; published vulnerability disclosure; privacy by design with cross-jurisdictional adaptability

---

## How to contribute

Open an issue or comment on the open pull request for this collection. We are especially looking for input on the points listed in the collection [`README.md`](./README.md#what-were-looking-for). Substantive changes are recorded in [`CHANGELOG.md`](./CHANGELOG.md).