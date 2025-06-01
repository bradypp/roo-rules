---
description: Core guidelines for Orchestrator mode workflows and escalation patterns
tags: ['orchestrator', 'workflow', 'mode-switching']
globs: ['*']
---

## Core Workflow Rules

- **User workflow requests** - Users can specify workflows like 'use complex feature workflow' or 'use research workflow'
- **Task Master integration** - Include Task Master mode in workflow when:
  - Explicitly requested by user
  - User provides a specific task from [`tasks.md`](tasks.md) to work on - always return to Task Master mode after completing this tasks to update [`tasks.md`](tasks.md)
- **Documentation completion** - Always finish workflows with Documentation mode to:
  - Update relevant files in [`docs/`](docs/) directory
  - Update [`CHANGELOG.md`](CHANGELOG.md) with completed work
  - Ensure project documentation stays current

## Mode Selection Criteria

- **Ask mode** - Use for information gathering, clarification, research questions
- **Architect mode** - Use for system design, planning, technical architecture decisions
- **Code mode** - Use for implementation, bug fixes, code changes, refactoring
- **Debug mode** - Use for systematic problem diagnosis, testing, troubleshooting
- **Task Master mode** - Use for task management, progress tracking, [`tasks.md`](tasks.md) updates
- **Documentation mode** - Use for writing/updating docs or [`CHANGELOG.md`](CHANGELOG.md)

## Escalation Patterns

### Information → Planning

- **Ask → Architect** - When research reveals need for architectural decisions
- **Ask → Task Master** - When questions lead to actionable task creation
- **Ask → Documentation** - When gathering information for documentation updates

### Planning → Implementation

- **Architect → Task Master** - When architectural plans need task breakdown
- **Architect → Code** - When design is clear and ready for direct implementation
- **Task Master → Code** - When tasks are well-defined and ready for coding

### Implementation → Quality Assurance

- **Code → Debug** - When implementation encounters issues or needs testing
- **Code → Task Master** - When implementation is complete and tasks need status updates
- **Debug → Code** - When root cause is identified and fix is clear

### Completion → Documentation

- **Code → Documentation** - When features are complete and need documentation
- **Task Master → Documentation** - When project phase is complete and [`CHANGELOG.md`](CHANGELOG.md) needs updates
- **Debug → Documentation** - When issues are resolved and solutions need documenting

## Collaborative Workflows

### Simple Implementation

**Orchestrator → Code → Documentation**

- Direct feature implementation
- Bug fixes and minor changes
- Code refactoring tasks

### Complex Feature Development

**Orchestrator → Architect → Task Master → Code → Task Master → Documentation**

- Multi-component features requiring planning
- System integrations and architectural changes
- Major functionality additions

### Bug Investigation & Resolution

**Orchestrator → Debug → Code → Documentation**

- Systematic issue diagnosis
- Root cause analysis and fixes
- Problem resolution documentation

### Research & Planning Projects

**Orchestrator → Ask → Architect → Task Master → Documentation**

- Technology evaluation and selection
- System design and planning phases
- Knowledge gathering for future implementation

### Maintenance & Optimization

**Orchestrator → Code → Debug → Documentation**

- Performance optimization tasks
- Code quality improvements
- System maintenance work

### Documentation-Focused Work

**Orchestrator → Ask → Documentation**

- API documentation creation
- User guide development
- Knowledge base updates

## Workflow Decision Matrix

| Task Type   | Complexity | From tasks.md? | Recommended Workflow                             |
| ----------- | ---------- | -------------- | ------------------------------------------------ |
| Bug Fix     | Simple     | No             | Code → Documentation                             |
| Bug Fix     | Complex    | No             | Debug → Code → Documentation                     |
| Bug Fix     | Any        | Yes            | Task Master → Code → Task Master → Documentation |
| Feature     | Simple     | No             | Code → Documentation                             |
| Feature     | Complex    | No             | Architect → Task Master → Code → Documentation   |
| Feature     | Any        | Yes            | Task Master → Code → Task Master → Documentation |
| Research    | Any        | No             | Ask → Documentation                              |
| Planning    | Any        | No             | Ask → Architect → Task Master (if requested)     |
| Maintenance | Any        | No             | Code → Debug → Documentation                     |

## Best Practices

- **Always assess task complexity** before choosing workflow path
- **Check if task originates from [`tasks.md`](tasks.md)** or requested by user to determine if Task Master mode is needed
- **Consider documentation impact** - complex features need more comprehensive docs
- **Use decision matrix** when workflow choice is unclear
- **Maintain mode context** - pass relevant information when switching modes
- **Document workflow choices** to help future decision-making
