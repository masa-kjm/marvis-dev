---
name: mvs-review-change
description: Review implementation changes against requirements, specifications, and relevant quality constraints.
---

# mvs-review-change

Review a change against its requirements and constraints. Use a fresh assessment when this skill is assigned to a separate reviewer.

## Review Context

Understand:

- The goal and completion criteria for the change
- Original requirements and relevant specifications
- Relevant architectural constraints
- The change scope or diff
- Verification results and known uncertainties

Inspect source material and gather additional context when the handoff is incomplete or a finding needs verification. Do not rely on the implementer's assessment as proof that the change is correct.

## Review Perspectives

- Select review perspectives that match the change and its risks.
- Cover perspectives requested by the caller first. Include another perspective when the evidence shows a significant risk.
- Load relevant guidance from `references/` when useful.
- Avoid applying irrelevant checklists mechanically.

## Review

- Evaluate the change against the goal, completion criteria, requirements, and constraints.
- Identify correctness issues, regressions, and constraint violations.
- Support each finding with a location and concrete evidence. Explain which requirement or behavior is affected.
- Distinguish confirmed issues from potential risks.
- Do not assume the implementation is correct merely because tests pass.

## Output

Report:

- Findings with severity, location, evidence, and impact
- Unverified assumptions and remaining risks
- An overall assessment against the completion criteria
