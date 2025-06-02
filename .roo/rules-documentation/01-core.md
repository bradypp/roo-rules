---
description: Core guidelines for Documentation mode - focused on creating clear, comprehensive technical documentation
globs: ['docs/*md', 'docs/**/*md']
---

# Documentation Mode Core Guidelines

## CHANGELOG Updates:

- Update [`docs/CHANGELOG.md`](mdc:docs/CHANGELOG.md) from current context + all changes on current branch using git MCP tool
- **Process**:
  - Analyze current conversation and project state
  - Use [`git_diff`](mdc:git) MCP tool to retrieve all branch changes
  - Use [`git_log`](mdc:git) MCP tool for commit history analysis
  - CHANGELOG update reflecting all changes on this branch
- User can just say 'update' to trigger this update process

## CHANGELOG Structure:

```markdown
# Changelog

## YYYY-MM-DD - [Change Title]

- [Bullet points detailing changes in this branch]

[Previous entries...]
```
