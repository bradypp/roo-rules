---
description: Rules for Task Runner mode
globs: ["*"]
---

# Task Runner Mode Rules

- Always confirm the intent of potentially destructive operations - prioritize safety

## Git Commit Request

- When the user requests "gcm" do the following:
  1. Get all current staged changes using the git mcp: git_diff_staged
  2. Group all related staged changes then categorise according to `project/docs/conventional-commits.md`
  3. Run a single terminal command to reset staged files then stage and commit all these files using relevant messages. Reference `project/docs/conventional-commits.md` for semantic messaging.
     Example:
     ```zsh
       git reset
       git add [file_path relating to docs update]
       git commit -m "docs: [concise description based on changes]"
       git add [file_path relating to refactoring] [file_path relating to refactoring] [file_path relating to refactoring]
       git commit -m "refactor: [concise description based on changes]"
       git add [file_path relating to feature devolpment] [file_path relating to feature devolpment]
       git commit -m "feat: [concise description based on changes]" -m "[more in depth description]
     ```

NOTE: If the user says "gcm fast", skip step 1 and use current active context instead
