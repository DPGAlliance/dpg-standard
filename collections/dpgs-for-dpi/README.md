# DPGs for DPI Collection

A DPGA Collection of open-source solutions that function as **foundational building blocks for Digital Public Infrastructure (DPI)** — the shared digital systems that enable governments and markets to operate at population scale.

**Status:** 🟢 Published

**Co-stewards:** Digital Public Goods Alliance (DPGA) Secretariat, [Co-Develop](https://www.codevelop.fund/), and the [Center for Digital Public Infrastructure (CDPI)](https://cdpi.dev/).

## Contents

- [`criteria.md`](./criteria.md) — the technical criteria a DPG must meet to be included (Layers 1–3).
- [`CHANGELOG.md`](./CHANGELOG.md) — version history of the criteria.

## Objectives

Unlike broader DPGs, solutions in this Collection are specifically designed to be **reusable across sectors, interoperable through open standards, and deployable at national scale**. The Collection helps countries identify trusted, proven open-source options for their core digital public infrastructure — covering **identity, payments, data exchange, registries, and trust services** — reducing the need to build from scratch and accelerating safe, inclusive digital transformation.

The Collection is available in the [DPG Registry](https://www.digitalpublicgoods.net/collections/coll-dpi).

## How the criteria are built

The Collection asks one focused question: *does this DPG function as a building block for digital public infrastructure — or is it general-purpose govtech?* It answers it through a layered model:

1. **Layer 1 — Prerequisite:** the solution is a recognized DPG in the [DPG Registry](https://www.digitalpublicgoods.net/registry).
2. **Layer 2 — DPI relevance:** a gateway test (domain fit, cross-sector reusability, population-scale intent). All three must be true.
3. **Layer 3 — DPI architecture alignment:** five criteria (A–E) drawn from [CDPI's DPI architecture principles](https://docs.cdpi.dev/the-dpi-wiki/dpi-tech-architecture-principles): interoperability, minimalist/reusable design, ecosystem enablement, federation readiness, and security & privacy at scale.

Full detail is in [`criteria.md`](./criteria.md).

## What we're looking for

This is a working draft. We would value community input on, in particular:

- **Domain boundaries** — are the five DPI domains (Digital Identity, Digital Payments, Data Exchange, Foundational Registries, Trust Infrastructure) and the "what is not in scope" boundary drawn in the right place?
- **Gateway test** — are *cross-sector reusability* and *population-scale intent* assessable in practice, and what evidence should demonstrate them?
- **Evidence expectations** — are the named evidence artifacts (OpenAPI specs, architecture diagrams, deployment guides, security policies, integration case studies) realistic and assessable from public documentation?
- **Federation and data sovereignty (Criterion D)** — is the bar right for solutions whose deployment topology depends on the implementing country?
- **Overlap** — anywhere the criteria unintentionally duplicate the DPG Standard or the Maturity Model rather than complementing them.

## How to contribute

1. **Discuss:** comment on the open pull request for this Collection, or open an issue.
2. **Propose changes:** open a pull request editing [`criteria.md`](./criteria.md) and add a matching entry to [`CHANGELOG.md`](./CHANGELOG.md).
3. Please follow the repository [Code of Conduct](../../CODE_OF_CONDUCT.md).

Decisions on which suggestions are integrated, adapted, or deferred are recorded so the rationale stays transparent to contributors and co-stewards.