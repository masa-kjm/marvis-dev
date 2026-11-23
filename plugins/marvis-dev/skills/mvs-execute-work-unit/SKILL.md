---
name: mvs-execute-work-unit
description: Implement and verify one Work Unit from a work plan, then report the result to the task executor.
---

# mvs-execute-work-unit

Execute one Work Unit  by orchestrating implementation and reviews against its goal, constraints, deliverables, and completion criteria.

## Work Execution

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

- Keep Work Plan (check-list) updates under this skill.
- Avoid unnecessary transfer of execution history between sub-agents.
- When a material decision requires user input, explain the decision and its impact. Present a recommended option with its rationale, considering long-term maintainability, compatibility, cost, and reversibility, alongside viable alternatives and their trade-offs.
- Continue work that does not depend on the decision. Do not create a new approval gate for routine implementation choices.

## Handoff

Report the changed files, verification evidence, review findings, unmet criteria, and any discovery that affects other Work Units or the task plan.
