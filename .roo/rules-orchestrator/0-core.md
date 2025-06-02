---
description: Core guidelines for Orchestrator mode workflows and escalation patterns
tags: ['orchestrator', 'workflow', 'mode-switching']
globs: ['*']
---

## Core Workflow Rules

- **User workflow requests** - Users can specify workflows like 'use complex feature workflow' or 'use research workflow'
- **Task Master integration** - Include Task Master mode in workflow when:
  - Explicitly requested by user
  - User provides a specific task from [`notes/tasks/tasks.md`](notes/tasks/tasks.md) to work on - always return to Task Master mode after completing this task

## Mode Selection Criteria

- **Ask mode** - Use for information gathering, clarification, research questions
- **Architect mode** - Use for system design, planning, technical architecture decisions (only output plan to file if requested by user)
- **Code mode** - Use for implementation, bug fixes, code changes, refactoring
- **Debug mode** - Use for systematic problem diagnosis, testing, troubleshooting
- **Task Master mode** - Use for task management, progress tracking, [`notes/tasks/tasks.md`](notes/tasks/tasks.md) updates
- **Documentation mode** - Shouldn't be used by orchestrator

## Workflow Decision Matrix

| Task Type   | Complexity | From tasks.md? | Recommended Workflow                         |
| ----------- | ---------- | -------------- | -------------------------------------------- |
| Bug Fix     | Simple     | No             | Code                                         |
| Bug Fix     | Complex    | No             | Debug → Code                                 |
| Bug Fix     | Simple     | Yes            | Code → Task Master                           |
| Bug Fix     | Complex    | Yes            | Debug → Code → Task Master                   |
| Feature     | Simple     | No             | Code                                         |
| Feature     | Complex    | No             | Architect → Code                             |
| Feature     | Simple     | Yes            | Code → Task Master                           |
| Feature     | Complex    | Yes            | Architect → Task Master → Code → Task Master |
| Research    | Any        | No             | Ask                                          |
| Planning    | Any        | No             | Ask → Architect → Task Master (if requested) |
| Maintenance | Any        | No             | Code → Debug                                 |

## Best Practices

- **Always assess task complexity** before choosing workflow path
- **Use decision matrix** when workflow choice is unclear
