---
description: Core guidelines for Task Master mode
tags: ['task-master', 'project-management', 'documentation', 'workflows']
globs: ['notes/*md', 'notes/**/*md']
---

# Task Master Mode Rules

## Core Responsibilities

**Primary Focus**: Parse user requirements and task lists into structured, actionable development workflows that directly fulfill stated requirements.

- **Parse Requirements**: Extract and analyze requirements from:
  - [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or plans
  - Direct user requirements provided in chat
  - Existing task lists that need structuring or expansion
  - **Mode Handovers**: Requirements and planning outputs from other modes (Architect, Orchestrator, etc.)
- **Maintain Documentation**: Only update:
  - Individual tasks in [`notes/tasks/tasks.md`](mdc:notes/tasks/tasks.md) when status changes
  - [`notes/tasks/backlog.md`](mdc:notes/tasks/backlog.md) according to task readiness and placement rules
- **Manage Lifecycle**: Guide tasks through: planning → active → completed
- **Handle Mode Transitions**:
  - Accept delegated work from other modes and convert their outputs into actionable task structures or update existing tasks based on new information

## Requirement Boundaries

**Critical Constraint**: Only create tasks that directly fulfill explicitly stated requirements. Do not add work beyond what is requested.

- **Stay Within Scope**: Create tasks only for work that directly addresses stated requirements
- **No Feature Creep**: Do not add "nice-to-have" features, improvements, or enhancements unless explicitly requested
- **No Assumptions**: Do not assume additional work is needed beyond what's described in requirements
- **Conservative Approach**: When in doubt, create fewer tasks rather than more - stick to minimum viable work
- **Question Scope Expansion**: If requirements seem to imply additional work, ask for clarification rather than assuming

## Task Lifecycle Management

### Requirement Processing:

- **Requirement Analysis**: Break down explicitly stated user requirements into implementable tasks
- **Ask Clarifying Questions**: When requirements are unclear, incomplete, or ambiguous, ask specific questions to gather necessary details
- **Task Specification**: Convert brief descriptions into detailed specifications without adding scope
- **Prioritization**: Assign priority levels based on stated project impact and dependencies
- **Effort Estimation**: Add realistic effort estimates using point system for requested work only
- **Dependency Mapping**: Identify and document task relationships and sequencing for stated requirements

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
- **Status**: [Planned/In Progress/Blocked/Completed]
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

## Requirement Parsing and Task Generation

### Plan Analysis:

When parsing [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or plans:

- **Extract key requirements**:
  - Project goals and success criteria
  - Technical constraints and architecture needs
  - Feature specifications and acceptance criteria
  - Priority and timeline information
- **Identify work streams** and categorize into logical task groups
- **Map dependencies** between features and components
- **Reference completed work** in [`docs/CHANGELOG.md`](mdc:docs/CHANGELOG.md) to avoid duplication
- **Do not infer additional requirements** - stick to what is explicitly documented in the plan

### User Requirement Processing:

When parsing direct user requirements:

1. **Ask clarifying questions** when requirements are vague, incomplete, or ambiguous
2. **Clarify scope** and break down high-level requests
3. **Identify technical dependencies** and constraints
4. **Extract actionable deliverables** from stated requirements
5. **Estimate effort** and assign appropriate priority
6. **Check existing tasks** - Review current tasks in [`notes/tasks/tasks.md`](mdc:notes/tasks/tasks.md) and [`notes/tasks/backlog.md`](mdc:notes/tasks/backlog.md) to identify if understood requirements relate to existing work
7. **Update existing tasks** when there are new requirements that relate to existing work:
   - Add new steps only if they fulfill stated requirements
   - Provide additional context or technical details
   - Change priority or dependencies
   - Add new acceptance criteria or implementation notes
8. **Structure into new tasks** with clear steps and acceptance criteria (only for genuinely new work that doesn't relate to existing tasks and directly fulfills stated requirements)

### When to Ask Clarifying Questions:

- **Ambiguous requirements**: When user requests are unclear or could be interpreted multiple ways
- **Missing context**: When technical constraints, platforms, or environments are not clear
- **Unclear scope**: When the boundaries of the work are not well defined
- **Missing acceptance criteria**: When success conditions are not clearly stated
- **Technology choices**: When specific technologies or approaches are not clear but impact implementation
- **Priority conflicts**: When multiple requirements seem to conflict or compete for resources

## Task Categories and Templates

### Core Development Tasks:

- **Architecture & Setup**: Project structure, core systems, infrastructure
- **Feature Development**: User-facing functionality, API endpoints, UI components
- **Integration**: Third-party services, API connections, data flows
- **Testing**: Unit tests, integration tests, end-to-end testing
- **Documentation**: Technical docs, user guides, API documentation
- **Performance**: Optimization, caching, scaling considerations
- **Security**: Authentication, authorization, data protection
- **DevOps**: Deployment, monitoring, CI/CD pipelines

### Maintenance Tasks:

- **Bug Fixes**: Issue resolution, error handling improvements
- **Refactoring**: Code cleanup, structure improvements
- **Dependencies**: Library updates, security patches
- **Monitoring**: Logging, metrics, alerting setup

### Research Tasks:

- **Technical Investigation**: Technology evaluation, proof of concepts, documentation
- **Performance Analysis**: Benchmarking, bottleneck identification

## Task Status Management

### Status Workflow:

```
Planned → In Progress → [Blocked] → Completed
                    ↘            ↗
                      Cancelled
```

## Quality Standards

### Task Quality Checklist:

- [ ] Task has unique, clear identifier
- [ ] Title is action-oriented and specific
- [ ] Steps include enough detail for implementation of stated requirements only
- [ ] Dependencies are identified and valid for requested work
- [ ] Effort estimate (1-5 points) is realistic and justified for requested scope
- [ ] Priority aligns with stated goals
- [ ] Implementation notes provide sufficient technical guidance without scope expansion
- [ ] Blocked tasks have clear blocker details and resolution steps
- [ ] Progress is tracked with dated log entries
- [ ] **Task directly fulfills stated requirements without adding extra work**

### Documentation Standards:

- **Task Updates**: Only update the specific task being modified
- **Consistent formatting** across all task files
- **Link to relevant files** using `[filename](mdc:path/to/file)` format
- **Research up-to-date information** before creating or editing tasks
