---
type: guide::au-agent-guides
goal: Choose a skill name that distinguishes its job within the package.
rule: Name the work the caller is asking for. Resolve ambiguity against the other names in the same package.
---

# Name the job the caller needs

List the requests the skill owns and compare them with neighboring skills.
Choose a short name that makes the intended destination recognizable.
Check the allowed form against [[mcp.skill::au-mcp-sdk:example]].

This package uses `write-a-skill` for creating or changing a skill and `review-a-skill` for returning findings about one.
Calling both `skill-craft` would hide the distinction between an edit and a review.
The paired names make that distinction visible before the descriptions are read.

Use [[the-description-is-the-router]] to explain boundaries that the name cannot carry.
Do not stretch the name into a list of every supported operation.

Before renaming a published skill, locate its callers and references.
Update them together, or arrange compatibility through the owning delivery mechanism.
