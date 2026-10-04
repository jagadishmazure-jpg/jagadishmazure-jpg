# AI principles

These are the rules I hold every AI system in this portfolio to. Each principle names the concrete
mechanism that enforces it and links to the code or test that does the enforcing, so a reader can check
the claim instead of trusting it.

**Scope and honesty note.** The portfolio is a set of offline reference builds. Every repository runs on
synthetic data with deterministic model mocks, and none has been deployed to a live Azure tenant yet. "Enforced"
below means enforced in code and in CI on every push; it does not mean "proven in production".

## Summary

| # | Principle | Enforced by | Where to look |
|---|---|---|---|
| 1 | Humans decide on consequential actions | Approval steps that block the workflow until a named person signs | [HITL in the agent platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/src/agentplatform/orchestrations/hitl.py) |
| 2 | Nothing ships without passing evaluations | Golden-set eval gates that fail the build | [ADR: eval gates block release](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/adr/0004-eval-gates-block-release.md) |
| 3 | Guardrails at every layer | Input, tool, output and infrastructure controls, each tested | [Runtime safety](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/runtime-safety.md) |
| 4 | Least privilege and no stored secrets | OIDC federation, managed identity, on-behalf-of tokens | [ADR: OIDC and managed identity](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/adr/0003-oidc-and-managed-identity.md) |
| 5 | Protect personal data | PII and PHI masking, row-level security, synthetic data only | [Fabric data agent guardrails](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi/blob/main/src/fabricbi/serve/guardrails.py) |
| 6 | Fairness is measured, not assumed | Disparate-impact tests with a hard threshold | [Bias scenario](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/scenarios/bias-disparate-impact.md) |
| 7 | Every model is documented and risk-rated | Model cards, data sheets and risk cards checked by CI | [Model cards pillar](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/pillars/model-cards.md) |
| 8 | Decisions are traceable | Hash-chained audit logs, tracing, cited evidence | [HITL sign-off and audit chain](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/components/hitl-signoff.md) |
| 9 | Cost is a design constraint | Token budgets, cost guards, savings changes that need approval | [AI budgets](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops/blob/main/src/finops/ai/budgets.py) |
| 10 | Claims stay honest | Test counts from real runs, labelled sample data, docs checked against code | [Maturity assessor sample answers](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment/blob/main/samples/portfolio/questionnaire.yaml) |

## 1. Humans decide on consequential actions

An agent may draft, rank, recommend and prepare. When an action moves money, changes a record of
someone's rights or health, or changes cloud resources, a person approves it first.

How it is enforced:

* The mortgage workflow in the agent platform stops at an underwriter approval step and resumes only
  after a decision is recorded ([`hitl.py`](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/src/agentplatform/orchestrations/hitl.py)).
* The agent labs route risky tool calls through middleware that pauses for approval
  ([middleware and HITL](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs/blob/main/docs/components/middleware-and-hitl.md)).
* The FinOps agent can only produce plans; changes need human approval and run as a dry run, and the agent
  cannot approve its own plan ([`approval.py`](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops/blob/main/src/finops/agent/approval.py),
  [ADR](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops/blob/main/docs/adr/0004-human-approval-dry-run.md)).
* The maturity assessor never accepts a low-confidence score on its own; a reviewer signs off and the
  sign-off is bound to a digest of the evidence ([HITL review](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment/blob/main/docs/components/hitl-review.md)).

## 2. Nothing ships without passing evaluations

Every agent has a golden set of questions or cases with expected results. The CI build runs them and fails
when a score drops below its threshold, the same way a failing unit test would.

How it is enforced:

* [ADR: eval gates block release](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/adr/0004-eval-gates-block-release.md) and the [eval harness](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/components/eval-harness.md) in the agentic-ai repository.
* [`run_eval_gate.py`](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/scripts/run_eval_gate.py) and [`run_safety_evals.py`](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/scripts/run_safety_evals.py) in the integration platform.
* [Eval thresholds](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi/blob/main/evals/thresholds.yaml) for the Fabric data agent (NL-to-SQL accuracy, retrieval, guardrail attacks).
* The FinOps [eval gate](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops/blob/main/src/finops/ai/eval_gate.py) blocks a cheaper model route when it lowers answer quality.

## 3. Guardrails at every layer

No single filter is trusted. Controls sit at the input (prompt-injection and content checks), the tool layer
(allow-lists, read-only tools, scoped credentials), the output (grounding, masking, refusal) and the
infrastructure (network, policy, budgets).

How it is enforced:

* [Runtime safety](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/runtime-safety.md) and the [tool gateway](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/tool-gateway.md) in the integration platform.
* [Safety component](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/docs/components/safety.md) with an Azure AI Content Safety client in the agent platform.
* [Prompt-injection scenario](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/scenarios/prompt-injection.md) and [tool-misuse scenario](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/scenarios/tool-misuse.md), each run with controls on and off.
* [Agent safety spike](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab/tree/main/topics/04-nvidia-open-agent-safety) in the learning lab, whose verdict was adopted.

