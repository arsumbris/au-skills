---
type: guide::au-agent-guides
goal: Decide when to put an operation in code and how to make it usable by an agent.
rule: Use code for an exact transformation or check. Give it explicit inputs, useful failure output and a verified invocation path.
---

# Put exact operations in code

Use code when the agent would otherwise recreate the same algorithm on each run.
A repeatable implementation reduces that variation.
It can still contain bugs or depend on changing inputs and environment state.

**Choose the operation**

Code helps with work such as:

- A fragile transformation with a known algorithm
- Repeated calculations or formatting
- A check with explicit acceptance criteria
- Another operation whose exact behavior is easier to maintain in code

Keep variable judgment in the skill.
Use [[match-the-degrees-of-freedom]] to check which restrictions the task actually needs.

**Help the caller recover**

Supply inputs through:

- Arguments
- Environment variables
- Stdin

Avoid interactive prompts in an unattended path.

Send results to stdout.
Send diagnostics to stderr.
Use exit codes the caller can interpret.

An error should identify the failed input or operation.
It should give the caller a useful next step.

Make retries safe where possible.
For a destructive operation, provide a preview or validation step.
Define what may change between checking and applying it.
[[guarantee-vs-guidance]] distinguishes an available check from an enforced one.

**Describe what the example demonstrates**

Illustration: a file-renaming skill can delegate collision detection and rename-plan construction to a script.
The skill resolves ambiguous names.
It explains the proposed changes.
The operation applying the plan rechecks conflicts before writing.

**Check delivery and use**

Check how the caller obtains the executable.
Check how it invokes the operation.

Native skill materialization does not itself package arbitrary adjacent scripts.
Use a loaded tool or another explicit delivery path when the operation needs one.

Running an inspected operation can avoid loading its source into context on each run.
Read the source when the task requires it, for example:

- To establish trust
- To debug a failure
- To inspect a changed implementation

[[progressive-disclosure]] covers the context tradeoff.
