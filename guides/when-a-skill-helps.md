---
type: guide::au-agent-guides
goal: Decide whether a recurring task needs a skill.
rule: Identify a missing procedure and a task it would improve before adding another skill.
---

# Identify the missing procedure

Start with a request that the current setup handles poorly.
Describe what the agent needs to do differently and whether that need is likely to recur.
A one-time instruction may be enough for a one-time task.

Check where the missing information belongs.
A field's accepted values belong with its type contract.
A procedure spanning several decisions may belong in a skill.
[[pick-the-vehicle::au-agent-guides]] covers the available mechanisms.

For this package, valid skill metadata alone is insufficient: the author must also check delivery, selection and task results.
[[write-a-skill]] connects those checks into an authoring procedure.

When the benefit is uncertain, compare the same task with and without the proposed guidance.
Use [[eval-driven-authoring]] to record the comparison and its limits.
Keep only the guidance for which you can explain a useful contribution.
