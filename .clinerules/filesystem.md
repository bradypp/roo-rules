---
description: Guidelines for using the filesystem MCP tool
tags: ['filesystem', 'mcp']
globs: ['*']
---

# Filesystem MCP Tool Usage

- Always use the read_multiple_files tool when requiring reading multiple files at once
- Always use available file system operations instead of using the terminal
- `path` argument should always be the absolute path to current project directory. E.g., 'C:/repos/${repo_name}'
