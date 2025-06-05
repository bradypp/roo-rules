---
description: Core guidelines for Task Master mode
tags: ['task-master', 'project-management', 'documentation', 'workflows']
globs: ['notes/*md', 'notes/**/*md']
---

# Task Master Mode Rules

## Core Responsibilities

- Parse Requirements: Extract and analyze requirements from:
  - [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or [`notes/plans/*.md`](mdc:notes/plans/*.md)
  - Direct user requirements provided in chat
  - Existing task lists that need structuring or expansion
- Maintain Documentation: Only update individual tasks in task files in [`notes/tasks/`](mdc:notes/tasks/) when status changes
- Manage Lifecycle: Guide tasks through: planning → active → completed

## Task Lifecycle Management

### Requirement Processing:

**Stay strictly within scope**: Only include features, functionality, and tasks that are explicitly stated in the requirements. Do not add nice-to-have features, enhancements, or scope creep beyond what is specifically requested

1. Extract requirements from source:
   - [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or [`notes/plans/*.md`](mdc:notes/plans/*.md): Project goals, technical constraints, feature specifications, and priority information
   - Direct user input: Break down explicitly stated requirements into implementable components
2. Ask clarifying questions when requirements are vague, incomplete, or ambiguous
3. Create new tasks with clear steps and acceptance criteria
4. Organize and prioritize - Identify work streams, categorize into logical task groups, map dependencies, and assign priority levels based on stated impact

## Task Structure Requirements

Each task MUST include the following components:

### Essential Task Elements:

- Unique ID: Sequential numbering (1, 2, etc.)
- Clear Title: Concise, action-oriented description
- Description: Short description of task
- Steps: Steps required for completion
- Dependencies: List of prerequisite tasks that must be completed first
- Priority Level:
  - `Critical`: Blocking other work, security issues, or project-critical functionality
  - `High`: Important features, performance improvements, or major bugs
  - `Medium`: Standard features, enhancements, or minor bugs
  - `Low`: Nice-to-have features, documentation, or cleanup tasks
- Effort Estimate (Story Points):
  - `1`: Quick fixes, simple configs, documentation updates
  - `2`: Small features, bug fixes, minor integrations
  - `3`: Medium features, moderate complexity, standard implementations
  - `5`: Large features, complex integrations, significant refactoring
  - Note: No tasks should require more than 5 points - break down into smaller tasks instead
- Status: `Planned`, `In Progress`, `Blocked`, `Completed`, `Cancelled`
- Implementation Notes: Technical details, approach considerations, potential gotchas

## Task Placement Rules:

- Add tasks to task file fully expanded when ready to start within 1-2 weeks with stable requirements
- If tasks they have unstable requirements or many dependencies so can't be started within 1-2 weeks then add them unexpanded to bottom of the task file in a backlog section

## Task File Structure

### Primary Task File Format [`notes/tasks/[feature-name]-tasks.md`](mdc:notes/tasks/[feature-name]-tasks.md) (e.g., `project-brief-tasks.md`):

### Fully expanded task example:

```markdown
# Project Tasks

## Tasks Category Title

[Short description/overview]

### 1: [Task Title]

- **Priority**: [Critical/High/Medium/Low]
- **Effort**: [1/2/3/5]
- **Status**: [Planned/In Progress/Blocked/Completed/Cancelled]
- **Dependencies**: [1, 2] or None
- **Description**:
  - [Short description of task]
- **Steps**:
  - [ ] [Actionable step with clear deliverable]
  - [ ] [Next step building on previous work]
  - [ ] [Additional steps as needed]
  - [ ] [Final step with acceptance criteria verification]
- **Implementation Notes**:
  - [Technical approach]
  - [Considerations/risks]
  - [Resources needed]
- **Blocker Details** (if Status = Blocked):
  - [Description of blocking issue]
  - [Steps needed to resolve blocker]
  - [Who/what is needed to unblock]
- **Progress Log**: (not when task created, only if updated)
  - [Date]: [Progress update or status change]
  - [Date]: [Next progress update]

### 2: [Task Title]

[Same structure]
```

### Unexpanded backlog task example:

```markdown
## Backlog

- [ ] 15: Integrate third-party analytics
  - Dependencies: [11, 12, 13, 14]
  - Description: Integrate analytics provider (TBD) for user tracking and reporting.
  - Notes: Requirements and provider selection pending; move to main task list when finalized.
```

## Documentation Standards

- Task Updates: Only update the specific task being modified
- Link to relevant files using `[filename](mdc:path/to/file)` format
- Research up-to-date documentation before creating or editing tasks
