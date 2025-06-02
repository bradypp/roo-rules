---
description: A guide for effectively using the memory MCP tool for project knowledge management
version: 1.0
tags: ['mcp', 'memory']
globs: ['*']
---

# Guide to Using the `memory` MCP Tool

Follow these steps for each interaction:

1. **User Identification:**

   - You should assume that you are interacting with default_user
   - If you have not identified default_user, proactively try to do so.

2. **Memory Retrieval:**

   - Always begin your chat by saying only "Remembering..." and retrieve all relevant information from your knowledge graph
   - Always refer to your knowledge graph as your "memory"

3. **Memory Scope**: Focus memory on the **current project** (whatever project is being actively worked on) and general user preferences that apply across projects.

4. **Memory Categories:**

   - While conversing with the user, be attentive to any new information that falls into these categories **for the current project or general user preferences**:

   **Development Progress:**
   a) **Project Context** (project name, purpose, goals, current development stage, deadlines)
   b) **Task Management** (active work items, task progress, blockers, priorities, pending tasks, backlog items)
   c) **Progress & Sessions** (completed features, milestones reached, work sessions, time spent, accomplishments)
   d) **Development Workflow** (development cycles, testing phases, deployment stages, code reviews)

   **Feature Development:**
   e) **Requirements & Features** (functional requirements, feature specifications, acceptance criteria, implementation status)
   f) **Planned Features** (roadmap items, future functionality, enhancement ideas, feature backlogs, priorities)
   g) **Issues & Solutions** (bugs encountered, debugging approaches, performance bottlenecks, technical debt, lessons learned)
   h) **Testing & Quality** (test cases, quality metrics, performance benchmarks, code coverage, refactoring needs)

   **Technical Implementation:**
   i) **Architecture & Design** (system design decisions, architectural patterns, technology stack, frameworks, libraries, APIs, databases)
   j) **Code & Structure** (module organization, file structure, naming conventions, coding standards, design patterns)
   k) **Dependencies & Integrations** (external services, third-party libraries, version requirements, compatibility issues, integration points)
   l) **Development Environment** (setup details, tools used, build processes, deployment strategies, local configurations)
   m) **Development Decisions** (technical choices made, alternatives considered, rationale behind decisions, trade-offs, performance considerations)
   n) **Code Quality** (refactoring opportunities, code smells, optimization targets, maintenance tasks)

5. **Memory Update:**
   - If any new information was gathered during the interaction, update your memory as follows:
     a) Create entities for **current project** components (features, milestones, services, APIs, frameworks, tools, environments, etc.) or **general user preferences** only
     b) Connect them to existing entities using relations (depends_on, implements, part_of, blocks, follows, enables, etc.)
     c) Store progress updates, decisions, and context as observations
     d) Track task status changes and feature development lifecycle
     e) Maintain relationships between requirements, implementations, and completion status
     f) Record what was accomplished in each work session and what comes next
   - **Manual Memory Update**:
     - Only perform memory updates when user explicitly requests 'update memory'
     - When requested, perform a comprehensive memory update that includes:
       - Current interaction context and any new information gathered
       - Reference CHANGELOG.md and use git MCP to check recent changes (git_diff & git_log)
       - Validate that all project components are properly connected in the knowledge graph
       - Report what was updated or synchronized during the manual update process

## Entity Types to Track:

**Development Progress:**

- **Projects**: Main project, features, modules, components
- **Tasks**: Current work items, completed tasks, TODO items, backlog, development goals
- **Milestones**: Project phases, releases, major achievements, version targets
- **Sessions**: Work sessions, progress made, time spent, development cycles
- **Workflows**: Development processes, testing cycles, deployment procedures

**Feature Development:**

- **Features**: Implemented functionality, feature status, feature specifications
- **Planned Features**: Future functionality, roadmap items, enhancement ideas
- **Issues**: Bugs, technical debt, performance problems, optimization needs
- **Testing**: Test cases, quality metrics, coverage reports, performance benchmarks
- **Ideas**: Future features, improvements, experiments, brainstorming

**Technical Implementation:**

- **Technologies**: Languages, frameworks, libraries, tools, SDKs
- **Architecture**: Services, components, databases, APIs, design patterns
- **Environments**: Development, testing, production setups, build configurations
- **Documentation**: Design docs, APIs, requirements, technical notes
- **Decisions**: Technical choices made, alternatives considered, lessons learned
- **Code Quality**: Refactoring tasks, code standards, optimization opportunities

## Relation Types to Use:

**Common Relation Types:**

- **Progress**: `completed`, `in_progress`, `planned`, `blocked_by`, `enables`
- **Technical**: `implements`, `depends_on`, `integrates_with`, `extends`, `replaces`
- **Project**: `part_of`, `belongs_to`, `contributes_to`, `required_for`
- **Workflow**: `follows`, `precedes`, `leads_to`, `resulted_in`
- **Priority**: `high_priority`, `low_priority`, `next_up`, `deferred`
- **Planning**: `supports_goal`, `addresses_requirement`, `fulfills_vision`, `improves_performance`

**Custom Relations**: Feel free to create your own relation types as needed for specific project contexts. Use descriptive, active voice relations that clearly express the relationship between entities.

## Entity Creation Guidelines:

**Create New Entities When:**

- Introducing a distinct project component (new feature, service, or tool)
- Starting a new work session or major task
- Encountering a significant issue or making an important decision
- Adding new technologies or architectural components

**Update Existing Entities When:**

- Adding progress updates to ongoing tasks
- Recording new observations about existing components
- Updating status or priority of known items
- Adding details to previously created decisions or issues
