---
type: guide::au-agent-guides
goal: Decide which instructions must constrain how a task is performed.
rule: Keep a restriction when it protects a stated requirement. Explain the failure it prevents and how to check compliance.
---

# Give each restriction a reason

Start with the requested result and its acceptance criteria.
For each mandatory instruction, identify what would go wrong if it were omitted.
Remove restrictions that merely impose the author's preferred working style.

In this package, a review finding needs a file location and a consequence so the author can investigate it.
Requiring exactly five findings would serve no such purpose: a review may find none.
[[review-a-skill]] therefore specifies what a finding must contain without setting a quota.

Make a required order explicit when one action needs the result of another.
For example, check a reader's finding before editing the skill to address it.
Otherwise an unsupported criticism can become an unnecessary change.

If compliance must be enforced, identify the operation that can reject a violation.
An instruction in a skill cannot supply that enforcement by itself.
Use [[guarantee-vs-guidance]] to check the execution boundary and [[carry-code-for-determinism]] for an executable check.

Try the procedure on a task with different inputs.
If a restriction prevents an acceptable result, narrow it to the condition that actually needs it.
