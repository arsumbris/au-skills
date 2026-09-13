---
type: guide::au-agent-guides
goal: Help the agent distinguish requests owned by this skill from nearby work.
rule: Describe the request and expected result, then check ambiguous requests against neighboring skills.
---

# Make the task boundary visible

Write the description so a caller can distinguish this skill from the others available in the session.
Use [[name-the-skill]] for the short name and [[mcp.skill::au-mcp-sdk:example]] for the field contract.

In this package, a request to improve a skill belongs to `write-a-skill`.
A request for findings about an existing skill belongs to `review-a-skill`.
Their descriptions should expose that difference without requiring the agent to read both procedures.

Try requests that belong to each skill, including an ambiguous case near the boundary.
Record which skill was selected and why a different selection would be a problem.
Revise a description when it obscures that distinction.

If the expected skill is missing, check its availability through [[author-a-skill]] before changing its wording.
A description cannot select a skill that the launch never supplied.

Check the resulting work separately.
Selection tells you which procedure ran; it does not tell you whether that procedure succeeded.
