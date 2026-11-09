# Jagadish Meduri

**Agentic AI Engineer | Microsoft Foundry, Microsoft Agent Framework, LangGraph | Multi-Agent Systems, RAG, MCP, A2A | Enterprise AI Integration**

I build AI agents with the controls production needs, and connect them safely to the enterprise systems a business already runs on: approvals before risky actions, access-controlled retrieval, audited tool calls, eval gates in CI, and failure handling designed in from the start. My industry experience covers banking, healthcare, insurance, mortgage and retail.

## Featured repositories

| Repository | Proof (outcome first) | Tests |
|---|---|---|
| [**Jagadish-azure-agent-platform**](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform) | Mortgage underwriting agents that pause for a human underwriter's approval and, after a crash, resume the loan where they left off; all five Microsoft Agent Framework orchestrations compared on the same loan review (offline, synthetic loans) | 116 |
| [**Jagadish-azure-ai-integration-platform**](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform) | Agents reach SAP, Salesforce, ServiceNow, Workday, Dynamics and Jira only through five gateways, with the user's own Entra OBO permissions; the watchdog contained 9 of 9 simulated attack scenarios with 0 false alarms, quarantining in under 2 ms (measured locally) | 232 |
| [**Jagadish-agentic-ai**](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai) | 21 business agents across eight industries and eight orchestration patterns measured side by side; fine-tuning lifted synthetic mortgage document classification accuracy from 0.64 to 0.97 with about 90% fewer input tokens per call (measured offline) | 554 |
| [**Jagadish-azure-ai-soc**](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-soc) | Multi-tenant AI SOC for a fictional MSSP: on 40 synthetic holdout incidents the analyst feedback loop took verdict accuracy from 77.5% to 100% with zero attacks auto-closed, and 9 of 9 scripted attack stories were detected and contained in dry run | 641 |
| [**Jagadish-agentic-data-layer**](https://github.com/jagadishmazure-jpg/Jagadish-agentic-data-layer) | The governed data layer agents act on, across four simulated domains: the data gateway stopped 14 of 14 access attacks and the retail forecast beat the same-day-last-week baseline (WAPE 31.9% vs 48.2%, synthetic data) | 666 |
| [**Jagadish-azure-aks-agent-platform**](https://github.com/jagadishmazure-jpg/Jagadish-azure-aks-agent-platform) | Claims paused for a human adjuster resumed on another pod after a pod kill 178 of 178 times with shared checkpoints vs 0 of 37 with pod-local disk; 96 of 96 injection attacks blocked with 0 of 100 benign prompts flagged (simulated, labelled stub model) | 152 |
| [**Jagadish-medical-vision-retrieval**](https://github.com/jagadishmazure-jpg/Jagadish-medical-vision-retrieval) | Hybrid image-plus-text retrieval over synthetic scans with confidence scores, retrieval attribution and a 5-step reasoning trace; top hybrid score 0.92, Precision@3 1.0 on 12 synthetic cases — retrieval and explanation only, never a diagnosis | 50 |
| [**Jagadish-tax-accounting-agents**](https://github.com/jagadishmazure-jpg/Jagadish-tax-accounting-agents) | Orchestrator-worker filing pipeline over synthetic returns: tax research, self-critique return validation, audit packs from confirmed findings only, and 3-jurisdiction parallel research with conflicts flagged, never silently resolved | 58 |
| [**Jagadish-environmental-monitoring-agents**](https://github.com/jagadishmazure-jpg/Jagadish-environmental-monitoring-agents) | Seismic, satellite and weather agents feeding a prediction coordinator that predicts only when ≥2 sources agree within 180 minutes; 5 of 6 predictions matched on synthetic events, mean lead time 90.0 minutes, false-alarm rate 0.1667 | 62 |
| [**Jagadish-road-infrastructure-agents**](https://github.com/jagadishmazure-jpg/Jagadish-road-infrastructure-agents) | Maintenance ranking and detour simulation over a synthetic road graph (6 junctions, 8 segments); closing one segment affected 6 routes with 37.8 added minutes at confidence 0.55, correctly routing to a senior approver | 70 |
| [**Jagadish-reasoning-method-suite**](https://github.com/jagadishmazure-jpg/Jagadish-reasoning-method-suite) | Same 12 synthetic tasks through 6 reasoning methods on one harness: algorithm-of-thoughts 12/12, lookahead 10/12, tree and rewound 9/12 each, graph 8/12, broken baseline 0/12 — swapping method and task order changes no scores | 52 |
| [**Jagadish-document-parser-benchmark**](https://github.com/jagadishmazure-jpg/Jagadish-document-parser-benchmark) | Three simulated parsers over the same 6 documents with field-level scoring and a quality gate that unredacted PII can never bypass; layout-aware F1 0.9831, OCR 0.8525, plain-text 0.5714 | 64 |
| [**Jagadish-agent-memory-defense**](https://github.com/jagadishmazure-jpg/Jagadish-agent-memory-defense) | Six-class agent-memory failure taxonomy with detection, quarantine and human-gated recovery; demo ends with 2 findings quarantined, 3 entries rolled back exactly, post-scan findings 0 | 61 |
| [**Jagadish-local-model-agents**](https://github.com/jagadishmazure-jpg/Jagadish-local-model-agents) | Local-first agent stack on a simulated local model with labelled degraded fallback, never silent; 5 of 6 tasks local, 1 degraded, 0 egress entries in every mode, local $0.0012 vs cloud-pattern $0.0240 (illustrative costs) | 59 |
| [**Jagadish-llm-provenance-classifier**](https://github.com/jagadishmazure-jpg/Jagadish-llm-provenance-classifier) | Which small LLM drafted a passage, for a fictional insurer's content audit: 66.2% accuracy on 160 unseen-topic test passages vs 25% chance; with calibration and an "unknown model" rule it names a model for 37.5% of passages and is right on 86.7% of those; a copied writing style still fools it on 26.2% of attacks (kept visible), and 0 of 440 findings were automatic accusations (synthetic corpus generated on CPU by five open models) | 90 |
| [**Jagadish-agentic-system-design**](https://github.com/jagadishmazure-jpg/Jagadish-agentic-system-design) | A fictional airport's passenger assistant built through 14 design layers, scored on the process as well as the answer: the learning loop took 129 synthetic scenarios from 69.0% to 95.3% success with 0 regressions, cut duplicate side effects from 9 to 0 with 0 unauthorized actions, and sent 96.2% fewer context tokens (offline, deterministic mock model) | 166 |
| [**Jagadish-cost-aware-llm-router**](https://github.com/jagadishmazure-jpg/Jagadish-cost-aware-llm-router) | Sends each request to the cheapest model likely to get it right, for a fictional logistics firm: on 120 held-out tasks the learned router scores 70.0% vs 65.0% for always using the large model, at 31.9% of the cost and a p95 latency of 1.5 s vs 5.3 s; a 10% budget cap is never exceeded, a circuit breaker keeps 100% of requests served in an outage, and 0 personal-data prompts reach the large tier; two-step arithmetic defeats every model (kept visible) (measured runs of three open models on CPU, synthetic tasks) | 74 |
| **Total (seventeen featured repositories)** | | **3,167** |

Test counts are from each repository's own CI-checked run on its latest `main` commit. Every result in the table comes from synthetic data or a simulation and is labelled as such in the linked README. All seventeen run offline with deterministic mocks or committed data; none has been deployed to a live Azure tenant yet. Each runs CI (pinned actions, lint, tests), security scanning and Dependabot, and has branch protection with no force-push or deletion.

## Everything else

All other public repositories (learning and pattern studies, security and privacy labs, AI model risk, exposure management and more) are listed with their test counts, status and case studies in the **[portfolio catalog](https://jagadishmazure-jpg.github.io/Jagadish-portfolio-catalog/)**, searchable by framework, industry and skill.

## Principles, plans and honest self-assessment

| Doc | What it covers |
|---|---|
| [AI principles](docs/ai-principles.md) | Ten principles and the code, tests and CI gates that enforce each one |
| [Roadmap](docs/roadmap.md) | Month 1-12 plan from offline builds to deployed, observed and reviewed systems |
| [Skills matrix](docs/skills-matrix.md) | What is proven in the repositories, what is written but not deployed, and what I am still learning |
| [Community and learning](docs/community-and-learning.md) | How I learn new tech, how I share it and how you can take part |
| [Data access process](docs/data-access-process.md) | Synthetic data only in the repos, and the steps for handling real data |
| [Domain expert involvement](docs/domain-expert-involvement.md) | How subject-matter experts are meant to shape golden sets, risk cards and approvals (intended process) |

## Tech stack

**Agents & LLMs:**
![Microsoft Agent Framework](https://img.shields.io/badge/Microsoft_Agent_Framework-5C2D91?style=flat)
![Microsoft Foundry](https://img.shields.io/badge/Microsoft_Foundry-0078D4?style=flat)
![Azure OpenAI](https://img.shields.io/badge/Azure_OpenAI-0078D4?style=flat)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat)
![MCP](https://img.shields.io/badge/MCP-555555?style=flat)
![A2A](https://img.shields.io/badge/A2A-555555?style=flat)

**Retrieval & evaluation:** RAG (hybrid, temporal, graph, access-controlled, multimodal) · Azure AI Search · AI Vision · Document Intelligence · Content Safety · azure-ai-evaluation · golden-set eval gates · fine-tuning

**Security operations:** Microsoft Sentinel · Defender XDR · KQL detections · MITRE ATT&CK and ATLAS · threat intel · UEBA · identity posture and privilege paths for Entra ID, PIM and Entra Agent ID (offline, synthetic data)

**Azure integration:** Entra ID (OAuth 2.0 OBO, managed identity, GitHub OIDC federation) · API Management · Event Grid · Service Bus · Durable Functions · Logic Apps · Container Apps · Cosmos DB · Event Hubs · ADLS Gen2 · Azure Maps · Key Vault

**Engineering:**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Bicep](https://img.shields.io/badge/Bicep%20%2F%20azd-0078D4?style=flat)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat&logo=opentelemetry&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
