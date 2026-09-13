---
type: guide::au-agent-guides
goal: Keep a skill's context cost proportional to the task.
rule: Keep selection metadata lean and read supporting material when it is needed. Check that the delivery path makes those references available.
---

# Read detail when the task needs it

Separate the information used to select a skill from the instructions used to perform its task.
Put optional detail where the agent can reach it when needed.

**Selection metadata**

The active skill's name and description help the agent choose it.
Keep them focused on the task boundary.
Which skills become active depends on the launch selection and harness.

**The body**

The body supplies the task procedure when the skill is used.
Keep the decisions and completion conditions needed to drive the work.
Point to supporting material instead of copying it into every skill.

**Supporting material**

[[write-a-skill]] reads craft guides at the step that needs them.
It refers native authoring and delivery questions to the owning guide.
This lets a wording edit use less context than a new skill.

In Ars Umbris, native materialization carries the skill's metadata and body.
Supporting guides remain in mounted packages and can be read through `au_agent_guide` by `name::package`.
Check a separate delivery path before relying on adjacent files or scripts.

Make the required reference easy to reach from the step that uses it.
Reuse unchanged evidence instead of rereading it on every step.
Run an inspected script when its output is enough.
Read its source when the task requires that understanding.
[[carry-code-for-determinism]] explains how to make such an operation usable.

To check the design, trace one small task and one task needing the optional detail.
Both should obtain the context they need through an available path.
