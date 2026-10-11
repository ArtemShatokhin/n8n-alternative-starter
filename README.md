# n8n alternative starter — an open-source workflow-migration agent on Kortix

An open-source, self-hosted starting point for a team whose work has outgrown
a fixed workflow. n8n is a good workflow engine: you draw the steps once and
it runs them. Real company work does not always fit that shape — it needs an
agent that can read the situation, decide, and act.

This template runs on **[Kortix](https://kortix.com)** — the open-source AI
Operating System. In Kortix your agents, skills, company memory and connectors
are text files in one git repo you own, on any model with your own keys,
self-hosted or on managed cloud. Every session runs on its own isolated
computer and lands its work as a change request you review and merge.

It ships a **workflow-migration agent**: point it at an n8n workflow export
and it drafts the Kortix agent + skill that does the same job with room to
decide, plus a diff of what changed.

## Why an agent, not another workflow

A workflow engine is the right tool for work that is the same every time: a
webhook fires, three fixed steps run, done. It gets awkward when the work has
branches you did not draw — an invoice that needs a human, a lead that needs
judgment, an error that needs reproducing before it can be fixed.

An **agent** plans, uses tools and runs multi-step work it actually finishes,
inside your own repo. On Kortix the "workflow" becomes an agent file and a
skill you can read, diff and roll back — and the result lands as a change
request instead of a silent run.

See the full comparison at
[n8n-alternative.com/n8n-vs-kortix](https://n8n-alternative.com/n8n-vs-kortix).

## What's in the repo

```
kortix.yaml                  the manifest: image, connectors, triggers
agents/workflow-migrator.md  the agent: turn a workflow into an agent + skill
skills/convert-workflow.md   the steps the migration follows (referenced by the agent)
docs/setup.md                run it on Kortix in ~10 minutes
docs/vs-n8n.md               when a workflow engine stops fitting
docs/faq.md                  licence, models, self-hosting, pricing
```

## Quick start

1. Fork or clone this repo, or copy the files into an existing Kortix project.
2. Connect your tools (a ticket tracker, a CRM, a messaging app) — see
   `docs/setup.md`.
3. Drop an n8n workflow export into `imports/` and run the agent.
4. Read the change request: it contains the new agent, the new skill, and a
   diff of what the migration changed.

## Learn more

- Kortix on the web: https://kortix.com
- Product docs: https://kortix.com/docs
- Kortix on GitHub: https://github.com/kortix-ai/suna
- The campaign site: https://n8n-alternative.com
