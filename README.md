# TrustLens — a trust-first AI reuse marketplace (demo)

**Problem:** Teams build yet another AI tool because they don't know what already exists—or they cannot tell whether an existing solution is safe and legally usable.

**Idea:** Before you build, discover existing AI projects, compare their suitability, and transparently see what evidence is present, unknown, or still required. The prototype deliberately avoids fake compliance badges.

## Run locally

No account, API key, database, Node modules, build step, or external backend required. The site consists of three static files.

```bash
git clone https://github.com/pratikadhikari-de/ai_tools_market.git
cd ai_tools_market
python3 -m http.server 8000
```

Open **http://localhost:8000**. You may also open `index.html` directly; the HTTP server makes local demo behavior more consistent.

## 3-minute curated demo script

1. **Problem:** “Our manufacturing firm needs to process technical PDF documents. We don't want to rebuild a parser from scratch.”
2. **Discover:** On the home page choose **Document intelligence**. Show real upstream projects such as **Docling**, **RAGFlow**, and **Haystack**. Select **MIT / Apache license** to narrow license categories.
3. **Trust is visible:** Open **View trust dossier**. Show public repo provenance, license metadata, and clearly marked **NOT ASSESSED** security, privacy, and AI Act requirements. Say: *“We won't make up certifications just to rank a tool.”*
4. **Compare:** Select 2–3 projects and open **Compare tools**. Discuss component vs. full application and how existing solutions can be extended.
5. **Build vs. reuse:** Open **Build vs. reuse** to see the reuse-first decision and a concrete adoption checklist.
6. **Procurement handoff:** Click **Download decision brief**. A Markdown report is generated locally. Open **Review queue** to show the three assessments still needed before production.

## Curated source-linked projects

The GitHub owner, repository existence, archived status, and GitHub-reported SPDX license metadata were checked on **2026-11-09**. Verify all details again before business use.

| Project | Upstream repository | GitHub-reported SPDX metadata |
| --- | --- | --- |
| Docling | https://github.com/docling-project/docling | MIT |
| RAGFlow | https://github.com/infiniflow/ragflow | Apache-2.0 |
| Haystack | https://github.com/deepset-ai/haystack | Apache-2.0 |
| Langflow | https://github.com/langflow-ai/langflow | MIT |
| Open WebUI | https://github.com/open-webui/open-webui | NOASSERTION — review current terms |
| Ollama | https://github.com/ollama/ollama | MIT |
| LibreChat | https://github.com/LibreChat-AI/LibreChat | MIT |
| Qdrant | https://github.com/qdrant/qdrant | Apache-2.0 |

**Important:** The license shown is a repository metadata identifier, not a legal opinion about all code, models, dependencies, images, branding, or commercial deployments. “Open source” is used broadly for discoverability; not every listing necessarily meets OSI definitions. Open WebUI is flagged for explicit license review.

## Honest evidence model

- **Source-linked:** a real upstream GitHub project exists. Not synonymous with a vetted codebase.
- **License metadata identified:** GitHub returns an SPDX identifier. Not an independent legal review.
- **Security, GDPR and EU AI Act:** **not assessed**. This app has no third-party audit reports, data-processing agreements, supplier attestations, or certification evidence.
- **Match percentages:** deterministic **simulated** use-case relevance derived from hand-curated capability levels and deployment/license metadata. They are *not* independent performance benchmarks, accuracy results, or security scores.
- **Review queue:** illustrative client-side checklist; completing a task is not vendor verification.

If made into a real product, each claim should have `claim`, `scope`, `source_url`, `issuer`, `date_checked`, `expiry`, `assurance_level`, `reviewer` and `status` (`vendor_declared`, `source_linked`, `independently_tested`, `audited`, `not_assessed`, `expired`).

## What's included

- Responsive single-page app: **discovery**, **compare**, **build vs. reuse**, **review queue**.
- Four business scenarios: document intelligence, private assistants, agents/automation, semantic search.
- Search and requirement filters; real upstream repository links; eight product dossiers.
- A three-tool comparison matrix with a limit of three selections.
- Client-side persistence for comparison and checklist progress (`localStorage`).
- Downloadable Markdown decision brief, generated in the browser.
- A transparent methodology panel and explicit evidence gaps.

## What's deliberately not included

No authentication, vendor claims ingestion, GitHub live polling, production-grade recommendation model, compliance engine, security scans, or live AI agents. This is **a curated fake-data prototype**, not a real marketplace or assurance service.

## Roadmap after the demo

1. Real tool profiles with typed evidence, source snapshots, version/commit hashes, and audit trails.
2. Better product categories and task-level evaluation datasets with reproducible benchmarks.
3. Supplier evidence requests, privacy/security questionnaire mapping, and buyer-specific controls.
4. Human-reviewed trust dossiers and ongoing evidence freshness monitoring.
5. Integration recommendations and build-vs-buy cost estimates.

Built using plain HTML, CSS, and JavaScript to make running the 30-minute proof of concept trivial.