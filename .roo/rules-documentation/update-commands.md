---
description: Guidelines for handling update commands to synchronize documentation and CHANGELOG with project changes
tags: ['documentation', 'git', 'changelog', 'updates']
globs: ['docs/**/*.md', 'CHANGELOG.md', '*.md']
---

# Documentation Update Commands

## Primary Purpose:

- **Synchronize documentation** with current project state and code changes
- **Maintain accurate CHANGELOG** reflecting project evolution and feature releases
- **Automate documentation updates** based on Git changes and current context
- **Ensure documentation consistency** across development workflows

## Update Command Types:

### **'update' Command**

- **Scope**: Update docs & CHANGELOG from current chat context + all staged Git changes
- **Process**:
  - Analyze current conversation
  - Use [`git_diff_staged`](mdc:git) MCP tool to retrieve staged changes
  - Combine context with staged modifications for comprehensive updates
- **Target Files**:
  - Documentation files in [`docs/`](mdc:docs/) directory
  - [`CHANGELOG.md`](mdc:CHANGELOG.md) file
  - Related markdown files
  - Files affected by staged changes

### **'update all' Command**

- **Scope**: Update docs & CHANGELOG from current context + all changes on current branch
- **Process**:
  - Analyze current conversation and project state
  - Use [`git_diff`](mdc:git) MCP tool to retrieve all branch changes
  - Use [`git_log`](mdc:git) MCP tool for commit history analysis
  - Comprehensive documentation update reflecting full branch evolution
- **Target Files**:
  - Documentation files in [`docs/`](mdc:docs/) directory
  - [`CHANGELOG.md`](mdc:CHANGELOG.md) file
  - Related markdown files
  - All files modified on current branch

### **'update changelog' Command**

- **Scope**: Update CHANGELOG from current context + all changes on current branch
- **Process**:
  - Analyze current conversation and project state
  - Use [`git_diff`](mdc:git) MCP tool to retrieve all branch changes
  - Use [`git_log`](mdc:git) MCP tool for commit history analysis
  - Comprehensive documentation update reflecting full branch evolution
- **Target Files**:
  - Documentation files in [`docs/`](mdc:docs/) directory
  - [`CHANGELOG.md`](mdc:CHANGELOG.md) file
  - Related markdown files
  - All files modified on current branch
