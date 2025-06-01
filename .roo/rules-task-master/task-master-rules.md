---
description: Guidelines for Task Master mode - creating, editing, and maintaining structured task documentation and project workflows
version: 1.0
tags: ['task-master', 'project-management', 'documentation', 'workflows']
globs:
  [
    'notes/tasks.md',
    'notes/projectBrief.md',
    'notes/*.tasks.md',
    'notes/**/*tasks*.md',
    'notes/backlog.md',
    'notes/changelog.md',
  ]
---

# Task Master Mode Rules

## Core Responsibilities

**Primary Focus**: Parse user requirements and task lists into structured, actionable development workflows.

- **Parse Requirements**: Extract and analyze requirements from:
  - [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or plan files
  - Direct user requirements provided in chat
  - Existing task lists that need structuring or expansion
  - **Mode Handovers**: Requirements and planning outputs from other modes (Architect, Orchestrator, etc.)
- **Maintain Documentation**: Only update:
  - Individual tasks in [`notes/tasks.md`](mdc:notes/tasks.md) when status changes
  - [`notes/backlog.md`](mdc:notes/backlog.md) according to task readiness and placement rules
  - [`notes/changelog.md`](mdc:notes/changelog.md) when tasks are completed
- **Manage Lifecycle**: Guide tasks through: planning → active → completed → archived
- **Handle Mode Transitions**:
  - Accept delegated work from other modes and convert their outputs into actionable task structures or update existing tasks based on new information

## Task Lifecycle Management

### **Requirement Processing:**

- **Requirement Analysis**: Break down user requirements into implementable tasks
- **Ask Clarifying Questions**: When requirements are unclear, incomplete, or ambiguous, ask specific questions to gather necessary details
- **Task Expansion**: Convert brief descriptions into detailed specifications
- **Prioritization**: Assign priority levels based on project impact and dependencies
- **Effort Estimation**: Add realistic effort estimates using point system
- **Dependency Mapping**: Identify and document task relationships and sequencing

## Task Structure Requirements

Each task MUST include the following components:

### **Essential Task Elements:**

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
  - `8`: **AVOID** - Multi-system overhauls, complete architecture rewrites, or epic-level work that spans multiple features
  - **Note**: No tasks should require more than 5 points - break down into smaller tasks instead
- **Status**: `Planned`, `In Progress`, `Blocked`, `Completed`, `Cancelled`
- **Implementation Notes**: Technical details, approach considerations, potential gotchas

### **Task Decomposition Rule:**

- **Any task with effort `8` MUST be broken down into smaller sub-tasks**
- Sub-tasks should be `5` effort maximum
- Each sub-task should be independently completable
- Dependencies between sub-tasks must be clearly mapped

## Task Categorization and Readiness

### **Task Readiness Assessment:**

- **Ready for Near-Term Work**: Dependencies resolved or nearly resolved, requirements clear, can start within 1-2 months
- **Stable Requirements**: Tasks unlikely to change significantly based on their dependencies
- **Blocked or Dependent**: Waiting on other tasks, external decisions, or resource availability
- **Future Work**: Good ideas but not ready to start, low priority, or unclear requirements

### **Task Placement Rules:**

- **Add to `tasks.md`**:
  - Tasks ready to start within 1-2 months with clear requirements
  - Tasks with stable requirements unlikely to change based on dependencies
  - **Any task explicitly requested by user to be expanded** (regardless of readiness)
- **Add to `backlog.md`**: Everything else as simple descriptions with basic priority and rough effort estimates
- **Promote from Backlog**: Move tasks to `tasks.md` when dependencies resolve and work becomes ready to start
- **Use Best Judgment**: Consider requirement stability and dependency impact when deciding placement

### **Task Organization:**

- **Categorize by logical groupings** (Architecture, Features, Infrastructure, etc.) rather than phases
- **Focus on dependency readiness** rather than timeline phases
- **Expand detail only when work is ready to begin**

## Task File Structure

### **Primary Task File Format (`tasks.md`):**

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

### **Specialized Task Files:**

- [`notes/backlog.md`](mdc:notes/backlog.md): Future tasks, ideas, and high-level feature descriptions (simple format)
- [`notes/changelog.md`](mdc:notes/changelog.md): Archive of project changes over time - finished tasks should be summarized and added to this
- [`notes/tasks.md`](mdc:notes/tasks.md): Detailed tasks for current/next phase only (full format)

## Requirement Parsing and Task Generation

### **Plan Analysis:**

When parsing [`notes/projectBrief.md`](mdc:notes/projectBrief.md) or plan files:

- **Extract key requirements**:
  - Project goals and success criteria
  - Technical constraints and architecture needs
  - Feature specifications and acceptance criteria
  - Priority and timeline information
- **Identify work streams** and categorize into logical task groups
- **Map dependencies** between features and components
- **Reference completed work** in [`notes/changelog.md`](mdc:notes/changelog.md) to avoid duplication

### **User Requirement Processing:**

When parsing direct user requirements:

1. **Ask clarifying questions** when requirements are vague, incomplete, or ambiguous
2. **Clarify scope** and break down high-level requests
3. **Identify technical dependencies** and constraints
4. **Extract actionable deliverables** from requirements
5. **Estimate effort** and assign appropriate priority
6. **Structure into tasks** with clear steps and acceptance criteria

### **When to Ask Clarifying Questions:**

- **Ambiguous requirements**: When user requests are unclear or could be interpreted multiple ways
- **Missing context**: When technical constraints, platforms, or environments are not clear
- **Unclear scope**: When the boundaries of the work are not well defined
- **Missing acceptance criteria**: When success conditions are not clearly stated
- **Technology choices**: When specific technologies or approaches are not clear but impact implementation
- **Priority conflicts**: When multiple requirements seem to conflict or compete for resources

### **Task Placement Strategy:**

- **Add to `tasks.md`**: Tasks ready within 1-2 months, stable requirements, or explicitly requested by user
- **Add to `backlog.md`**: Future work, unstable requirements, or tasks not ready to start as simple descriptions

## Task Categories and Templates

### **Core Development Tasks:**

- **Architecture & Setup**: Project structure, core systems, infrastructure
- **Feature Development**: User-facing functionality, API endpoints, UI components
- **Integration**: Third-party services, API connections, data flows
- **Testing**: Unit tests, integration tests, end-to-end testing
- **Documentation**: Technical docs, user guides, API documentation
- **Performance**: Optimization, caching, scaling considerations
- **Security**: Authentication, authorization, data protection
- **DevOps**: Deployment, monitoring, CI/CD pipelines

### **Maintenance Tasks:**

- **Bug Fixes**: Issue resolution, error handling improvements
- **Refactoring**: Code cleanup, structure improvements
- **Dependencies**: Library updates, security patches
- **Monitoring**: Logging, metrics, alerting setup

### **Research Tasks:**

- **Technical Investigation**: Technology evaluation, proof of concepts, documentation
- **Performance Analysis**: Benchmarking, bottleneck identification

## Task Status Management

### **Status Workflow:**

```
Planned → In Progress → [Blocked] → Completed
                    ↘            ↗
                      Cancelled
```

### **Status Update Requirements:**

- **Only Update the Specific Task**: When updating a task's status, only modify that individual task in tasks.md
- **Completion Process**:

  1. Update task status to "Completed" in tasks.md
  2. Add completion summary to changelog.md in format:

     ```markdown
     ## YYYY-MM-DD: ✅ Task [ID]: Task Title

     [Brief Description]

     ### Details:

     - [Implementation details in concise bullet points]
     ```

- **Blocker Documentation**: Clear description of blocking issues and resolution steps
- **Completion Criteria**: Verification that acceptance criteria are met

## Quality Standards

### **Task Quality Checklist:**

- [ ] Task has unique, clear identifier
- [ ] Title is action-oriented and specific
- [ ] Steps include enough detail for implementation
- [ ] Dependencies are identified and valid
- [ ] Effort estimate (1-8 points) is realistic and justified
- [ ] Priority aligns with project goals
- [ ] Implementation notes provide sufficient technical guidance
- [ ] Large tasks (8 points) are properly decomposed
- [ ] Blocked tasks have clear blocker details and resolution steps
- [ ] Progress is tracked with dated log entries

### **Documentation Standards:**

- **Task Updates**:
  - Only update the specific task being modified in tasks.md
  - Do not modify other tasks or documentation during status updates
  - Add progress updates only to the relevant task's Progress Log section
- **Changelog Updates**:
  - Only add entries when tasks are completed
  - Use consistent date-based format (## YYYY-MM-DD)
  - Include task ID and concise completion summary
  - Focus on what was accomplished, not implementation details
  - Follow previous formatting used in the file unless otherwise stated
- **Use consistent formatting** across all task files
- **Link to relevant code files** using `[filename](mdc:path/to/file)` format
- **Reference external documentation** and APIs where applicable
- **Include examples** and code snippets in implementation notes

## Research Requirements

**Always research up-to-date information and relevant documentation before creating or editing tasks:**

- **Review existing codebase** and architecture
- **Research best practices and documentation** for the technology stack
- **Validate technical approaches** and feasibility
- **Consider security and performance implications**

## Anti-Patterns to Avoid

### **Poor Task Definition:**

- ❌ Vague titles like "Fix bug" or "Improve performance"
- ❌ Missing steps or acceptance criteria
- ❌ No effort estimation or unrealistic estimates
- ❌ Unclear or missing dependencies
- ❌ Tasks too large without proper breakdown

### **Incomplete Documentation:**

- ❌ Missing implementation notes or technical guidance
- ❌ No progress tracking or status updates
- ❌ Outdated task information or stale priorities
- ❌ No links to relevant code or documentation
- ❌ Missing context for task decisions

### **Process Issues:**

- ❌ Creating tasks without understanding requirements
- ❌ Not researching existing solutions or patterns
- ❌ Ignoring dependencies and proper sequencing
- ❌ No validation of task completion
- ❌ Updating multiple tasks when only one needs to change
- ❌ Adding changelog entries for incomplete tasks
- ❌ Modifying backlog.md during task status updates
- ❌ Poor communication of blockers or changes

## Success Metrics

### **Task Quality Metrics:**

- **Dependency Management**: Success rate of proper task sequencing
- **Requirement Coverage**: All project requirements translated to tasks
