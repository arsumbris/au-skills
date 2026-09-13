---
type: guide::au-agent-guides
goal: Decide whether a constraint needs guidance or an enforced check.
rule: Put a required invariant in the execution path that controls the action. A script named in skill prose still depends on the agent invoking it.
---

# Put enforcement in the controlled path

Code supplies an exact operation when invoked.
Enforcement also needs a path that runs the check and refuses the invalid action.

**Guidance**

A skill or inject explains what the agent should do.
Use it for decisions that need judgment and adaptation.
The agent may still miss an instruction.

**Enforcement**

Place an invariant at the boundary that controls the action.
A mediator can reject a tool call through its configured path.
A script invoked only at the agent's discretion can be skipped.

Check the mechanism's scope and failure behavior.
An observer records events but does not prevent them.
A successful validation establishes only what its checks cover.
[[pick-the-vehicle::au-agent-guides]] distinguishes the runtime mechanisms.

**Combine them**

Illustration: a skill explains how to prepare a migration.
The operation applying it refuses a plan that fails its validation.
The skill guides the preparation.
The operation enforces the check.

If one missed instruction would violate correctness, identify the boundary that catches it.
Check a failing case through that path.
Name any available path that bypasses the check before claiming enforcement.
