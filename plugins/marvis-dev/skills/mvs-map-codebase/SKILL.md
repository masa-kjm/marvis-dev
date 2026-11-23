---
name: mvs-map-codebase
description: Create or update a repository-specific Codebase Map that helps agents find architecture, conventions, and primary sources.
---

# mvs-map-codebase

## Purpose

Maintain a repository-specific Discovery Index that helps agents locate relevant context efficiently and accurately.

The Codebase Map is a navigation aid, not an authoritative replacement for source code, tests, configuration, or documentation.

## Responsibilities

- Discover repository-specific architecture, responsibilities, boundaries, conventions, and important information sources.
- Maintain a concise, navigable Codebase Map.
- Provide pointers to primary sources for subsequent investigation.
- Update existing information when repository changes affect the map.
- Identify potentially stale, unsupported, or conflicting information.

## Scope

Consider the following information when relevant:

- Repository purpose and overall structure
- Architecture and component relationships
- Module responsibilities and ownership boundaries
- Dependencies and important contracts
- Repository-specific conventions and policies
- Relevant documentation, tests, configuration, and infrastructure
- Important implementation entry points

These categories are discovery guidance, not a mandatory schema.

Record information when it materially reduces future repository investigation, especially when the information is distributed across multiple primary sources or not obvious from repository structure alone.

## Outputs

Maintain the Codebase Map under `.marvis/codebase/`.

- `README.md`: Required entry point and high-level Discovery Index.
- `topics/*.md`: Optional detailed context organized by meaningful repository areas.

Keep the entry point concise and navigable. Create additional files only when they improve independent discovery or maintenance.

## Workflow

1. Inspect the existing Codebase Map, if present.
2. Investigate the repository and identify missing, outdated, or useful discovery information.
3. Read relevant primary sources to establish the facts.
4. Create or update the map, preserving useful existing information.
5. Validate important references and claims.
6. Summarize the changes and any unresolved uncertainties.

Choose investigation methods and scope based on the repository and the requested task.

## Quality Requirements

- Ground repository-specific claims in primary sources.
- Provide useful references for important architectural and boundary information.
- Distinguish documented rules from observed implementation patterns.
- Avoid duplicating detailed source code or existing documentation.
- Avoid speculative descriptions.
- Prefer concise information that supports future context discovery.
- Preserve navigability and avoid unnecessary fragmentation.
- Do not treat existing map content as authoritative without verification.

## Boundaries

This skill does not:

- Decide implementation approaches for individual tasks.
- Produce task-specific Work Plan context.
- Determine whether a code change is correct.
- Replace primary-source investigation by consuming agents.
- Enforce repository policies.

Consumers remain responsible for deciding which context is relevant and verifying the information used for their decisions.
