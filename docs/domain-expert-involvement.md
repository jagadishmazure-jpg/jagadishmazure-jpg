# Domain expert involvement

How subject-matter experts (underwriters, claims adjusters, clinicians, compliance officers, data owners)
are meant to shape the AI systems in this portfolio.

**This is the intended process, written down before it has been used.** Today the portfolio has one
maintainer and no outside experts have reviewed it. The domain logic in the repositories comes from my own
industry experience and from public sources, applied to synthetic data. Until the steps below have been
carried out and recorded, treat every domain rule in these repositories as a reasonable starting point, not
as expert-validated.

## Why experts are needed

Code can check that an agent follows its rules. It cannot check that the rules are right. Experts are the
only reliable source for:

* what a correct answer looks like (golden sets and acceptance criteria),
* which mistakes are harmless and which are serious (risk card impact scores),
* where a human must stay in the loop (approval points), and
* what the data actually means (field definitions and edge cases).

## When experts are consulted

| Stage | What the expert does | What changes in the repository |
|---|---|---|
| Framing | Confirms the problem, the users and the decisions the agent may and may not make | Use case section in the README and the model card's intended use |
| Data | Explains fields, edge cases and known quality problems | Data sheet and data quality checks |
| Golden set | Writes or approves the expected answers used by the eval gate | `evals/` golden files, with the reviewer recorded |
| Risk | Scores likelihood and impact of each failure and agrees the controls | Risk cards and scenario thresholds |
| Approval points | Decides which actions need a human and who that human is | HITL steps in the workflow |
| Release | Signs off before an agent moves from validation to production | Sign-off entry in the audit log |
| Monitoring | Reviews a sample of real outputs on a fixed cadence | New golden cases from real failures |

## How a session runs

1. **Prepare**: share the model card, data sheet, risk cards and ten to twenty sample outputs.
2. **Review**: the expert marks each sample as correct, acceptable or wrong, and says why.
3. **Record**: notes go into the repository as an issue or a doc; disagreements are recorded, not smoothed over.
4. **Change**: golden sets, thresholds, risk scores or approval points are updated in a pull request that
   links the session notes.
5. **Confirm**: the expert checks the change, and the sign-off is recorded.

## Which experts for which repository

| Repository | Expert roles needed |
|---|---|
| [Agent platform](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-platform) (mortgage underwriting) | Mortgage underwriter, fair-lending compliance |
| [Model risk](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk) | Model validator, compliance, and one expert per domain agent (fraud, claims, underwriting, prior authorization, pricing) |
| [Agentic AI projects](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai) | One reviewer per industry project (credit, claims, care, logistics, telecom) |
| [Agent labs](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs) | Emergency management, ophthalmology research, civil engineering, contract law, wind-turbine maintenance |
| [Fabric enterprise BI](https://github.com/jagadishmazure-jpg/Jagadish-fabric-enterprise-bi) | Retail operations and data owners |
| [FinOps](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops) | Cloud finance and platform owners |
| [Maturity assessor](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment) | Reviewers for the HITL sign-off of each category |

## How you can help

If you work in one of these fields and are willing to review a golden set or a risk card, open an issue on
the repository titled "domain review offer". Sessions are short and focused, and every change made from your
input is credited in the pull request.

## Status

| Item | Status |
|---|---|
| Process written | Done (this page) |
| Hooks in the code (golden sets, risk cards, HITL sign-off with reviewer identity) | Built in the repositories |
| First expert session | Planned, Month 10 in the [roadmap](roadmap.md) |
| Experts embedded in a team with a shared knowledge base | Not planned within the roadmap |
