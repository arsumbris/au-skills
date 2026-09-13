---
type: mcp.skill::au-mcp-sdk
name: review-a-skill
description: Returns an independent review of an existing agent skill or guide, with supported findings and proposed fixes. Use for review requests and checks before release. For edits, use write-a-skill or write-a-guide. Engine diagnostics alone do not require this skill.
---

# Review a skill or guide

Read the complete target file and establish the requested scope.
Inspect current diagnostics, refreshing them if absent or stale.
Read the owning contract or implementation when a finding depends on it.

Give a fresh reader the artifact, applicable criteria, evidence and neighboring descriptions or guide goals.
Use [[the-independent-checker]] for that setup.
Keep delegation within the caller's authorization and report when independent reading is unavailable.

Read supporting guides through `au_agent_guide` using `name::au-skills` as needed.

## Assess the artifact

For a skill, check:

- Can the agent distinguish its job from neighboring skills? Use [[name-the-skill]] and [[the-description-is-the-router]].
- Can the procedure reach a checked result, including recovery from a failed step? Use [[structure-the-body]].
- Does each mandatory restriction protect a requirement? Use [[match-the-degrees-of-freedom]].
- What does the skill add to the task? Use [[when-a-skill-helps]], [[gotchas-first]] and [[write-less-as-models-improve]].

For a guide, use [[write-a-useful-guide::au-agent-guides]] and [[a-guide-earns-its-slot::au-agent-guides]].
Check that it helps with a distinct decision, explains when its advice applies and supports factual claims with inspectable evidence.
Distinguish illustrations from observed results and recommendations from runtime enforcement.
Compare neighboring guides before proposing another entry.

## Return supported findings

Check the reader's findings against the file and evidence.
For each confirmed problem, give its location, consequence, applicable requirement and proposed fix.
Order findings by their effect on task success.

A reading can expose an ambiguous instruction; a claim about actual selection or execution needs an observed trial.
Keep those conclusions separate.
Report a clean review when no supported problem remains, and state unresolved questions, unrun checks and limits to independence.
