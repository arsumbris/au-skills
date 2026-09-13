---
type: guide::au-agent-guides
goal: Reassess old instructions when the model or environment changes.
rule: Test whether an instruction is still needed before removing it. Preserve requirements that the result must continue to satisfy.
---

# Recheck old instructions

A procedure can retain workarounds for behavior that has changed.
After a model or environment update, revisit the tasks those workarounds were intended to fix.

Try the revised procedure on representative tasks with the current setup.
Compare the results against the requirements, including cases the old instruction protected.
Use [[eval-driven-authoring]] when the instruction's contribution is uncertain.

Remove a workaround when the comparison supports doing so.
One successful run does not establish that a rare failure is gone.
Keep required checks even when the model usually produces an acceptable result without them.

Record which tasks were checked and which remain uncertain.
