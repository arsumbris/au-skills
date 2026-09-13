---
type: guide::au-agent-guides
goal: structure a skill that drives code so the agent's own work is checked
rule: For a behavior change, write a requirement-based test and observe its failure before fixing the implementation. Preserve the assertion unless evidence shows the test is wrong.
---

# Test first when you can

Use a test to distinguish required behavior from the current implementation.
Test first when a missing behavior or regression needs that evidence.
Reuse an existing check when it already establishes the requirement.

[[demand-evidence-of-completion]] applies this principle beyond code.
The assertion must represent the requirement.
Preserve it unless evidence shows the test is wrong.

## Check the behavior in order

1. **Write the test**

   - Derive it from the missing behavior or regression in the requirement

2. **Run it**

   - Check that it fails because the behavior is missing
   - Investigate whether an unexpected pass means the behavior exists or the test misses it
   - Correct setup errors before treating a failure as evidence

3. **Preserve the requirement**

   - Keep assertions that establish the requirement
   - Correct a demonstrated test defect against that requirement
   - Record why the test changed
   - Rerun the affected checks

4. **Fix the implementation**

   - Diagnose the failure before editing
   - Use the requirement to locate the problem:
     - The implementation
     - The test
     - The environment

## Check what the test establishes

A test makes its encoded assertion repeatable.
[[carry-code-for-determinism]] explains that benefit.
Review the assertion to check that it represents the requirement.
[[structure-the-body]] places the check in the procedure.

Prefer a real integration.
Mock only an external service.
A mock that supplies the expected result can hide the missing implementation.
Excessive mocking can merely reproduce the implementation the agent just wrote.

## Check the skill's procedure

- Does a new test address a missing behavior or regression?
- Is the test written and observed to fail before fixing the code?
- Is a test edit justified against the requirement?
- Does it mock only what is external?
