---
type: mcp.skill::au-mcp-sdk
name: write-a-skill
description: Creates or revises an agent skill, including its task boundary, instructions and checks. Use for requests to write or improve a skill. For findings without edits, use review-a-skill; for guide authoring, use write-a-guide.
---

# Write a skill

Establish the request the skill owns and the result it should produce.
Use the user's requirements and the existing package to decide what needs changing.
For a new skill, identify the missing procedure with [[when-a-skill-helps]].

Read supporting guides through `au_agent_guide` using `name::au-skills` when the task needs them.
For native file contracts, package dependencies or launch delivery, use [[author-a-skill]].

## Make the change

Write the procedure around the inputs, decisions and completion check.
Use [[structure-the-body]] for ordering and [[match-the-degrees-of-freedom]] to justify mandatory instructions.
Keep the name and description distinct from neighboring skills; see [[name-the-skill]] and [[the-description-is-the-router]].

Address known mistakes at the affected step using [[gotchas-first]].
Use [[carry-code-for-determinism]] when an operation needs an executable implementation and [[guarantee-vs-guidance]] when a requirement needs enforcement.
Keep optional detail reachable through [[progressive-disclosure]].

## Check the saved result

Choose checks for the change:

- For a new skill or a changed task boundary, try requests it should own and similar requests it should leave to another skill.
- For a procedure change, check the affected task result. Use [[eval-driven-authoring]] for a new skill's baseline or when its added value is uncertain.
- For a delivery change, inspect discovery and the intended launch artifact through [[author-a-skill]].

Reuse evidence while its task, model and environment remain applicable.
Inspect current diagnostics; request `au_diagnostics` when they are absent or stale.
Fix introduced errors and assess warnings.

For substantial new guidance or a requested independent review, use [[review-a-skill]] and [[the-independent-checker]].
Keep checks and delegation within the caller's authorization; report when an independent reader is unavailable.
Check findings before acting on them.
Resolve supported problems and explain rejected findings.

Remove redundant instructions using [[write-less-as-models-improve]] and recheck behavior affected by the cuts.
Return the saved path, what changed, observed check results and any unresolved findings or checks that did not run.
