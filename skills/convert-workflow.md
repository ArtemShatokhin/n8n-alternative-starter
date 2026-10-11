# Skill: convert a workflow into an agent (Kortix, the open-source AI Operating System)

This is the step list the `workflow-migrator` agent follows on **Kortix**, the
open-source AI Operating System. Skills are how a company does a job — here,
how it turns a fixed workflow into an agent.

## When to use

An n8n workflow keeps breaking on cases it was not drawn for, or the team
keeps adding "if a human needs to look at this" branches.

## Steps

1. **Inventory the trigger.** What starts the workflow — a webhook, a
   schedule, a new row? Match it to a Kortix trigger (a cron schedule or a
   signed webhook).
2. **List the nodes.** For each node, write one line: what it does and which
   tool it calls. This is the raw material.
3. **Classify.** Mark each node **fixed** (same every run) or **judgment**
   (needs a decision). Merge the fixed nodes into a skill; give the judgment
   nodes to the agent as instructions.
4. **Name the tools.** For every tool the workflow used, decide the
   permission: allow, ask, or block. Default to ask.
5. **Write the files.** Produce `agents/<job>.md` and `skills/<job>.md`.
6. **Verify against the original.** Re-read the export and confirm every node
   is represented or explicitly noted as not represented.
7. **Open a change request.** Commit the files and describe the migration.

## Output

A change request containing the new agent, the new skill, and a short diff.
