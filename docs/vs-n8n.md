# When a workflow engine stops fitting (n8n vs Kortix)

n8n is a strong open-source workflow engine. Kortix is an open-source AI
Operating System. They overlap more than they look, and the useful question
is which shape of work you actually have.

## What you are choosing

| Question | Workflow engine (n8n) | Kortix (this starter) |
|---|---|---|
| Primary job | Run a fixed set of steps you drew | Run an agent that plans, decides and finishes work |
| When it breaks | On a case you did not draw | The agent reasons about the case |
| Where the logic lives | The workflow canvas / DB | Agent + skill files in one git repo |
| Where work lands | A silent run + logs | A change request against your repo |
| Permissions | Node/credential level | Per tool call (allow / ask / block) |
| Model choice | Limited | Any model, per agent / session / message; your keys |
| Licence | Open source | Open source |

## The tell

If your workflow has grown a branch for "what if a human needs to look at
this," or a sub-workflow that fires when the automation is wrong, the work is
not really a workflow. It is a job with judgment, and it wants an agent.

## Keep the fixed parts

You do not have to throw the engine away. The common pattern: leave genuinely
fixed, high-frequency pipelines in n8n and move the judgment-heavy jobs to a
Kortix agent. This starter helps with the second half — it reads an exported
workflow and drafts the agent and skill that do the same job with room to
decide.

Try it: clone the repo, follow `docs/setup.md`. Full head-to-head at
[n8n-alternative.com/n8n-vs-kortix](https://n8n-alternative.com/n8n-vs-kortix).
