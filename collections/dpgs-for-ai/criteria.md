# DPGs for AI — Technical Criteria

**Status:** Draft for community input · **Version:** 0.1.0 (unreleased)
**Co-stewards & partners:** Digital Public Goods Alliance (DPGA), with input from the [Open Data Institute (ODI)](https://theodi.org/), the [United Nations International Computing Centre (UNICC)](https://www.unicc.org/), and [Digital Futures Lab](https://digitalfutureslab.in/).

> This is a working draft published for open review. Nothing here is final. See [`CHANGELOG.md`](./CHANGELOG.md) for version history and the pull request thread for the discussion that produced it.

---

## How these criteria work

This document is a **supplementary lens** applied on top of the frameworks DPGs are already expected to comply with. It does **not** re-assess what those frameworks already cover; each criterion specifies only the *additional, AI-specific* expectation.

| Framework | What it covers | Obligation |
| :-- | :-- | :-- |
| [DPG Standard](https://digitalpublicgoods.net/standard/) | Open licensing, SDG relevance, ownership, platform independence, documentation, data extraction, privacy & applicable laws, open standards, do no harm | **Prerequisite** — must be met before applying these criteria |
| [DPG Maturity Model](https://github.com/ricardomiron/dpg-maturity-indicators/blob/main/indicators/core-indicators.md) (self-assessment) | Governance, community, QA, security, deployment readiness, documentation, accessibility, interoperability, support, adoption | **Complementary** — assessed separately to track growth |

### Design logic

- **Binary gate.** Inclusion is a yes/no decision based on **mandatory** criteria only. Recommended criteria are surfaced as *best practices met*, not as a score. (A published maturity tier may be introduced post-launch.)
- **Consistent structure across categories.** Software, data, and AI systems are assessed against the same dimensions — Adoption Readiness, Interoperability, Responsible Practices (mandatory); and Equity & Inclusion (recommended) — with category-specific indicators. Relevance is assessed once, at Layer 2.
- **Grounded in user needs.** Every criterion traces to a real need of a developer, government, researcher, or downstream community.
- **Achievable by Global Majority maintainers.** Mandatory criteria are documentation requirements, not engineering or measurement overhead, and require no specialised legal or technical infrastructure.
- **Assessable by DPGA.** Every criterion can be checked by a trained reviewer against public documentation — no proprietary access or code execution.

### Criteria at a glance

| Dimension | Status | Software | Data | AI Systems |
| :-- | :-- | :-- | :-- | :-- |
| **Adoption Readiness** | Mandatory | Governance & maintenance floor | Technical specs + versioning/changelog + API access | Benchmarks + versioning + changelog |
| **Interoperability** | Mandatory | AI-ready formats & integration points | AI-compatible formats + machine-readable metadata | *(covered by Standard; exchange formats recommended)* |
| **Responsible Practices** | Mandatory | Documented limitations & failure modes | Minimum-disclosure bias, limitations, de-identification | Safety-testing statement (or explicit absence) |
| **Equity & Inclusion** | Recommended | Mid-range hardware; language support; low/no-code; offline/on-prem | Supply-chain disclosure | Hardware disclosure (A2, mandatory); frugal variants; fine-tuning pathway |
| **Other recommended** | Recommended | Responsible-AI tooling | API access; copyright attestation; synthetic-data flagging; ISO standards | Third-party evaluation; exchange formats; energy/carbon with stated methodology |

---

## Layer 1 — Prerequisite: Recognized Digital Public Good

The solution must be a recognized DPG in the [DPG Registry](https://www.digitalpublicgoods.net/registry). **DPG Standard compliance is a precondition** for inclusion in this collection.

> **Note on AI systems:** the DPG Standard's requirements for AI systems are intentionally more demanding than for other categories (open weights, training-data transparency, open code). The Layer 3 criteria for AI systems are therefore deliberately light — they add only what the Standard does not already cover.

---

## Layer 2 — AI Relevance

Refers to solutions that meaningfully enable the development, deployment, or responsible use of AI. The collection covers three categories:

| Category | What it includes | What it excludes |
| :-- | :-- | :-- |
| **Open source software** | Tools with specific functionality in at least one AI lifecycle stage (data collection/annotation, training, fine-tuning, evaluation, inference/deployment, safety testing, monitoring) | Generic solutions (e.g. form builders, general-purpose tools, apps that only consume AI) whose connection to AI is indirect |
| **Open data** | Datasets explicitly scoped for, or with demonstrated use in, AI/ML training, fine-tuning, or evaluation | Datasets published in non-machine-readable formats; data only incidentally usable for AI |
| **Open AI systems** | AI models and systems (any type of AI, not only generative) meeting the DPG Standard's AI requirements | Wrappers around proprietary models; systems whose core components are closed |

**All three of the following must be true to proceed to Layer 3:**

1. **Category fit.** The solution falls clearly into one of the three categories above.
2. **AI lifecycle utility.** The solution provides specific, demonstrated capability in at least one AI lifecycle stage (software), is explicitly scoped or demonstrably used for AI/ML (data), or has a documented use case stating the problem addressed, target audience, and context (AI systems).
3. **Documented relevance / impact.** At least one documented deployment, use case, or relevance-by-design rationale exists. Scale, impact, or design-for-AI-training characteristics count as equivalent evidence to a deployment count.

---

## Layer 3 — Technical Criteria

Where the criteria below overlap with the DPG Standard or Maturity Model, the requirement specifies the **additional, AI-specific expectation** beyond what those frameworks already require.

### 💻 Open Source Software (AI lifecycle tools)

**Mandatory (all required):**

| # | Criterion | Evidence |
| :-- | :-- | :-- |
| **S1** | **Adoption readiness:** Transparent governance with identifiable contribution mechanisms and evidence of active maintenance | Governance doc, roadmap, or commit/release activity |
| **S2** | **Interoperability:** Use of open, standard formats for AI artifacts (e.g. ONNX, JSON-LD, CSV/Parquet) and documented integration points with other tools | Format/API documentation |
| **S3** | **Responsible practices:** Documentation of known limitations, biases, and failure modes | Public limitations statement |

> *Beyond DPG Standard/Maturity:* The Maturity Model tracks governance depth and maintenance over time; S1 sets a minimum evidence floor at entry. The Standard (Indicator 8) requires open standards generically; S2 requires AI-pipeline-compatible formats specifically.

**Recommended:**

- **Equity & inclusion:** Runs on standard mid-range hardware (CPUs/older GPUs); supports non-Latin scripts or low-resource languages where text processing is involved; low-code/no-code interfaces enabling non-specialist teams to deploy and configure.
- **Responsible practices:** Built-in responsible-AI tooling (bias detection, fairness auditing, PII masking, or privacy-preserving techniques such as differential privacy / federated learning).
- **Inclusion & autonomy:** Fully functional in local/on-premise deployment without mandatory internet or cloud dependency; no architectural mechanism by which downstream users can be locked out by changes in commercial or access terms.

### 📊 Open Data

**Mandatory (all required):**

| # | Criterion | Evidence |
| :-- | :-- | :-- |
| **D1** | **Adoption readiness:** Basic technical specifications (modalities, dimensions, update frequency, column/field definitions), versioning with a maintained changelog, and programmatic/API access to data and metadata | Datasheet or dataset documentation page + API documentation |
| **D2** | **Interoperability:** AI-compatible open formats (CSV/CSVW, Parquet, RDF, etc.) and machine-readable metadata, with **Croissant preferred** and CSVW or schema.org/Dataset as acceptable fallbacks | Format + metadata files |
| **D3** | **Responsible practices:** Minimum-disclosure documentation of bias, representation, known limitations, and collection context, including the de-identification/anonymisation method where personal data is present | Croissant-RAI, datasheet, or data statement |

> *Beyond DPG Standard/Maturity:* Indicator 7 requires privacy compliance; D3 adds methodological transparency. Indicator 5 requires mechanisms to extract data; D2 adds pipeline compatibility — a dataset that cannot enter an ML pipeline without manual extraction does not function as AI-ready. Minimum-disclosure means a genuine narrative statement of coverage, gaps, and collection context.

**Recommended:**

- **Responsible practices:** Copyright attestation (explicit statement of the legal basis for source inputs, distinct from the dataset's own licence); demarcation of synthetic data and machine annotation.
- **Equity & inclusion:** Human and organisational supply-chain disclosure (who collected/annotated, under what conditions).
- **Standards & vocabularies:** Use of international standards where applicable (ISO 3166, ISO 8601, controlled vocabularies).

### 🧠 Open AI Systems

**Mandatory (all required):**

| # | Criterion | Evidence |
| :-- | :-- | :-- |
| **A1** | **Adoption readiness:** Performance results on public or domain evaluation sets with stated methodology, plus versioned releases with a changelog | Benchmark report + release notes or research paper |
| **A2** | **Equity & inclusion:** Public disclosure of baseline hardware and system requirements (minimum RAM, CPU/GPU dependency, storage; CPU-only feasibility where applicable) and an intended deployment-context declaration | README or model-card section + e.g. UNICC Frugal AI deployment profiles (ultra-constrained edge → cloud-assisted) |
| **A3** | **Responsible practices:** Safety-testing / red-teaming documentation | Safety section of the model card |

> *Beyond DPG Standard/Maturity:* The Standard for AI systems already requires training-data transparency, open weights, and open code; these are **not re-assessed here**. A1 adds the minimum a downstream user needs to judge fit-for-purpose. A2 is a documentation-only requirement (no benchmarking overhead) that lets low-resource adopters assess deployment feasibility before investing in testing. A3 establishes an honesty floor — explicit disclosure of *absence* is acceptable.

**Recommended:**

- **Equity & inclusion:** Optimised variants for constrained deployment (quantisation, pruning, distillation; frugal/small-model design); published inference benchmarks on low-resource or commodity hardware. An intended deployment-context declaration (e.g. the UNICC Frugal AI deployment profiles, from ultra-constrained edge to cloud-assisted) is encouraged as a template.
- **Inclusion & autonomy:** Documented fine-tuning pathway for domain or language adaptation; capability to run fully offline/on-premise.
- **Responsible practices:** Independent or third-party evaluation results; energy/carbon-per-inference disclosure where a stated, reproducible methodology is used.
- **Interoperability:** Standard model-exchange formats (e.g. ONNX, safetensors) or open APIs. *(Agentic design considerations: TBD.)*

---

## Relationship to other DPGA collections

DPGA Collections are curated sets of DPGs grouped by strategic priority (e.g. Climate, DPGs4DPI, DPGs4AI) to accelerate impact in specific sectors. This collection mirrors the layered structure used by the DPGs4DPI and Climate collections — **prerequisite → relevance gate → category criteria** — so it complements rather than duplicates those workstreams.

## How to contribute

Open an issue or comment on the open pull request for this collection. We are especially looking for input on the points listed in the collection [`README.md`](./README.md#what-were-looking-for). Substantive changes are recorded in [`CHANGELOG.md`](./CHANGELOG.md).
