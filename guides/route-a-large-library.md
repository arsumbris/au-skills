---
type: guide::au-agent-guides
goal: Keep a large skill library findable without loading every description.
rule: Narrow the active set when selection or context cost warrants it. A router needs a delivery path that actually controls which skills load.
---

# Narrow the active skill set

Keep a flat list while it remains easy to select the right skill.
Consider grouping when observed selection failures or context cost justify another step.
[[curate-dont-accumulate]] helps decide which skills deserve to remain available.

**Check the actual listing**

Installed and active skills can differ.
Inspect the metadata the intended session receives.
Listing budgets and truncation behavior depend on the harness.
Do not assume a universal skill-count threshold.

**Choose the grouping**

Group skills by task boundaries the caller can distinguish.
A broad description selects the domain.
The leaf descriptions distinguish tasks within it.
Use [[the-description-is-the-router]] for those boundaries.

The extra choice has a cost.
A wrong domain can hide the right skill.
Test requests near the boundary before adopting the hierarchy.

**Connect the grouping to delivery**

In Ars Umbris, a launch profile can select a subset of discovered skills.
A router's prose alone does not remove leaf descriptions from the launch context.
Loading additional guidance during a task needs an available discovery and reading path.
[[a-skill-is-launch-static::au-agent-guides]] explains the delivery layers.

A query can keep the candidate list current with the graph.
It does not establish that the grouping or descriptions remain useful.
Check those judgments when the library changes.

To check a grouping, compare how much the agent reads and how often it selects correctly.
Keep the simpler list if the extra stage adds cost without improving the result.
