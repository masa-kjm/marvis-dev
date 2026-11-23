---
name: mvs-execute-work-unit
description: Implement and verify one Work Unit from a work plan, then report the result to the task executor.
---

# mvs-execute-work-unit

Execute one Work Unit by coordinating implementation, verification, and review against its goal, constraints, deliverables, and completion criteria.

## Work Execution

- Keep small or tightly coupled work with the orchestrator when delegation overhead outweighs the benefit.
- Provide each executor with the relevant task definition, constraints, context references, and completion criteria.
- Allow executors to investigate additional context as needed.
- Collect implementation results, verification evidence, and unresolved issues.

## Review

- Check the change against the Work Unit completion criteria after implementation and verification.
- Use a separate sub-agent with `mvs-review-change` when independent review gives a concrete benefit, such as a fresh assessment of substantial changes, a distinct risk area, or a focused review of complex behavior. Keep small changes with this executor when delegation adds little value.
- Give the reviewer the Work Unit goal and completion criteria, original requirements, relevant specifications and architectural constraints, change scope or diff, verification results, and any requested review perspectives. Give references to source material so the reviewer can inspect more context. Do not transfer the full implementation history unless it is needed to explain a decision.
- Use more than one reviewer only when distinct perspectives each justify a separate review. Ask reviewers to report findings with evidence and remaining risks.
- Evaluate the findings against the requirements and constraints. Resolve significant findings, repeat relevant verification, and request another review when a material change needs independent assessment. This executor decides whether the Work Unit is complete.

## Coordination

- Keep Work Plan (check-list) updates under this skill.
- Avoid unnecessary transfer of execution history between sub-agents.
- When a material decision requires user input, explain the decision and its impact. Present a recommended option with its rationale, considering long-term maintainability, compatibility, cost, and reversibility, alongside viable alternatives and their trade-offs.
- Continue work that does not depend on the decision. Do not create a new approval gate for routine implementation choices.

## Handoff

Report the changed files, verification evidence, review findings, unmet criteria, and any discovery that affects other Work Units or the task plan.
