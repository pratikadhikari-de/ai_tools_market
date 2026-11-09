# TrustLens — a trust-first AI reuse marketplace for supply chain & logistics

**Demo purpose:** Encourage logistics engineers and businesses to **discover, compare, pilot and reuse** existing AI, optimization and operational solutions *before* building more software from scratch.

**Scope:** 45 curated, source-linked public GitHub projects across **11 supply-chain domains**, from forecasting to warehouse robotics. This is a static, locally running demonstration, not an AI audit platform.

## Run locally

No API keys, npm, databases or online services are needed to run the UI.

```bash
git clone https://github.com/pratikadhikari-de/ai_tools_market.git
cd ai_tools_market
python3 -m http.server 8000
```

Open **http://localhost:8000** (or double-click `index.html`).

## Coverage — start from a business domain

| Domain | Illustrative open-source starting points | Catalog count* |
| --- | --- | ---: |
| Demand forecasting | StatsForecast, MLForecast, NeuralForecast, Darts | 8 |
| Inventory & replenishment | Stockpyl, frePPLe, ERPNext, OR inventory planning | 12 |
| Procurement & suppliers | OCA Purchase Workflow, ERPNext, Docling, Skyvern | 6 |
| Warehouse operations | OpenBoxes, ERPNext, OCA Warehouse, Open-RMF | 10 |
| Routing & dispatch | PyVRP, VROOM, OR-Tools, OSRM, GraphHopper | 8 |
| Fleet & shipment visibility | Traccar, ThingsBoard, Valhalla, OpenRouteService | 9 |
| Trade & logistics documents | Docling, PaddleOCR, Tesseract, Unstructured | 7 |
| Warehouse robotics & vision | Open-RMF, Nav2, openTCS, MMDetection, YOLO | 5 |
| Production & network planning | Pyomo, frePPLe, OR-Tools, ERPNext | 8 |
| Risk & knowledge intelligence | RAGFlow, Haystack, Qdrant, LibreChat | 14 |
| Data, analytics & automation | Apache Airflow, Dagster, Superset, Skyvern | 14 |

*One project can belong to several domains, so counts overlap.* All 45 source repositories and their GitHub-reported license identifiers were checked on **2026-11-09**. Domain tagging, deployment descriptions and implementation complexity are editorial, not verified performance or security facts. Browse `catalog.js` to review or expand the source-linked dataset.

### Important: not all listed projects are AI

The catalog differentiates **AI/ML toolkits**, **operations-research solvers**, **routing engines**, **ERP/WMS software**, **robotics and IoT platforms**, **data infrastructure** and **analytics tools**. That is intentional: existing deterministic software is often safer, easier to audit and less expensive than building a new AI agent to do the same thing.

## Guided 5-minute demonstration: from problem to reuse

**Fictional buyer:** Northstar Logistics, an EU logistics operator. Sensitive shipment and supplier data must not be handed to unknown third-party services.

1. **Problem (30 sec):** “We want to build an AI system to optimize delivery routes.”
2. **Discover (45 sec):** Click **Routing & dispatch** → show OR-Tools, PyVRP, VROOM, OSRM. Explain the difference between optimizers and routing engines.
3. **Refine (45 sec):** Search `vehicle routing`, select a solution type and check the **Permissive metadata** filter to see how license terms change the shortlist. This filter only uses GitHub's license identifier.
4. **Trust (60 sec):** Open **View trust dossier** for PyVRP. Show repository, reported license and the explicit **NOT ASSESSED** security and GDPR checks. Compare to a project with **NOASSERTION** license metadata; lack of evidence is not a pass.
5. **Compare (60 sec):** Select PyVRP, VROOM and Google OR-Tools. Compare domain focus, integration complexity, licenses and unresolved assurance.
6. **Decide (30 sec):** Open **Build vs. reuse** and choose **Routing & dispatch**. The recommendation is to pilot an existing solver before building a custom engine.
7. **Export (30 sec):** Download a Markdown decision brief with GitHub sources and the outstanding due diligence tasks.

**Second storyline (forecasting):** Choose **Demand forecasting**; compare StatsForecast vs MLForecast vs NeuralForecast, then explain that the right model depends on measured historical accuracy—not on a star rating or fictional “trust score.”

## What's implemented

- Eleven interactive business-domain filters and **45** curated listings
- Repository source links and GitHub-reported license identifiers
- Search by solution, repo, operational capability or domain; filter by solution type, local/self-hosted potential, license metadata
- 3-way comparison of roles, deployment expectations and trust evidence gaps
- Evidence-oriented per-project **Trust dossier**, explicitly marking unassessed claims
- Build-vs-reuse scenario selection and actionable adoption checklist
- Browser-only decision brief export, review checklist and shortlist persistence
- Responsive UI that also works without internet once local files are present

## What the “trust” layer actually proves

- **Source-linked:** Repository identity and GitHub metadata snapshot were checked; this does *not* mean the code is safe, actively maintained forever or legally approved.
- **License metadata identified:** The reported SPDX identifier is shown. `NOASSERTION`/`Not reported` triggers explicit review. Even `MIT`/`Apache-2.0` does not establish that dependencies, pretrained models or datasets have compatible terms.
- **Independent security and GDPR / EU AI Act compliance:** **NOT ASSESSED** for every listing. There are no scanned vulnerabilities, audit reports, supplier attestations or data-processing agreements.
- **Domain fit %:** A transparent, **simulated** ranking based solely on editorial domain tags. It is not a benchmark, trust score, business impact, route optimization quality, prediction accuracy or compliance pass.
- **Review queue:** Local checklist, not a certificate or authorization to process production data.

A production-grade version would require version-scoped evidence records, reviewers, expiry dates, independent security tests, actual workflow benchmarks and buyer-specific compliance gates.

## Structure

```
index.html    Shell, accessible navigation
catalog.js    Curated domain definitions and 45 source-linked listings
app.js        Search, ranking, comparison, dossiers, workflow, export
styles.css    Responsive presentation
```

## Non-goals for this demo

No AI model or agent is executed. No automatic vulnerability scans, GitHub polling, compliance certification, real-time supplier ranking, live inventory, or production procurement recommendation is provided. **Do not use simulated ranking to make safety, legal or purchasing decisions.**
