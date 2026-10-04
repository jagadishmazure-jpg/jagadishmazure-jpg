# Skills matrix

An honest self-assessment. For each skill it says whether the skill is **proven in the repositories**
(working code and passing tests a reader can run), **written, not deployed** (code and infrastructure exist
and are validated offline, but have not run in a live cloud environment), or **learning** (studied or
prototyped, not yet demonstrated end to end).

Industry experience in banking, healthcare, insurance, mortgage and retail comes from my work history and is
not something these repositories can prove; the repositories only show synthetic, fictional versions of those
domains.

## How to read the levels

| Level | Meaning |
|---|---|
| Proven in repos | You can clone the repository, run the tests and see the behaviour |
| Written, not deployed | Code, IaC or pipelines exist and pass offline checks; never run against a live tenant |
| Learning | Spikes, notes or partial work; not something I would claim as delivered |

## Agentic AI engineering

| Skill | Level | Evidence |
|---|---|---|
| LangGraph and LangChain agents | Proven in repos | [21 projects](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai) |
| Microsoft Agent Framework | Proven in repos (offline, with mock chat clients) | [Agent platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform), [agent labs](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs) |
| Multi-agent orchestration patterns | Proven in repos | [Project 21](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/21-multi-agent-orchestration-patterns), [orchestration patterns](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/docs/orchestration-patterns.md) |
| Prompt and context engineering | Proven in repos | [Prompts](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/docs/components/prompts.md), [context builder](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/components/context-builder.md) |
| Agent harness (budgets, retries, resume) | Proven in repos | [Harness](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/docs/components/harness.md) |
| RAG (hybrid, graph, access-controlled) | Proven in repos | [Knowledge and context](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/docs/components/knowledge-and-context.md), [GraphRAG spike](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab/tree/main/topics/02-graphrag-hybrid-retrieval) |
| MCP servers and gateways | Proven in repos | [MCP gateway](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/mcp-gateway.md) |
| A2A agent cards and gateways | Proven in repos | [A2A gateway](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/a2a-gateway.md) |
| Evaluation and eval gates | Proven in repos | [Eval harness](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/components/eval-harness.md) |
| Guardrails and runtime safety | Proven in repos | [Runtime safety](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/runtime-safety.md) |
| Fine-tuning | Proven in repos for the local comparison; the Azure fine-tuning job is written, not run | [Project 19](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/tree/main/projects/19-finetune-vs-prompting) |
| Azure AI Foundry (live projects, hosted agents, evaluations) | Learning | Clients and IaC are written; nothing has run against a live Foundry project in these repositories |
| Live LLM quality at scale | Learning | All eval numbers come from deterministic mocks |

## Azure and infrastructure

| Skill | Level | Evidence |
|---|---|---|
| Bicep | Written, not deployed | Every repository has `infra/` with Bicep, built and linted in CI |
| Terraform | Written, not deployed | Every repository has Terraform with validate, offline plan tests, tflint and checkov |
| GitHub Actions CI | Proven in repos | Green CI on every repository |
| GitHub Actions deploy (OIDC, approvals) | Written, not deployed | `deploy.yml` in each repository, switched off by `DEPLOY_ENABLED` |
| Entra ID, managed identity, on-behalf-of flow | Written, not deployed (flows are unit-tested with stand-ins) | [Identity gateway](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/identity-gateway.md) |
| API Management, Event Grid, Service Bus, Durable Functions, Logic Apps | Written, not deployed | [Integration platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform) |
| AKS and Kubernetes | Learning | An AKS module exists in the integration platform's IaC; there are no Kubernetes manifests or Helm charts yet |
| Application Insights, Log Analytics, Azure Monitor | Written, not deployed | Tracing code and KQL exist; alert rules are still planned |
| Microsoft Fabric | Written, not deployed | [Fabric enterprise BI](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi) runs on a local stand-in (DuckDB) |

## Governance, risk and cost

| Skill | Level | Evidence |
|---|---|---|
| Model risk management (model cards, data sheets, risk cards, scenarios) | Proven in repos | [Model risk repository](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk) |
| Regulatory mapping (NIST AI RMF, EU AI Act, SR 11-7) | Proven as documentation and tests, not as a legal opinion | [Regulatory mapping](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/regulatory-mapping.md) |
| Human-in-the-loop sign-off with audit chains | Proven in repos | [HITL sign-off](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/components/hitl-signoff.md) |
| FinOps and AI FinOps | Proven on synthetic billing data | [FinOps repository](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops) |
| AI maturity assessment | Proven in repos | [Maturity assessor](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment) |
| Purview (lineage, labels) | Written, not deployed | Purview-style catalog in code; Purview IaC module exists |

## Software engineering

| Skill | Level | Evidence |
|---|---|---|
| Python, typed and tested | Proven in repos | pytest suites in every repository |
| FastAPI services | Proven in repos | [Portfolio API](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/components/portfolio-api.md) |
| Docker images | Written, not deployed | Dockerfiles exist; images are not pushed to a registry |
| OpenTelemetry | Proven in repos (local exporters) | [Observability](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/components/observability.md) |

## Working style

| Skill | Level | Evidence |
|---|---|---|
| Documentation for outside readers | Proven in repos | Every component doc includes real command output that CI checks against the code |
| Architecture decision records | Proven in repos | `docs/adr/` in each repository |
| Working with reviewers and domain experts | Learning | One maintainer today; see [`domain-expert-involvement.md`](domain-expert-involvement.md) |
| Learning new tech quickly and in the open | Proven in repos | [AI learning lab](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab), see [`community-and-learning.md`](community-and-learning.md) |

## What I am learning next

Matched to the [roadmap](roadmap.md): live Foundry deployments and evaluations, Azure Monitor alerting as
code, AKS with workload identity, and Fabric on a real capacity.
