---
name: mvs-workflow
description: Carry out implementation and reviews based on the plan.
---

# mvs-workflow

Execute the plan by orchestrating implementation and reviews.

## Work Execution

- Delegate Work Units to sub-agents when appropriate.
- Provide each executor with the relevant task definition, constraints, context references, and completion criteria.
- Allow executors to investigate additional context as needed.
- Collect implementation results, verification evidence, and unresolved issues.

## Review

- Use a separate sub-agent for independent review when warranted.
- Provide the reviewer with the original requirements, relevant specifications, implementation diff, and verification results.
- Evaluate whether the implementation satisfies the requirements and architectural constraints.
- Address significant findings and repeat verification as necessary.

## Coordination

- Execute independent Work Units concurrently when safe.
- Consider dependencies, shared files, and integration risks.
- Keep Work Plan updates under orchestrator control.
- Avoid unnecessary transfer of execution history between sub-agents.
