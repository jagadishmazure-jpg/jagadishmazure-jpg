# Jagadish Meduri

**Agentic AI Engineer | Azure AI Foundry, Microsoft Agent Framework, LangGraph | Multi-Agent Systems, RAG, MCP, A2A | Enterprise AI Integration**

I build AI agents with the controls production needs, and connect them safely to the enterprise systems a business already runs on: approvals before risky actions, access-controlled retrieval, audited tool calls, eval gates in CI, and failure handling designed in from the start. My industry experience covers banking, healthcare, insurance, mortgage and retail.

## Featured portfolios

| Repository | What it shows | Key tech |
|---|---|---|
| [**Jagadish-agentic-ai**](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai) | 21 working business agents across eight industries, eight multi-agent orchestration patterns measured side by side, and a fine-tuning vs prompting study, all held to eval gates in CI | Python, LangGraph, LangChain, RAG, MCP, A2A, OpenTelemetry, FastAPI, Terraform |
| [**Jagadish-azure-agent-platform**](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform) | Multi-agent mortgage underwriting on Azure: document intake, parallel checks, critic review, human underwriter approval and crash-safe resume, plus a governed A2A control plane | Microsoft Agent Framework, Azure AI Foundry, AI Search, Document Intelligence, Content Safety, Bicep/azd, Terraform |
| [**Jagadish-azure-agent-labs**](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs) | Five end-to-end Azure agent labs: disaster risk from fused seismic, satellite and weather signals; retinal-scan research triage with calibrated, case-cited hypotheses; road maintenance planning on a city graph; contract compliance with router and auditor agents; and wind-turbine diagnostics that learn from evaluated experience through gated lessons | Microsoft Agent Framework, Azure AI Foundry, AI Search, AI Vision, Document Intelligence, Azure Maps, Event Hubs, Cosmos DB, MCP, Bicep, Terraform |
| [**Jagadish-azure-ai-integration-platform**](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform) | Agents that use SAP, Salesforce, ServiceNow, Workday, Dynamics and Jira only through five gateways, acting with the user's own permissions and a full audit trail | Entra ID OBO, APIM, Event Grid, Service Bus, Durable Functions, Logic Apps, MCP, A2A, FastAPI, Bicep, Terraform |
| [**Jagadish-fabric-enterprise-bi**](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi) | The data platform under the agents: streaming and batch retail data into a medallion Lakehouse and star schema, with live alerts, a forecast, a Power BI semantic model and a governed data agent (row-level security, PII masking, read-only SQL) that other agents call over MCP and A2A, all under Purview-style lineage and labels | Microsoft Fabric, OneLake, Eventhouse/KQL, Mirroring, Power BI/TMDL, Purview, Event Hubs, IoT Hub, DuckDB, scikit-learn, MCP, A2A, Bicep, Terraform |
| [**Jagadish-azure-finops**](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops) | Azure FinOps and AI FinOps as code: ten cost optimization patterns (rightsizing, autoscale, reservations and savings plans, Spot, storage tiering, Hybrid Benefit, serverless, idle cleanup, tagging and chargeback, cache and egress) with evidence, savings math and skip lists; per-request AI token attribution, model routing, caching, PTU break-even, ROI per use case and an eval gate; and a FinOps agent over MCP whose plans need human approval and run as a dry run | Cost Management, FOCUS, Azure Advisor, Azure Policy, Resource Graph, KQL, Retail Prices API, Azure OpenAI/PTU, MCP, Bicep, Terraform |
| [**Jagadish-agentic-ai-model-risk**](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk) | Model risk management for agentic AI as code, built on the four pillars of the CSA AI Model Risk Management Framework: model cards, data sheets, risk cards with inherent and residual scoring, plus what-if scenario planning, all linked in code; five fictional enterprise agents (fraud, claims, mortgage underwriting with fair-lending tests, prior authorization with PHI masking, pricing); inventory and tiering, lifecycle approval gates, independent validation, monitoring, HITL sign-off with an audit chain, an MCP risk-register tool and a CI gate | NIST AI RMF, EU AI Act, SR 11-7, ISO/IEC 42001, Foundry evaluations, Azure Policy, Purview, Application Insights, MCP, Bicep, Terraform |
| [**Jagadish-ai-maturity-assessment**](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment) | An evidence-based AI maturity assessor on the six-pillar, 29-category UNESCO AI Maturity Framework (structure adapted under CC BY-SA 3.0 IGO): collectors read IaC, CI workflows, ADRs, model and risk cards, eval gates, FinOps reports and data contracts, a questionnaire covers people and culture, and each category gets a level, a confidence score and cited evidence; low-confidence calls go to HITL sign-off with an audit chain, then a gap analysis, a Month 1-12 roadmap and an executive report with a radar chart. It assesses my own portfolio (overall level 3, provisional) plus a fictional bank and public agency | Python, MCP, A2A, eval gates, Container Apps jobs, Key Vault, Log Analytics, Bicep, Terraform |
| [**Jagadish-azure-ai-soc**](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-soc) | An AI-assisted security operations centre for a fictional MSSP and three customers: Microsoft Agent Framework agents for triage, investigation, ATT&CK mapping, threat intel, behaviour analytics, predictive risk and response over synthetic Sentinel and Defender XDR data; tier 1/2/3 routing with an analyst feedback loop (holdout accuracy 77.5% to 100%, zero attacks auto-closed); read-only tools shaped like the Sentinel MCP server; containment only after customer approval, as a dry run with a hash-chained audit; prompt-injection, PII and cross-tenant leakage tests; STRIDE, OWASP LLM Top 10 and MITRE ATLAS threat model | Microsoft Sentinel, Defender XDR, KQL, MITRE ATT&CK, Microsoft Agent Framework, Foundry, MCP, Logic Apps, Entra ID managed identity, Bicep, Terraform |
| [**Jagadish-ai-learning-lab**](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab) | How I learn and adopt new AI tech: each new tool or paper gets an offline spike with real numbers, a verdict on a tech radar (adopt / trial / assess / hold) and a link to where it was adopted. Topics so far: NVIDIA agent safety (adopted), Jev as a fast classifier in front of an LLM, GraphRAG hybrid retrieval, five advanced agent architectures (adopted) | Python, numpy, scikit-learn, networkx, sqlite, GitHub Actions |

