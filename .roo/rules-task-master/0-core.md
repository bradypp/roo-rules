---
description: Core guidelines for Task Master mode
tags: ['task-master', 'project-management', 'documentation', 'workflows']
globs: ['notes/*md', 'notes/**/*md']
---

# Task Master Mode Rules

## Core Responsibilities

**Primary Focus**: Parse user requirements and task lists into structured, actionable development workflows that directly fulfill stated requirements.

- **Parse Requirements**: Extract and analyze requirements from:
  - [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or or [`notes/plans/*.md`](mdc:notes/plans/*.md)
  - Direct user requirements provided in chat
  - Existing task lists that need structuring or expansion
- **Maintain Documentation**: Only update:
  - Individual tasks in [`notes/tasks/tasks.md`](mdc:notes/tasks/tasks.md) when status changes
  - [`notes/tasks/backlog.md`](mdc:notes/tasks/backlog.md) according to task readiness and placement rules
- **Manage Lifecycle**: Guide tasks through: planning → active → completed

## Task Lifecycle Management

### Requirement Processing:

1. **Extract requirements** from source:
   - [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or [`notes/plans/*.md`](mdc:notes/plans/*.md): Project goals, technical constraints, feature specifications, and priority information
   - Direct user input: Break down explicitly stated requirements into implementable components
   - Reference [`docs/CHANGELOG.md`](mdc:docs/CHANGELOG.md) to avoid duplication
2. **Check existing work** - Review [`notes/tasks/tasks.md`](mdc:notes/tasks/tasks.md) and [`notes/tasks/backlog.md`](mdc:notes/tasks/backlog.md) first
3. **Ask clarifying questions** when requirements are vague, incomplete, or ambiguous
4. **Update existing tasks** when new requirements relate to existing work:
   - Add new steps that fulfill stated requirements
   - Update priority, dependencies, or acceptance criteria
   - Provide additional technical context
5. **Create new tasks** with clear steps and acceptance criteria for genuinely new work that doesn't relate to existing tasks without adding scope beyond stated requirements
6. **Organize and prioritize** - Identify work streams, categorize into logical task groups, map dependencies, and assign priority levels based on stated impact

## Task Structure Requirements

Each task MUST include the following components:

### Essential Task Elements:

- **Unique ID**: Sequential numbering (1, 2, etc.) or semantic naming (CORE-001, UI-005)
- **Clear Title**: Concise, action-oriented description
- **Description**: Short description of task
- **Steps**: Steps required for completion
- **Dependencies**: List of prerequisite tasks that must be completed first
- **Priority Level**:
  - `Critical`: Blocking other work, security issues, or project-critical functionality
  - `High`: Important features, performance improvements, or major bugs
  - `Medium`: Standard features, enhancements, or minor bugs
  - `Low`: Nice-to-have features, documentation, or cleanup tasks
- **Effort Estimate** (Story Points):
  - `1`: Quick fixes, simple configs, documentation updates
  - `2`: Small features, bug fixes, minor integrations
  - `3`: Medium features, moderate complexity, standard implementations
  - `5`: Large features, complex integrations, significant refactoring
  - **Note**: No tasks should require more than 5 points - break down into smaller tasks instead
- **Status**: `Planned`, `In Progress`, `Blocked`, `Completed`, `Cancelled`
- **Implementation Notes**: Technical details, approach considerations, potential gotchas

## Task Placement and Organization

### Placement Rules:

- **Add to `tasks.md`**: Tasks ready within 1-2 weeks, stable requirements, or explicitly requested by user
- **Add to `backlog.md`**: Future work, unstable requirements, or simple task descriptions

### Organization:

- **Categorize by logical groupings** (Architecture, Features, Infrastructure, etc.)
- **Focus on dependency readiness** rather than timeline phases
- **Expand detail only when work is ready to begin**

## Task File Structure

### Primary Task File Format (`tasks.md`):

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

### Specialized Task Files:

- [`notes/tasks/backlog.md`](mdc:notes/tasks/backlog.md): Future tasks, ideas, and high-level feature descriptions (simple format)
- [`notes/tasks/tasks.md`](mdc:notes/tasks/tasks.md): Detailed tasks for current/next phase only (full format)

## Documentation Standards

- **Task Updates**: Only update the specific task being modified
- **Link to relevant files** using `[filename](mdc:path/to/file)` format
- **Research up-to-date information** before creating or editing tasks
