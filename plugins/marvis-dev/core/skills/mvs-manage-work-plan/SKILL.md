---
name: mvs-manage-work-plan
description: Create, validate, and maintain executable work plans for medium-to-large development tasks.
---

# mvs-manage-work-plan

Create and maintain a work plan that guides execution and verification.

## Task Definition

Define the following for the overall task:

- **Goal**: The intended outcome.
- **Context**: Essential background, relevant architectural boundaries, and references to information needed for execution.
- **Constraints**: Requirements and boundaries that must be respected.
- **Deliverables**: Expected outputs.
- **Completion Criteria**: Concrete, verifiable conditions represented as an updateable checklist.

Use codebase maps, specifications, repository exploration, and other available sources to identify relevant context.

Keep context concise. Include essential findings and pointers to authoritative sources rather than duplicating extensive documentation.

## Work Units

Decompose the task into Work Units when doing so improves execution or verification.

Each Work Unit should define:

- Goal
- Context
- Constraints
- Deliverables
- Completion Criteria
- Dependencies, when applicable

Inherit task-level context and constraints unless overrides or additional details are necessary.

Avoid unnecessary decomposition.

## Plan Validation

Before finalizing or substantially revising the plan:

- Review the original request and applicable specifications.
- Verify that the plan covers all known requirements.
- Verify that the Work Units collectively support the overall Goal and Completion Criteria.
- Check consistency with known architectural boundaries and constraints.
- Identify unresolved assumptions, missing context, and significant risks.
- Revise the plan when validation reveals deficiencies.

Do not silently invent requirements or resolve material ambiguities without evidence.

## Plan Maintenance

During execution:

- Update Work Unit progress and Completion Criteria based on evidence.
- Record discoveries that materially affect the plan.
- Revise affected Work Units when requirements, assumptions, or implementation constraints change.
- Preserve the original intent and requirements unless explicitly changed.
- Revalidate the plan after material revisions.

Do not mark criteria complete without verification.

do not remove unmet requirements merely to make the plan appear complete.

## Plan Updates

- When updating progress, preserve the existing plan structure and requirements unless a revision is necessary.
- When new findings invalidate the plan, revise the affected sections and revalidate the plan.
- Preserve user-defined requirements unless explicitly changed by the user.
- Do not mark completion criteria as satisfied without evidence.
- Treat external edits to the plan as potentially intentional.

## completion

before declaring the task complete:

- verify the final deliverables against the original request and applicable specifications.
- check all task-level completion criteria, not only individual work unit criteria.
- record any unmet criteria or remaining limitations.
