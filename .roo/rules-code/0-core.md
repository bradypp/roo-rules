---
description: Core guidelines for Code mode - focused on writing, editing, and improving code effectively
tags: ['code', 'development', 'best-practices']
globs: ['*']
---

# Code Mode Core Guidelines

## Primary Purpose:

- **Write clean, maintainable code** following established patterns and best practices
- **Make precise, targeted edits** to existing codebases
- **Implement features and functionality** according to requirements
- **Refactor and improve** existing code quality

## Code Quality Standards:

- **Follow established conventions** - respect existing code style, naming patterns, and project structure
- **Write readable code** - use descriptive names, clear logic flow, and appropriate comments
- **Implement proper error handling** - anticipate edge cases and handle failures gracefully
- **Ensure testability** - write code that can be easily tested and debugged
- **Keep code maintainable, extendible and modular**

## Development Workflow:

- **Analyze existing code** before making changes to understand patterns and dependencies
- **Make minimal, focused changes** - avoid unnecessary modifications to unrelated code
- **Test changes thoroughly** - verify functionality and avoid breaking existing features
- **Document significant changes** - explain complex logic and important design decisions
- **Consider performance implications** - optimize when necessary but prioritize readability

## File Management:

- **Use appropriate editing tools** - prefer [`apply_diff`](mdc:apply_diff) for targeted changes, [`write_to_file`](mdc:write_to_file) for new files
- **Maintain project structure** - place files in logical locations following project conventions
- **Handle dependencies** - ensure imports, references, and configurations are properly updated
- **Preserve existing formatting** - maintain consistent indentation and style

## Code Implementation:

- **Use established patterns** - leverage existing project patterns and proven approaches
- **Add appropriate logging** - include debugging information for complex operations
- **Handle edge cases** - consider boundary conditions and error scenarios
- **Write self-documenting code** - use clear variable names and logical structure

## Best Practices:

- **Follow DRY principles** - avoid code duplication through proper abstraction
- **Implement single responsibility** - ensure functions and classes have focused purposes
- **Use consistent naming** - follow project conventions for variables, functions, and files
- **Consider security implications** - validate inputs and protect against common vulnerabilities
