# FAQ

**Is Kortix open source?**
Yes. Kortix is the open-source AI Operating System. Your agents, skills,
memory and connectors are text files in one git repo you own, and the harness
is open source too.

**Do I have to self-host it?**
No. Self-host, run it in your own VPC or on-prem, or use managed cloud. The
same repo works in all three.

**Which models can I use?**
Any. Pick the model per agent, per session or per message — Anthropic, OpenAI,
Google, or any OpenAI-compatible endpoint — with your own keys, or the ChatGPT
subscription you already pay for. Model choice is not locked in.

**Do I have to give up n8n?**
No. Many teams keep n8n for fixed, high-frequency pipelines and move
judgment-heavy jobs to a Kortix agent. This starter handles the migration of
one workflow at a time.

**How is this different from n8n?**
n8n runs steps you drew in advance. Kortix runs an agent that plans and
decides, inside your own repo, and lands its work as a change request. See
`docs/vs-n8n.md`.

**Is it safe to let it act?**
Every tool call is ruleable — allow, ask, or block — down to the arguments it
was given. Default is deny for agents, session work lands as a change request,
and connector credentials are brokered server-side and never enter the machine.

**How do I start?**
Follow `docs/setup.md`. About ten minutes, no laptop setup.

**Where are the docs?**
https://kortix.com/docs
