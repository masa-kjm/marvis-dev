---
name: mvs-define-spec
description: Define or revise a specification when the user requests specification writing, requirements analysis, or design decisions as a distinct task.
---

# mvs-define-spec

Help the user clarify their intent, evaluate requirements and design decisions, and define a specification suitable for subsequent planning and verification.

Use this skill when specification or requirements analysis is a distinct requested task. Handle routine clarification within ordinary development work without starting a separate specification phase.

## Codebase Map

When repository context is needed, read `.marvis/codebase/README.md` if it exists. Open relevant topics only as needed. Use the map to find sources, and verify important findings against source code, tests, configuration, or repository documentation. If the map is absent or unusable, investigate those sources directly. An absent map alone does not need a report.

Do not update the map as part of this skill. If the map is unusable or an entry fails to locate relevant sources, conflicts with a primary source, links to a missing target, or gives an incorrect responsibility boundary, use verified sources for the task. Report the map path, evidence, and task impact in the final handoff. Surface an unresolved conflict when it affects a current decision.

## Requirement Exploration

- Understand the user's intent, background, desired outcomes, and existing requirements.
- Investigate relevant repository context when it affects the requirements or design decisions.
- Identify material ambiguities, missing requirements, conflicting constraints, and significant risks.
- Consider relevant alternatives and explain their trade-offs when a decision is needed.
- Adapt the investigation and discussion to the nature and complexity of the task. Avoid unnecessary questions and rigid procedures.

## Specification Definition

Capture the information necessary to communicate the intended change, including when relevant:

- Background and intent
- Goal
- Requirements
- Scope and non-goals
- Constraints
- Acceptance criteria
- Important decisions and their rationale
- Open questions and assumptions
- References to relevant sources

Choose a structure and level of detail appropriate to the task. Do not treat these categories as a mandatory schema.

Distinguish confirmed requirements, proposed decisions, and unresolved assumptions. Do not silently turn suggestions into requirements or resolve material ambiguities without evidence or user agreement.

Include technical design decisions when they are necessary to define the intended behavior, contracts, or constraints. Leave routine implementation decisions to subsequent planning and execution.

## Specification Validation

Before finalizing or materially revising a specification:

- Check alignment with the user's original intent.
- Check for missing, ambiguous, or conflicting requirements.
- Check relevant repository constraints and existing contracts.
- Consider significant edge cases, failure behavior, compatibility, and operational implications when applicable.
- Ensure acceptance criteria are concrete and verifiable.
- Identify unresolved decisions that prevent reliable planning.

Revise the specification when validation reveals deficiencies.

## Handoff

Provide the specification in the requested format and location.

State whether the specification is ready for planning. Identify decisions that block planning and who must make them. Record other uncertainties for planning or implementation.

Keep the specification focused on the intended outcome and applicable constraints rather than decomposing implementation work.
