---
description: Guidelines for updating memory when explicitly requested
tags: ['memory', 'update', 'knowledge-graph']
globs: ['*']
---

## Memory Update Process

When the 'update memory' command is received:

1. **Context Analysis**

   - Extract relevant project changes from current conversation
   - Only save project-related information reflected in actual project state

2. **Project State**

   - Check git changes and history using git MCP (git_diff & git_log)
   - Review file changes, added features, documentation and new components
   - Reference CHANGELOG.md if available

3. **Knowledge Graph**

   - Validate entity connections and relationships
   - Ensure graph matches current project reality
   - Remove outdated or invalid entries

4. **Memory Sync**
   - Update project, tasks, and milestone status
   - Record architectural changes and and design decisions
   - Track new technologies and solutions

## Success Criteria

- Accurate project state representation
- Valid knowledge graph connections
- Recent changes documented
- Reality matches memory state
