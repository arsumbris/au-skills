---
type: guide::au-agent-guides
goal: Check whether a skill improves selection and task performance.
rule: Compare representative tasks with and without the skill when its contribution is uncertain. Grade the intended procedure as well as the final result.
---

# Measure the skill's contribution

Choose tasks and expected outcomes before revising the skill.
Keep the model and environment comparable across runs with and without it.
Reuse current evidence when the relevant behavior has not changed.

**Separate selection from task performance**

Check whether intended requests select the skill.
Check whether similar requests select the right neighbor.
Then check whether using the skill improves the work.
Correct selection alone establishes no improvement in the result.

A check that passes with and without the skill can still protect required behavior.
It does not demonstrate the skill's added value.
Keep such checks when they catch regressions.

**Read the process**

An agent may repair a defective skill during a run and still produce the right result.
Record a required repair as a defect in the tested skill when it changes the skill's:

- Instructions
- Configuration
- Code

Keep the eventual task result as a separate observation.

A planned loop of validation and retries is part of the skill's procedure.
Retrying after invalid task input does not by itself mean the skill is broken.
Grade what the check was meant to establish.
Identify what had to change.

**Match the check to the change**

A description change needs selection evidence.
A body change needs checks of the affected behavior.

A new model or environment may change the skill's value.
Repeat the relevant comparison when prior evidence no longer applies.

Report:

- The tasks
- The configuration
- The observed results
- Any comparisons that did not run

An inspected instruction does not establish an observed success.
