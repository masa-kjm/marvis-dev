---
name: mvs-execute-work-unit
description: Implement and verify one Work Unit from a work plan, then report the result to the task executor.
---

# mvs-execute-work-unit

Execute one Work Unit by coordinating implementation, verification, and review against its goal, constraints, deliverables, and completion criteria.

## Codebase Map

When repository context is needed, read `.marvis/codebase/README.md` if it exists. Open relevant topics only as needed. Use the map to find sources, and verify important findings against source code, tests, configuration, or repository documentation. If the map is absent or unusable, investigate those sources directly. An absent map alone does not need a report.

Do not update the map as part of this skill. If the map is unusable or an entry fails to locate relevant sources, conflicts with a primary source, links to a missing target, or gives an incorrect responsibility boundary, use verified sources for the task. Report the map path, evidence, and task impact in the final handoff. Surface an unresolved conflict when it affects a current decision.

## Work Execution

- Decide separately whether to delegate implementation and review before starting work.
- Keep small or tightly coupled implementation with this executor when delegation overhead outweighs the benefit.
- Provide each executor with the relevant task definition, constraints, context references, and completion criteria.
- Allow executors to investigate additional context as needed.
- Collect implementation results, verification evidence, and unresolved issues.

## Review

- Check the change against the Work Unit completion criteria after implementation and verification.
- Use a separate sub-agent with `mvs-review-change` when independent review gives a concrete benefit, such as checking substantial changes, complex behavior, document consistency, multiple criteria, or effects on later Work Units.
- If review stays with this executor, apply `mvs-review-change` after verification.
- Give the reviewer the Work Unit goal and completion criteria, original requirements, relevant specifications and architectural constraints, change scope or diff, verification results, and any requested review perspectives. Give references to source material so the reviewer can inspect more context. Do not transfer the full implementation history unless it is needed to explain a decision.
- Use more than one reviewer only when distinct perspectives each justify a separate review. Ask reviewers to report findings with evidence and remaining risks.
- Evaluate the findings against the requirements and constraints. Resolve significant findings, repeat relevant verification, and request another review when a material change needs independent assessment. This executor decides whether the Work Unit is complete.

## Coordination

- Keep Work Plan (check-list) updates under this skill.
- Avoid unnecessary transfer of execution history between sub-agents.
- When a material decision requires user input, explain the decision and its impact. Present a recommended option with its rationale, considering long-term maintainability, compatibility, cost, and reversibility, alongside viable alternatives and their trade-offs.
- Continue work that does not depend on the decision. Do not create a new approval gate for routine implementation choices.

## Handoff

Report the changed files, verification evidence, review findings, unmet criteria, and any discovery that affects other Work Units or the task plan. Give one sentence of reasoning for each decision not to delegate implementation or review.
