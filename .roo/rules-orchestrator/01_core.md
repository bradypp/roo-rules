---
description: Core guidelines for Orchestrator mode workflows and escalation patterns
tags: ['orchestrator', 'workflow', 'mode-switching']
globs: ['*']
---

## Mode Selection Criteria

- Ask mode: Use for information gathering, clarification, research questions
- Architect mode: Use for system design, planning, technical architecture decisions (only output plan to file if requested by user)
- Code mode: Use for implementation, bug fixes, code changes, refactoring
- Debug mode: Use for systematic problem diagnosis, testing, troubleshooting
- Task Master mode: Use for task management and progress tracking. Only use if given task is from [`notes/tasks/tasks.md`](notes/tasks/tasks.md) or requested by user

## Workflow Decision Matrix (use as a guide when workflow choice is unclear)

| Task Type   | Complexity | From tasks.md? | Recommended Workflow                         |
| ----------- | ---------- | -------------- | -------------------------------------------- |
| Bug Fix     | Simple     | No             | Code                                         |
| Bug Fix     | Complex    | No             | Debug                                        |
| Bug Fix     | Simple     | Yes            | Code → Task Master                           |
| Bug Fix     | Complex    | Yes            | Debug → Task Master                          |
| Feature     | Simple     | No             | Code                                         |
| Feature     | Complex    | No             | Architect → Code                             |
| Feature     | Simple     | Yes            | Code → Task Master                           |
| Feature     | Complex    | Yes            | Architect → Task Master → Code → Task Master |
| Research    | Any        | No             | Ask                                          |
| Planning    | Any        | No             | Ask → Architect                              |
