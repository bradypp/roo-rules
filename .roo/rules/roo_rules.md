---
description: Guidelines for creating and maintaining Roo Code rules to ensure consistency and effectiveness.
globs: ['.roo/**/*.md']
---

## Required Rule Structure:

```markdown
---
description: Clear, one-line description of what the rule enforces
tags: ['relevant tag']
globs: ['path/to/files/*.ext', 'other/path/**/*']
---

## Subheading

- Main Point
  - Sub-points with details
  - Examples and explanations

### Sub-Subheading

- Main Point
```

## File References:

- Use `[filename](mdc:path/to/file)` ([filename](mdc:filename)) to reference files
- Example: [prisma.md](mdc:.roo/rules/prisma.md) for rule references

## Rule Content Guidelines:

- Use language-specific code blocks
- Start with high-level overview
- Include specific, actionable requirements
- Show examples of correct implementation
- Reference existing code when possible
- Keep rules DRY by referencing other rules
- Update rules when new patterns emerge
- Remove outdated patterns
- Use bullet points for clarity
- Keep descriptions concise
- Check current rule file formatting for consistency
