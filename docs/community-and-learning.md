# Community and learning

How I keep up with AI and cloud changes, how I share what I learn, and how other people can take part.
This page only describes things that exist in the repositories or are clearly marked as planned.

## How I learn

New tools, papers and services change every few weeks, so learning is a repeatable process rather than
reading alone. The [AI learning lab](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab)
is where it happens:

1. **Pick a topic** from release notes, papers or a problem in one of the other repositories.
2. **Write a spike**: a small, offline experiment with real numbers, from a shared
   [template](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab/tree/main/TEMPLATE).
3. **Record a verdict** on the tech radar: adopt, trial, assess or hold, with the reason.
4. **Link to adoption**: when a verdict is adopt, the spike links to the repository and file where the idea
   is now used, and that repository links back.

Topics covered so far:

| Topic | Verdict | Where it went |
|---|---|---|
| [Five advanced agent architectures](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab/tree/main/topics/01-five-agent-architectures) | Adopted | [Azure agent labs](https://github.com/jagadishmazure-jpg/Jagadish-azure-agent-labs) |
| [GraphRAG hybrid retrieval](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab/tree/main/topics/02-graphrag-hybrid-retrieval) | See the spike | Retrieval patterns in the agent repositories |
| [A fast classifier in front of an LLM](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab/tree/main/topics/03-jev-system1-classifier) | See the spike | Routing ideas for cost control |
| [Open agent safety tooling](https://github.com/jagadishmazure-jpg/Jagadish-ai-learning-lab/tree/main/topics/04-nvidia-open-agent-safety) | Adopted | Guardrail layers across the portfolio |

The current verdict for each topic is kept in the learning lab itself, which is the source of truth.

## Frameworks I study and build on

Public frameworks give the portfolio a shared vocabulary with risk, audit and leadership teams. Each one is
used with credit, in my own words, and the source document itself is never committed.

| Framework | Used in |
|---|---|
| CSA AI Model Risk Management Framework (four pillars) | [Model risk repository](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk) |
| UNESCO AI Maturity Framework (six pillars, structure adapted under CC BY-SA 3.0 IGO) | [Maturity assessor](https://github.com/jagadishmazure-jpg/Jagadish-ai-maturity-assessment) |
| NIST AI RMF, EU AI Act, SR 11-7 | [Regulatory mapping](https://github.com/jagadishmazure-jpg/Jagadish-agentic-ai-model-risk/blob/main/docs/regulatory-mapping.md) |
| FinOps Foundation FOCUS cost data format | [FinOps repository](https://github.com/jagadishmazure-jpg/Jagadish-azure-finops) |

## How I share

* **Everything is public and runnable.** Every repository runs offline with synthetic data, so anyone can
  clone it and check a claim in minutes.
* **Docs are written for three readers:** me, recruiters and teams that might adopt the work. Every
  component doc ends with an "Adopt this" section on reuse, configuration and safe extension.
* **Interview and implementation guides** in several repositories walk through the design at two, ten and
  thirty minutes of depth.
* **Decisions are explained**, not just made: each repository has architecture decision records in `docs/adr/`.

## How you can take part

| You want to | Do this |
|---|---|
| Report a bug or a wrong claim | Open an issue on the repository; wrong numbers in docs are treated as bugs |
| Report a security problem | Follow the repository's `SECURITY.md` and do not open a public issue |
| Contribute a change | Read `CONTRIBUTING.md`; CI runs lint, tests, eval gates and IaC checks on every pull request |
| Reuse a repository | Start from its `docs/adopt-this.md` or the "Adopt this" sections; MIT-licensed code unless a folder says otherwise |
| Review the design or act as a domain expert | Open an issue titled "review offer"; see [`domain-expert-involvement.md`](domain-expert-involvement.md) |

## What is not here yet

* No talks, posts or community memberships are listed, because none are linked from these repositories yet.
  When they exist, they will be added here with links.
* No outside contributors so far. The [roadmap](roadmap.md) plans for an outside review in Q4 and starts
  asking for one from Month 6.
