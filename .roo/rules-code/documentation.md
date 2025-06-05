---
description: Guidelines for writing code documentation
tags: ['code', 'development', 'documentation', 'best-practices']
globs: ['*']
---

# Code Documentation

- Comment when helpful - add comments for complex code, avoid commenting self-explanatory code
- Explain "why", not "what" - focus on explaining purpose & intent
- Keep comments current - update or remove outdated comments when code changes
- Only leave TODO comments when requested by the user. TODO comment format: `TODO: [description]`
- Document edge cases - explain handling of special conditions or error states
- Keep comments close to code - place explanations near the relevant implementation
- Use consistent comment style - follow project conventions for formatting
- Don't include specific values in comments - these are iterative and can change quickly
- Avoid referencing future code that doesn't exist yet in comments - focus on current implementation

## File Documentation

- Comment at the top of the file explaining it's purpose. Example format:

```
 [Title]
 Purpose: [Concise description]
 Key features:
 - [Describe key features in concise bullet points]
 Notes:
 - [Describe any extra useful details in concise bullet points]

[Rest of the script]
```