All ten repositories run offline with deterministic mocks and sandbox stand-ins so anyone can clone and test them; none has been deployed to a live Azure tenant yet. Each one also has the same infrastructure in Bicep and Terraform, and a GitHub Actions deploy pipeline (OIDC sign-in, dev -> prod approval gates) that stays switched off until a subscription exists.

## Principles, plans and honest self-assessment

Written for recruiters, reviewers and teams that might adopt this work:

| Doc | What it covers |
|---|---|
| [AI principles](docs/ai-principles.md) | Ten principles and the code, tests and CI gates that enforce each one |
| [Roadmap](docs/roadmap.md) | Month 1-12 plan from offline builds to deployed, observed and reviewed systems |
| [Skills matrix](docs/skills-matrix.md) | What is proven in the repositories, what is written but not deployed, and what I am still learning |
| [Community and learning](docs/community-and-learning.md) | How I learn new tech, how I share it and how you can take part |
| [Data access process](docs/data-access-process.md) | Synthetic data only in the repos, and the steps for handling real data |
| [Domain expert involvement](docs/domain-expert-involvement.md) | How subject-matter experts are meant to shape golden sets, risk cards and approvals (intended process) |

## Projects by industry

| Industry | Projects |
|---|---|
| Banking | [15 banking-credit-memo](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/15-banking-credit-memo) (commercial credit memo, dual control) · [20 long-term-memory-agent](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/20-long-term-memory-agent) (assistant that remembers customers and forgets on request) |
| Healthcare | [14 healthcare-prior-auth](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/14-healthcare-prior-auth) (prior-auth packets, PHI redaction, clinician sign-off) · [medical-eye-scan-multimodal](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs/tree/main/labs/medical-eye-scan-multimodal) (retinal-scan research triage, not a medical device) |
| Insurance | [13 insurance-fnol-coverage](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/13-insurance-fnol-coverage) (first notice of loss to adjuster-approved reserve) |
| Mortgage | [19 finetune-vs-prompting](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/19-finetune-vs-prompting) (document classification) · [21 multi-agent-orchestration-patterns](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/21-multi-agent-orchestration-patterns) (underwriting exception solved eight ways) · [azure-agent-platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform) (underwriting conditions on Azure) |
| Retail | [03 refund-agent](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/03-refund-agent) (refunds with policy checks and approval) · [11 customer-care-e2e](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/11-customer-care-e2e) (late shipment and refund, end to end) · [fabric-enterprise-bi](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi) (grocery data platform, live freezer alerts, governed data agent) |
| Telecom | [16 telecom-outage-care](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/16-telecom-outage-care) (outage-aware care, bill explanation, dispatch) |
| Logistics & supply chain | [18 logistics-exception-agent](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/18-logistics-exception-agent) (shipment exceptions, carrier claims) · [10 supply-chain-multi-agent](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/10-supply-chain-multi-agent) (replenishment to approved PO) |
| Energy | [wind-turbine-continual-learning](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs/tree/main/labs/wind-turbine-continual-learning) (turbine diagnostics with eval-gated lessons) |
| Public sector & infrastructure | [disaster-signal-fusion](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs/tree/main/labs/disaster-signal-fusion) (multi-signal hazard risk, human alert decision) · [road-network-maintenance-graph](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs/tree/main/labs/road-network-maintenance-graph) (budgeted road maintenance plan) |
| Security operations (MSSP) | [azure-ai-soc](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-soc) (alert triage, investigation and human-approved containment for three fictional customers) |
| Automotive | [17 automotive-technician-copilot](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/17-automotive-technician-copilot) (service bulletins, parts, warranty claims) |
| Cross-industry back office | [05 invoice-po-matching](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/05-invoice-po-matching) · [08 contract-review](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/08-contract-review) · [legal-document-compliance](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs/tree/main/labs/legal-document-compliance) (banking, insurance and healthcare contracts) · [09 collections-agent](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/09-collections-agent) · [azure-ai-integration-platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform) (SAP, Salesforce, ServiceNow, Workday, Dynamics) |

