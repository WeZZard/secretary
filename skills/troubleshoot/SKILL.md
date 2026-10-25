---
name: troubleshoot
description: "Use when a bug or defect is reported."
---

# Troubleshoot

Drive an end-to-end troubleshooting process with the reproduction, the root cause analysis and the architectural fix plan.

## Process

1. **Build an end-to-end reproducer of the reported issue.**
   - Read the user message as an issue report.
   - Reproduce the issue exactly as reported before touching any code.
   - The reproducer **MUST** run end to end against the real system boundaries that the report describes, not against mocks of the component under suspicion.
   - The reproducer **MUST** fail deterministically before the fix and pass deterministically after the fix. Keep it as a regression test.

2. **Drive the troubleshooting process with the reproducer.**
   - Form a hypothesis, change one variable, and rerun the reproducer.
   - A hypothesis is confirmed only when the reproducer's outcome changes as predicted.
   - You **MUST NOT** claim a root cause that the reproducer has not demonstrated.

3. **Develop an architectural fix and update the relevant documents.**
   - Prefer a fix at the architectural level over a local workaround. A local workaround is acceptable only when the architectural fix is documented as follow-up work.
   - Update every document that describes the changed behavior, contract, or invariant.
   - You **MUST** follow the `documentation` skill when updating documents.

4. **Build a plan in the `.plans` directory citing the document changes.**
   - Write the plan as a file under the project's `.plans/` directory.
   - Each plan item that changes behavior **MUST** cite the document sections it makes true.
   - The plan must state how the reproducer verifies the fix.
