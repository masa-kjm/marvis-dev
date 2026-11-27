# marvis-dev

Read the linked skill files for their full instructions.

## Purpose

The `marvis-dev` plugin contains reusable skills for development work.

- Keep skill instructions independent of Codex, Claude Code, Cursor, GitHub Copilot, and other agent tools.
- Keep settings for each tool in separate manifests and marketplace files.
- Use a layout that can adapt as agent tools change.

The other `mvs-*` skills use `.marvis/codebase/README.md` as an entry point when they need repository context. They open relevant topics as needed and check important findings against primary sources. If the map is unavailable, they inspect primary sources directly. They report concrete map problems in their handoffs without changing the map.

The map uses short selection conditions to help readers choose the next source. It can point to feature and module entry points, verification procedures, and repository-specific tools when those pointers reduce search.

## Components

### Skills

| Skill | Purpose |
| --- | --- |
| [`mvs-map-codebase`](skills/mvs-map-codebase/SKILL.md) | Maintain a codebase map in `.marvis/codebase/`. |
| [`mvs-define-spec`](skills/mvs-define-spec/SKILL.md) | Define or revise a specification when requested. |
| [`mvs-manage-work-plan`](skills/mvs-manage-work-plan/SKILL.md) | Create and update a work plan with goals, limits, tasks, and completion criteria. |
| [`mvs-review-change`](skills/mvs-review-change/SKILL.md) | Review changes against requirements and test results. |
| [`mvs-execute-work-unit`](skills/mvs-execute-work-unit/SKILL.md) | Implement and verify one Work Unit. |

## Workflow

These diagrams show how agents can use the skills and their output. Subgraphs mark phases. Rounded nodes refer to other phases. Cylinders show stored repository content. Diamonds show decisions. Rectangles show callers, skills, and actions. Arrows show information transfer or the next action, as stated by their labels. An arrow does not start a skill automatically.

### Map Codebase Phase

```mermaid
flowchart TD
  subgraph Mapping["Map Codebase Phase"]
    Caller["Caller"]
    Sources[("Repository sources")]
    MapSkill["mvs-map-codebase"]
    Map[(".marvis/codebase/")]
  end
  Consumers(["Other Phases"])

  Caller -->|Map request| MapSkill
  Sources -->|Repository facts| MapSkill
  Map -->|Existing map| MapSkill
  MapSkill -->|Create or update| Map
  Map -->|Navigation pointers| Consumers
```

### Specification Definition Phase

```mermaid
flowchart TD
  subgraph Definition["Specification Definition Phase"]
    Caller["Caller"]
    Sources[("Repository sources")]
    SpecSkill["mvs-define-spec"]
    Ready{"Ready for planning?"}
  end
  Planning(["Planning Phase"])

  Caller -->|Specification request| SpecSkill
  Sources -->|Relevant facts| SpecSkill
  SpecSkill -->|Draft and open decisions| Caller
  Caller -->|Decisions or corrections| SpecSkill
  SpecSkill -->|Validated specification| Ready
  Ready -->|No: decisions needed| Caller
  Ready -->|Yes: specification| Planning
```

### Planning Phase

```mermaid
flowchart TD
  subgraph Planning["Planning Phase"]
    Caller["Caller"]
    PlanSkill["mvs-manage-work-plan"]
  end
  Execution(["Execution Phase"])

  Caller -->|Specification| PlanSkill
  PlanSkill -->|Work Plan| Caller
  Planning -->|Work Plan| Execution
  Execution -->|Plan revision required| Planning
```

### Execution Phase

Execute by unit

```mermaid
flowchart TD
  subgraph Execution["Execution Phase"]
    Caller["Caller"]
    ExecuteWU["mvs-execute-work-unit"]
    Implement["Implement change"]
    Verify["Verify result"]
    Review["mvs-review-change"]
    Decision{"Completion Criteria<br/>Satisfied?"}
    Update["Update Work Plan"]
    Report["Report results"]
  end

  Caller -->|"Work Plan (by unit)"| ExecuteWU
  ExecuteWU -->|Implementation task| Implement
  Implement -->|Changed code| ExecuteWU
  ExecuteWU -->|Verification task| Verify
  Verify -->|Change and verification results| Review
  Review -->|Findings and risks| Decision

  Decision -->|No: fix required| ExecuteWU
  Decision -->|Yes: record progress| Update
  Update -->|Updated plan| Report
  Report -->|Work Unit results| Caller
```

- The executor may perform or delegate implementation, verification, and review. Review uses `mvs-review-change` in either case.
