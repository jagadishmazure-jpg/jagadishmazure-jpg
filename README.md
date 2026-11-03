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
| **Total (six featured repositories)** | | **2,361** |

Test counts are from each repository's own CI-checked run on its latest `main` commit. Every result in the table comes from synthetic data or a simulation and is labelled as such in the linked README. All six run offline with deterministic mocks; none has been deployed to a live Azure tenant yet. Each runs CI (pinned actions, lint, tests, gitleaks), CodeQL and Dependabot, and has a `main` ruleset with no force-push or deletion.

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
