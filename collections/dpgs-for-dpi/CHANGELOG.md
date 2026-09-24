# Changelog — DPGs for DPI Collection criteria

All notable changes to the DPGs for DPI [`criteria.md`](./criteria.md) are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this collection's criteria aim to follow [Semantic Versioning](https://semver.org/) (MAJOR = a change to which criteria are mandatory; MINOR = added/clarified criteria or evidence; PATCH = editorial fixes).

## [0.1] - Unreleased

- Initial draft criteria.

## [1.0] — Published

Supersedes the earlier unversioned working criteria (five flat criteria: society-wide, foundational/modular/reusable, interoperable, inclusive and accessible, secure and private by design).

### Added

- Explicit purpose statement, definitions (DPI, DPG, Building Block), and a table showing how the criteria sit alongside the DPG Standard and the DPG Maturity Model.
- A "what is not in scope" boundary distinguishing DPI building blocks from general-purpose govtech.
- "Beyond DPG Standard/Maturity" notes on each Layer 3 criterion, stating the additional DPI-specific expectation.
- Summary self-assessment checklist.

### Changed

- **Layered model.** Reorganised into Layer 1 (DPG Registry prerequisite), Layer 2 (DPI relevance gateway) and Layer 3 (DPI architecture alignment).
- **Domain fit is now a gateway test** in Layer 2, separated from the architecture criteria, so a solution outside the DPI domains does not need to read further.
- **DPI domains expanded from four to five**, using the World Bank DPI framework as the basis. Verifiable credentials, consent management and wallets (previously under Digital ID) become their own **Trust Infrastructure** domain.
- **Architecture criteria renamed A–E** to map onto CDPI's five DPI architecture principles: Interoperability, Minimalist/Reusable Building Blocks, Ecosystem Enablement, Federation/Decentralization, and Security & Privacy by Design.

### Removed

- **"Inclusive and accessible" as an entry criterion.** It is substantively covered by DPG Standard Indicator 9 (do no harm) and Maturity Model 1.1 (governance) and 3.4 (accessibility); repeating it here duplicated effort.