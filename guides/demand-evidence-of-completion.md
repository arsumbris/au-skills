---
type: guide::au-agent-guides
goal: write a skill's completion criteria so the agent proves the work, not just claims it
rule: A model calls a task done when it looks done. Make the completion bar demand evidence, a command run and its output, not "verify it works".
---

# Demand evidence of completion

Put the required evidence in the skill's completion criteria.
A plausible output can lead the agent to report success before checking the result.

A reusable skill can run many times without its author watching.
Its completion criteria need to support a check even when no one reviews the run as it happens.

**Name the evidence**

"Verify it works" names no check.
The agent can satisfy it with a claim.

Specify evidence the agent must produce, such as:

- A command and its output
- Test results
- A screenshot where the requirement concerns appearance
- Another record that establishes the required result

Prefer an objective check when it can establish the requirement.
[[carry-code-for-determinism]] explains how a script can supply one.

Recorded evidence lets a human or later agent review the result without repeating the check.

**Check the required state**

For a state change, check the state itself.
For example, read the saved record or the resulting status.
A page that looks right does not establish that the underlying state changed.

**Preserve the requirement**

Fixing the work and rerunning the check is legitimate debugging.
Weakening the check merely to obtain a pass defeats it.
So does presenting evidence from an earlier run that no longer matches the delivered work.

Correct a demonstrated check defect against the requirement.
Record why the check changed.
Rerun the affected checks and take the evidence from the delivered work.
[[test-first-when-you-can]] applies this to code.

Evaluate required repairs to the skill separately from whether the final work passes.
[[eval-driven-authoring]] covers that authoring check.

**Check the completion criteria**

- Do they name the evidence the agent must produce?
- Does the evidence establish the required state or behavior?
- Could the agent claim success without running the check or by weakening it?
- Does the evidence match the final state?
- Can a human or later agent assess it without repeating the work?