## How I work

Each repository documents the same things in the same places, so a reviewer can check claims quickly:

| Where | What you will find |
|---|---|
| `docs/best-practices.md` | Enterprise cloud practices (identity, least privilege, networking, secrets, tagging, cost, IaC, CI/CD gates, observability, DR) and agentic AI practices (human in the loop, eval gates, guardrails, tool governance and MCP, memory, grounding, tracing, model versioning, responsible AI), each marked implemented, written-not-deployed or planned, with links to the code |
| `docs/adr/` | Architecture decisions: Bicep and Terraform side by side, offline mocks by default, OIDC and managed identity, eval gates that block the build, a deploy pipeline shipped switched off |
| `docs/deployment.md` | The deploy pipeline and the one-time Azure setup it needs |
| `SECURITY.md` · `CONTRIBUTING.md` · `CHANGELOG.md` | How to report a problem, the checks a change must pass, what changed |

Best-practice checklists: [agentic-ai](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/best-practices.md) · [azure-agent-platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/docs/best-practices.md) · [azure-agent-labs](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs/blob/main/docs/best-practices.md) · [azure-ai-integration-platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/best-practices.md) · [fabric-enterprise-bi](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi/blob/main/docs/best-practices.md) · [azure-finops](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops/blob/main/docs/best-practices.md) · [agentic-ai-model-risk](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/best-practices.md) · [ai-maturity-assessment](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment/blob/main/docs/best-practices.md) · [azure-ai-soc](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-soc/blob/main/docs/best-practices.md)

## Tech stack

**Agents & LLMs:**
![Microsoft Agent Framework](https://img.shields.io/badge/Microsoft_Agent_Framework-5C2D91?style=flat)
![Azure AI Foundry](https://img.shields.io/badge/Azure_AI_Foundry-0078D4?style=flat)
![Azure OpenAI](https://img.shields.io/badge/Azure_OpenAI-0078D4?style=flat)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat)
![MCP](https://img.shields.io/badge/MCP-555555?style=flat)
![A2A](https://img.shields.io/badge/A2A-555555?style=flat)

**Retrieval & evaluation:** RAG (hybrid, temporal, graph, access-controlled, multimodal) · Azure AI Search · AI Vision · Document Intelligence · Content Safety · azure-ai-evaluation · golden-set eval gates · fine-tuning

**Security operations:** Microsoft Sentinel · Defender XDR · KQL detections · MITRE ATT&CK and ATLAS · threat intel · UEBA (offline, synthetic data)

**Azure integration:** Entra ID (OAuth 2.0 OBO, managed identity, GitHub OIDC federation) · API Management · Event Grid · Service Bus · Durable Functions · Logic Apps · Container Apps · Cosmos DB · Event Hubs · ADLS Gen2 · Azure Maps · Key Vault

**Engineering:**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![Bicep](https://img.shields.io/badge/Bicep%20%2F%20azd-0078D4?style=flat)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat&logo=opentelemetry&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)

## Tested, not just demoed

**3,146 automated tests** across the ten repositories (544 agentic-ai + 114 agent platform + 222 integration platform + 158 agent labs + 58 learning lab + 200 Fabric + 236 FinOps + 592 model risk + 682 maturity + 340 AI SOC, counted with pytest in each repository's own environment). All pass except two maturity tests that are skipped on purpose: one needs a reference text that is never committed, the other compares a live scan of the sibling checkouts and only runs when asked. Every push runs lint, tests and eval gates in GitHub Actions, plus Terraform validation, offline plan tests, tflint and checkov on the infrastructure. Every repository also pins its GitHub Actions to commit SHAs, scans its full git history with gitleaks, runs CodeQL and gets weekly Dependabot updates; secret scanning with push protection, Dependabot security updates, private vulnerability reporting and a `main` ruleset (no force-push or deletion, CI required on pull requests) are switched on.
