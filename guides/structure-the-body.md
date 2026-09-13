---
type: guide::au-agent-guides
goal: choose a skill body structure that makes the task and completion conditions clear
rule: Order steps when sequence matters. Give fragile operations a check that establishes completion.
---

# Structure the body for the task

Use ordered steps when later actions depend on earlier ones.
For judgment tasks, state the outcome and the criteria that guide the decision.

Give the agent enough to begin and finish:

- Workable inputs
- Decisions it can make
- A stopping condition

A checklist helps track required work across a long workflow.
A validator helps when it can establish that a fragile operation succeeded.
Choose these for the failure they prevent.

State what completes the task and what requires recovery.
[[write-a-skill]] separates selecting the skill from checking its task results.
The author checks review findings before resolving confirmed problems.
That order prevents a reader's unsupported finding from becoming an automatic edit.

Check task results separately from whether the skill was selected.
A selectable description does not establish that the procedure works.

To check the procedure, walk a realistic task through the body.
Check that it makes the required order and completion conditions clear.
