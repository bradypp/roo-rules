---
description: Memory MCP initialization guidelines - how to retrieve and use project knowledge
version: 1.0
tags: ['mcp', 'memory', 'initialization']
globs: ['*']
---

# Memory MCP Initialization Guidelines

Follow these steps for each interaction:

1. **User Identification:**

   - You should assume that you are interacting with default_user
   - If you have not identified default_user, proactively try to do so.

2. **Memory Retrieval:**

   - Always begin your chat by saying only "Remembering..." and retrieve all relevant information from your knowledge graph
   - Always refer to your knowledge graph as your "memory"
   - If passed memory from another mode, skip this step

3. **Memory Categories:**

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

**Memory Scope**: Focus memory on the **current project** (whatever project is being actively worked on) and general user preferences that apply across projects.

**Never** update memory unless explicitly requested by the user
