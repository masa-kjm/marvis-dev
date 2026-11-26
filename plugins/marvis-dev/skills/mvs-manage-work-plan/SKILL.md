---
name: mvs-manage-work-plan
description: Create, validate, and maintain executable work plans for medium-to-large development tasks.
---

# mvs-manage-work-plan

Create and maintain a work plan that guides execution and verification.

## Codebase Map

When repository context is needed, read `.marvis/codebase/README.md` if it exists. Open relevant topics only as needed. Use the map to find sources, and verify important findings against source code, tests, configuration, or repository documentation. If the map is absent or unusable, investigate those sources directly. An absent map alone does not need a report.

Do not update the map as part of this skill. If the map is unusable or an entry fails to locate relevant sources, conflicts with a primary source, links to a missing target, or gives an incorrect responsibility boundary, use verified sources for the task. Report the map path, evidence, and task impact in the final handoff. Surface an unresolved conflict when it affects a current decision.

## Task Definition

Define the following for the overall task:

- **Goal**: The intended outcome.
- **Context**: Essential background, relevant architectural boundaries, and references to information needed for execution.
- **Constraints**: Requirements and boundaries that must be respected.
- **Deliverables**: Expected outputs.
- **Completion Criteria**: Concrete, verifiable conditions represented as an updateable checklist.

Use specifications, repository exploration, and other available sources to identify relevant context.

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
- Check Work Unit dependencies, the verifiability of Completion Criteria, and verification of the integrated result.
- Check consistency with known architectural boundaries and constraints.
- Identify unresolved assumptions, missing context, and significant risks.
- For plans with substantial scope, complex dependencies, or significant uncertainty, request an independent review with fresh context. Give the reviewer the original request, specifications, plan, and pointers to relevant repository sources. Ask the reviewer to check requirement coverage, repository assumptions, dependencies, Completion Criteria, and integration verification. The reviewer must not edit the plan; ask for evidence-based findings that distinguish confirmed defects, unverified assumptions, and execution blockers, plus remaining risks.
- Revise the plan when validation reveals deficiencies.

Do not silently invent requirements or resolve material ambiguities without evidence.

## Plan Maintenance

During execution:

- Update Work Unit progress and Completion Criteria based on evidence.
- Record discoveries that materially affect the plan.
- Treat external edits to the plan as potentially intentional.
- Preserve the existing structure, original intent, and user-defined requirements unless a revision is necessary or the user explicitly changes them.
- When findings invalidate the plan or requirements, assumptions, or implementation constraints change, revise the affected sections and Work Units.
- Revalidate the plan after material revisions.

Do not mark criteria complete without verification.

Do not remove unmet requirements merely to make the plan appear complete.

## Completion

Before declaring the task complete:

- Verify the final deliverables against the original request and applicable specifications.
- Check all task-level Completion Criteria, not only individual Work Unit criteria.
- Record any unmet criteria or remaining limitations.
