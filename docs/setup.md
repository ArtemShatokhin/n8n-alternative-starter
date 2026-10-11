# Run this starter on Kortix

Kortix is the open-source AI Operating System. This template migrates a fixed
n8n workflow into an agent that can decide and act.

Time: about 10 minutes, no laptop setup.

## 1. Get the files into a repo you own

Fork this repo, or copy `agents/`, `skills/`, `kortix.yaml` and `docs/` into
an existing Kortix project. The repo *is* the company — agents, skills,
memory and connector config are all text files here.

## 2. Edit the manifest

Open `kortix.yaml`. Set the connectors the agent may reach (start with
`github` and `slack`). Leave `permissions.default: ask` until you trust the
tool calls, then move a specific tool to `allow`.

## 3. Connect your tools

Point Kortix at the systems the old workflow touched — a ticket tracker, a
CRM, a messaging app. Connector credentials are brokered server-side and never
enter the machine, so you wire up Slack or a CRM without pasting keys into a
config.

## 4. Drop in a workflow

Export an n8n workflow to JSON, put it in `imports/`, and run the
`workflow-migrator` agent against the repo.

## 5. Read the change request

The agent opens a change request with the new agent file, the new skill, and a
diff of what the migration changed. Review it as a diff, then merge.

## 6. Give it a schedule

Once it runs reliably, add a trigger (cron or a signed webhook) so migrations
of new workflows start on their own.

## Where to go next

- Product docs: https://kortix.com/docs
- The comparison with a workflow engine:
  https://n8n-alternative.com/n8n-vs-kortix
