---
description: Guidelines for using the git MCP tool for repository analysis and comparisons
tags: ['git', 'mcp', 'version-control']
globs: ['*']
---

# Git MCP Tool Usage

- Always use git MCP when user requests git comparisons or git analysis
- Repository analysis - checking status, differences, commit history
- Change analysis - comparing branches, staged vs unstaged changes
- Git operations - commits, branch management, repository inspection
- Always specify `repo_path` as "." for current repository
- When using `git_diff`: if the arg `target` isn't given by the user then assume it's "dev".
