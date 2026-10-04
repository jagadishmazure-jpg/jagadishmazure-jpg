# Portfolio roadmap (Month 1 to Month 12)

This is the plan for taking the portfolio from offline reference builds to deployed, observed and reviewed
systems. It uses relative months, starting from the month the plan is adopted; there are no calendar dates.

**Owner of every item:** Jagadish Meduri (single maintainer). Where an item needs someone else, such as a
reviewer or a domain expert, the row says so, and the item is not marked done until that person has taken part.

## Where things stand at Month 0

| Area | State today |
|---|---|
| Code and tests | Nine public repositories, all offline, all green in CI; counts are in the [profile README](../README.md#tested-not-just-demoed) |
| Infrastructure | Bicep and Terraform for every repository, validated and plan-tested in CI; nothing deployed |
| Deploy pipelines | GitHub Actions with OIDC and dev-to-prod approval, switched off by a `DEPLOY_ENABLED` flag |
| Governance | Model cards, risk cards, HITL sign-off and audit chains as code; CODEOWNERS in every repository |
| Gaps found by the [maturity assessor](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment) | Single maintainer, no independent reviewer, no live deployment, people-and-culture answers are sample answers |

## Plan by quarter

| Quarter | Theme | Exit criteria |
|---|---|---|
| Q1 (Months 1-3) | First live deployment | One repository deployed to dev, observed, and torn down, all inside a budget |
| Q2 (Months 4-6) | Production-grade operations | Alerts, dashboards and runbooks exist and have fired at least once in a drill |
| Q3 (Months 7-9) | Scale and reliability | AKS deployment path tested; load and chaos tests have recorded results |
| Q4 (Months 10-12) | Independent review and reuse | At least one outside reviewer and one domain expert have taken part; one adopter has reused a repository |

## Month by month

| Month | Phase | Owner | Deliverable | Done when |
|---|---|---|---|---|
| 1 | Foundation | Jagadish | Subscription with a budget and alerts; move the remaining API-key path (fine-tuning script) to Entra ID | Budget alert fires in a test; no key-based auth left in the code path |
| 1 | Foundation | Jagadish | Turn on the deploy pipeline for the integration platform (the cheapest repository) | Dev deployment succeeds through GitHub Actions and is torn down the same day |
| 2 | Foundation | Jagadish | Deploy the agent platform to dev with Foundry and AI Search | Golden-set eval gate passes against a live model; cost recorded |
| 2 | Foundation | Jagadish | Application Insights, Log Analytics and Azure Monitor wired for the deployed services | Traces for one end-to-end request visible in the portal |
| 3 | Foundation | Jagadish | Azure Monitor alert rules as code (Bicep and Terraform) | Alerts deploy from the pipeline and one is triggered on purpose |
| 4 | Operations | Jagadish | Runbooks for the top failure modes in each deployed repository | Each runbook walked through once in a drill |
| 4 | Operations | Jagadish | Workbooks and dashboards for latency, cost per request and guardrail blocks | Dashboard shows real numbers from a test run |
| 5 | Operations | Jagadish | Deploy the Fabric enterprise BI repository to a Fabric trial capacity | Pipeline runs end to end; row-level security roles defined in the semantic model |
| 5 | Operations | Jagadish | Live cost data feeds the FinOps patterns instead of synthetic billing | At least three patterns produce findings from real cost exports |
| 6 | Operations | Jagadish | Model risk registry linked to deployed agents (tags and Azure Policy) | Policy blocks an untagged model deployment in dev |
| 7 | Scale | Jagadish | Kubernetes manifests or Helm charts and an AKS path for one agent service | Service runs on AKS with workload identity and autoscaling |
| 8 | Scale | Jagadish | Load tests with recorded results | Latency and cost curves published in the repository docs |
| 9 | Scale | Jagadish | Chaos tests on the deployed environment (model outage, throttling, dependency loss) | Each failure mode handled as documented, with traces as proof |
| 10 | Review | Jagadish with an outside reviewer | Independent code and design review of one flagship repository | Review findings filed as issues and the top ones fixed |
| 10 | Review | Jagadish with a domain expert | First domain-expert session, following [`domain-expert-involvement.md`](domain-expert-involvement.md) | Session notes and resulting changes recorded |
| 11 | Reuse | Jagadish | Package the shared pieces (eval harness, guardrail middleware) for reuse | One repository consumes the shared package instead of a copy |
| 11 | Reuse | Jagadish | Replace sample people-and-culture answers with answers a reviewer has checked | Maturity assessor categories signed off by a human, not provisional |
| 12 | Review | Jagadish | Re-run the maturity assessment and refresh this roadmap | New scores and the next roadmap committed |

## How this roadmap is kept current

* The [maturity assessor](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment) produces
  its own gap-to-roadmap plan from the evidence; this page is the human-owned version and is checked against it.
* Items move only when their "done when" column is true, and the change is recorded in the relevant
  repository's `CHANGELOG.md`.
* Any item that needs spend waits for a cost estimate and an explicit go-ahead.

## Risks to the plan

| Risk | Effect | Mitigation |
|---|---|---|
| Cloud cost overruns | Live work pauses | Budgets with alerts, same-day teardown, cheapest repository first |
| No outside reviewer available | Q4 review items slip | Ask through the communities listed in [`community-and-learning.md`](community-and-learning.md) early, from Month 6 |
| Preview services change their APIs | Rework | Version pins and the SDK notes kept in each repository |
| Single maintainer capacity | Fewer items per month | The maturity assessor caps the plan at three steps per month |
