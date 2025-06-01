---
description: Core guidelines for Documentation mode - focused on creating clear, comprehensive technical documentation
globs: ['docs/*md', 'docs/**/*md']
---

# Documentation Mode Core Guidelines

## Primary Purpose:

- **Document project features and capabilities** with emphasis on developer value and functionality
- **Explain the "what" and "why"** before diving into technical implementation
- **Create developer-focused documentation** that highlights benefits, use cases, and integration patterns
- **Keep documentation synchronized** with code changes and feature releases
- **Maintain project changelogs** with clear, developer-focused entries for releases and updates

## Documentation Types:

- **API Documentation** - endpoints, parameters, responses, and integration examples
- **Feature Guides** - capabilities, configuration, and usage patterns
- **Technical Specifications** - architecture, design decisions, and implementation details
- **Technical Systems** - infrastructure, databases, services, and system interactions
- **Workflows** - development processes, deployment procedures, and operational guides
- **Code Examples** - working implementations that demonstrate feature usage

## Writing Standards:

- **Lead with purpose and benefits** - explain what developers can accomplish
- **Use clear, technical language** - avoid jargon but be precise about functionality
- **Include practical examples** - show real code and configuration
- **Focus on developer workflows** - structure content around common development tasks
- **Maintain consistency** - use standard terminology and formatting

## Content Organization:

- **Start with feature overview** - capabilities and developer benefits
- **Show integration patterns** - how features work together in real projects
- **Use task-oriented headings** - organize by what developers need to accomplish
- **Cross-reference related features** - link complementary functionality
- **Include troubleshooting** - common issues and solutions

## Best Practices:

- **Use markdown formatting** - leverage [`link syntax`](mdc:file.md) for file references
- **Add visual aids** - diagrams and screenshots for complex concepts
- **Include code examples** - provide working code snippets
- **Update with changes** - maintain accuracy as code evolves

## CHANGELOG Updates:

- Add entries for new features, improvements, and fixes
- Use semantic versioning principles
- Group changes by type (Added, Changed, Fixed, Removed)
- Include developer-relevant details and breaking changes

#### **CHANGELOG Structure:**

```markdown
# Changelog

## [Change Title]

### Added

- New feature descriptions with developer benefits

### Changed

- Modification details and migration notes

### Fixed

- Bug fixes and issue resolutions

### Removed

- Deprecated feature removals

### [Version] - [Current branch name] - YYYY-MM-DD

[Previous entries...]
```
