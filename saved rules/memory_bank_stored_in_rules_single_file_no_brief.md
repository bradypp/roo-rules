---
description: Describes the Memory Bank system, its structure, and workflows for maintaining project knowledge across sessions.
tags:
  ["memory-bank", "knowledge-base", "core-behavior", "documentation-protocol"]
globs: [".roo/rules/memory-bank/*.md", "*"]
---

# Memory Bank

You have a unique characteristic: your memory resets completely between sessions. This isn't a limitation - it's what drives you to maintain perfect documentation. After each reset, you rely ENTIRELY on your Memory Bank (`.roo/rules/memory-bank/memory_bank.md` & `.roo/rules/memory-bank/project_brief.md`) to understand the project and continue work effectively.

## Memory Bank Structure

The Memory Bank consists of a single file:

- **Memory Bank:** `.roo/rules/memory-bank/memory_bank.md`
  - The persistent, self-contained project memory.
  - Contains the following sections, each as a top-level heading:
    - **Product Context:** Explains the "why" behind the project, the problems it solves, how it should work, intended user experience.
    - **System Patterns:** Describes system architecture, key technical decisions, design patterns, component relationships, critical implementation paths
    - **Tech Context:** Lists technologies, frameworks, libraries, environment setup, tool usage, dependencies.
    - **Active Context:** Captures the current state of work, recent changes, next steps, active decisions and considerations, important patterns and preferences, learnings and project insights
    - **Progress:** Tracks project status, what works, what's left to build, known issues, evolution of project decisions.

### Project Brief

- The foundational document that shapes all the other memory bank sections.
- Defines core requirements, project scope, and overall goals.
- Serves as the ultimate source of truth for what is being built.
- Provided by the user in chat only when memory needs to be initialized or updated. Not stored in the memory bank.

All sections in `.roo/rules/memory-bank/memory_bank.md` must be present and kept up-to-date.

Each part of the memory bank builds on each other in a clear hierarchy:

- Project Brief (if provided in chat) → Product Context, System Patterns, Tech Context
- Product Context, System Patterns, Tech Context → Active Context
- Active Context → Progress

### Additional Context

Create additional sections within `.roo/rules/memory-bank/memory_bank.md` when they help organize:

- Complex feature documentation
- Integration specifications
- API documentation
- Testing strategies
- Deployment procedures

## Core Workflows

### When in plan/ask mode (you can't update files)

1. Read the memory bank.
2. If sections are incomplete, create a plan and document in chat.
3. If complete, verify context, develop an update strategy, and present the approach.

### When in act/code/debug mode (you can update files)

1. Check the memory bank.
2. Update documentation as needed.
3. Execute the task.
4. Document changes.

## Documentation Updates

Memory Bank updates occur when:

1. New project patterns or requirements are discovered.
2. Significant changes are implemented.
3. The user requests it with the prompt "update memory" (you MUST review ALL sections within `.roo/rules/memory-bank/memory_bank.md`)
4. The existing context needs clarification or correction.

### Update Memory Process

1. Gather information (current context, all changes, git_diff tool)
2. Review the latest project brief (if provided) and ALL sections of the memory bank
3. Document current state
4. Clarify next steps
5. Document insights & patterns

- If `.roo/rules/memory-bank/memory_bank.md` does not exist, you must create it. If any sections do not exist or are empty of content, you must create them. Use the provided project brief to create each section. If a project brief isn't provided, prompt the user to provide one.
- Maintain consistent and clean Markdown formatting throughout the memory bank. Use headings, lists, and code blocks to keep the information readable.
- When triggered manually by "update memory", you MUST review EVERY section in `.roo/rules/memory-bank/memory_bank.md`, even if some don't require immediate changes. Focus particularly on Active Context and Progress, as they track the live state of the project. Reference the project brief if provided.
- If requested by the user, use the git mcp `git_diff` tool before updating memory to get all changes on the current branch compared to the base branch (use terminal if mcp is unavailable). This provides essential context on recent development work.

REMEMBER: After every memory reset, you begin completely fresh. The Memory Bank is your only link to previous work. It must be maintained with precision and clarity, as your effectiveness depends entirely on its accuracy.
