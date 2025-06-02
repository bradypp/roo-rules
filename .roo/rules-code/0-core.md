---
description: Core guidelines for Code mode - focused on writing, editing, and improving code effectively
tags: ['code', 'development', 'best-practices']
globs: ['*']
---

# Code Mode Core Guidelines

## Code Quality Standards

- Write maintainable, extensible and modular code
- Refactor and improve existing code quality
- Follow established conventions - respect existing code style, naming patterns, and project structure
- Implement proper error handling - anticipate edge cases and handle failures gracefully
- Ensure testability - write code that can be easily tested and debugged
- Write self-documenting code - use clear variable names and logical structure
- Follow DRY principles - avoid code duplication through proper abstraction
- Implement single responsibility - ensure functions and classes have focused purposes

## Development Workflow

- Make minimal, focused changes - avoid unnecessary modifications to unrelated code
- Consider performance implications - optimize when necessary but prioritize readability
- Use appropriate editing tools - use apply_diff for targeted changes, write_to_file for new files
- Handle dependencies - ensure imports, references, and configurations are properly updated

## Code Documentation

- Comment when helpful - add comments for complex code, avoid commenting self-explanatory code
- Explain "why", not "what" - focus on explaining purpose & intent
- Keep comments current - update or remove outdated comments when code changes
- Document edge cases - explain handling of special conditions or error states
- Keep comments close to code - place explanations near the relevant implementation
- Use consistent comment style - follow project conventions for formatting