## 4. Least privilege and no stored secrets

Pipelines sign in to Azure with GitHub OIDC federation, workloads use managed identities, and agents call
enterprise systems with the user's own permissions through on-behalf-of tokens, never with a shared
service account.

How it is enforced:

* [ADR: OIDC and managed identity](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/adr/0003-oidc-and-managed-identity.md) and the [identity gateway](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/identity-gateway.md).
* Infrastructure tests and checkov scans in CI on the Bicep and Terraform code.
* Model calls in the agentic-ai repository go keyless through `DefaultAzureCredential` by default ([`shared/llm.py`](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/shared/llm.py)); an API key is used only when one is explicitly set.
* Known exception: the optional Azure fine-tuning script in [project 19](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/projects/19-finetune-vs-prompting/finetune_lab/azure_finetune.py) still authenticates with an API key. Moving it to Entra ID is a Month 1 item in [`roadmap.md`](roadmap.md).

## 5. Protect personal data

Real personal data never enters these repositories. Every dataset is synthetic and seeded. The code still
behaves as if the data were real: personal fields are masked before they reach a model or a log, and data
access is filtered by role.

How it is enforced:

* [Ticket triage PII redaction](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/projects/02-ticket-triage/ticket_triage/pii.py).
* [Fabric data agent guardrails](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi/blob/main/src/fabricbi/serve/guardrails.py): region-level security, masked personal columns and read-only SQL.
* [PII leak scenario](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/scenarios/pii-leak.md) in the model risk repository.
* The process for asking for data is written down in [`data-access-process.md`](data-access-process.md).

## 6. Fairness is measured, not assumed

Where a model affects people (credit, claims, care), outcomes are compared across groups and the build
fails when the ratio falls below the threshold.

How it is enforced:

* The [bias and disparate-impact scenario](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/scenarios/bias-disparate-impact.md): the synthetic underwriting assistant keeps a fair-lending ratio of about 0.96 with controls on and drops to about 0.35 with them off.
* Limitation: the groups and data are synthetic, so this proves the control works, not that a real model is fair.

## 7. Every model is documented and risk-rated

Each agent carries a model card, a data sheet and risk cards with likelihood and impact, plus what-if
scenarios. CI fails when a pillar is missing or a high risk has no control.

How it is enforced:

* [Model cards](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/pillars/model-cards.md), [data sheets](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/pillars/data-sheets.md) and [risk cards](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/pillars/risk-cards.md).
* The [CI gate](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/components/ci-gate.md) and an Azure Policy definition that [requires model-card tags](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/infra/policies/require-model-card-tags.json).
* The [demand forecast model card](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi/blob/main/docs/model-card-demand-forecast.md) in the Fabric repository.

## 8. Decisions are traceable

A reviewer should be able to answer "why did the system do that?" from the record alone.

How it is enforced:

* Hash-chained audit logs for sign-offs in the [model risk](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/components/hitl-signoff.md) and [maturity](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment/blob/main/docs/components/hitl-review.md) repositories; tests break the chain on purpose and expect the check to fail.
* OpenTelemetry tracing and Application Insights wiring in the [agentic-ai observability component](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai/blob/main/docs/components/observability.md) and the [integration platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-ai-integration-platform/blob/main/docs/components/observability.md).
* Every maturity score cites numbered evidence from the scanned files.

## 9. Cost is a design constraint

Model calls, search indexes and clusters cost money. Budgets are set before anything runs, and savings
changes go through the same approval path as any other change.

How it is enforced:

* [Token budgets](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops/blob/main/src/finops/ai/budgets.py), per-request cost attribution and the [budget-burn KQL query](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops/blob/main/queries/kql/ai-budget-burn.kql).
* [Run budgets in the agent harness](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/src/agentplatform/harness/budgets.py) cap steps, tokens and time per run.
* Cost estimates live next to the infrastructure (for example the [agent platform cost estimate](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform/blob/main/docs/cost-estimate.md)), and deploy pipelines stay switched off until a budget exists.

## 10. Claims stay honest

The portfolio says what it does and what it does not do yet.

How it is enforced:

* Test counts in READMEs come from real pytest runs.
* Docs embed real command output, and CI checks that the docs still match what the code prints.
* Each `docs/best-practices.md` marks every practice as implemented, written-not-deployed or planned.
* The maturity assessor labels the portfolio's people-and-culture answers as sample answers, weights them
  low and queues every category that rests on them for a human reviewer.

## What these principles do not cover yet

* An independent reviewer: today one person writes, tests and reviews everything. CODEOWNERS files route
  reviews, but the owner and the reviewer are the same person.
* People affected by the systems are not consulted, because the systems have no real users. See
  [`domain-expert-involvement.md`](domain-expert-involvement.md) for the intended process.
* No live deployment, so nothing here has been verified against real traffic, real identities or real cost.
