---
name: mvs-workflow
description: Carry out implementation and reviews based on the plan.
---

# mvs-workflow

Execute the plan by orchestrating implementation and reviews.

## Work Execution

- Delegate a Work Unit when its scope is clear and a sub-agent provides a concrete benefit: safe parallel execution, independent investigation, or focused context for substantial work.
- Keep small or tightly coupled work with the orchestrator when delegation overhead outweighs the benefit.
- Provide each executor with the relevant task definition, constraints, context references, and completion criteria.
- Allow executors to investigate additional context as needed.
- Collect implementation results, verification evidence, and unresolved issues.

## Review

- Use a separate sub-agent for independent review when warranted.
- Provide the reviewer with the original requirements, relevant specifications, implementation diff, and verification results.
- Evaluate whether the implementation satisfies the requirements and architectural constraints.
- Address significant findings and repeat verification as necessary.

## Coordination

- Execute independent Work Units concurrently only when dependencies and writable scopes do not conflict, and integration and verification responsibilities are clear.
- Keep Work Plan updates under orchestrator control.
- Avoid unnecessary transfer of execution history between sub-agents.
- When a material decision requires user input, explain the decision and its impact. Present a recommended option with its rationale, considering long-term maintainability, compatibility, cost, and reversibility, alongside viable alternatives and their trade-offs.
- Continue work that does not depend on the decision. Do not create a new approval gate for routine implementation choices.
