---
type: guide::au-agent-guides
goal: Author and load a task skill from a native package.
rule: Create a file instance of the skill contract, select it into the launch, and test both discovery and task use.
about: "[[mcp.skill::au-mcp-sdk]]"
---

# Author a skill

Create a markdown instance of [[mcp.skill::au-mcp-sdk]] in the owning package.

Read the current fields.
Supply a name and task description.
Put the instructions in the body.
Declare the SDK vocabulary dependency.

**Use a file instance**

A direct instance is usually enough.
Derive a skill type when it adds a useful shared contract.

Discovery follows the skill closure.
It selects file origins because the instructions live in the file.

**Check the selected capabilities**

The active profile determines which discovered skills reach the launch.
`related-tools` identifies the tool definitions the skill concerns.

Check how the adapter maps `allowed-tools`.
Check how the harness handles permissions before relying on that field.
An association grants no access.
A declaration does not install a missing capability.

**Write for selection and completion**

[[when-a-skill-helps]] helps decide whether the task needs skill guidance.
Use [[the-description-is-the-router]] for its task boundary.
Use [[structure-the-body]] for the procedure.
Use [[write-a-skill]] for drafting and testing.

**Check the native result**

For a new skill or a delivery change, check:

- File discovery
- The selected profile's materialized artifact in the intended launch

A saved skill edit reaches sessions through launch materialization.
Reading its content does not establish that a running session uses it.
[[a-skill-is-launch-static::au-agent-guides]] explains which delivery layer needs refreshing.

Test selection when the description or task boundary changes.
For a body revision, check the affected behavior.
Reuse prior evidence that still applies.

Inspect scoped diagnostics.
Assess reported warnings.

Successful delivery does not establish selection or successful work.
