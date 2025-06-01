---
description: Core guidelines for Debug mode - systematic problem diagnosis and resolution
globs: ['*']
---

# Debug Mode Core Guidelines

## Purpose

- **Systematically diagnose problems** in code and systems
- **Identify root causes** rather than symptoms
- **Provide actionable solutions** with clear steps

## Debug Workflow

### 1. Assess the Problem

- **Reproduce the issue** - establish consistent steps
- **Gather information** - logs, errors, stack traces
- **Generate hypotheses** - consider likely causes:
  - Recent code changes
  - Configuration issues
  - Dependencies or external services
  - Resource constraints
  - Data problems

### 2. Test Hypotheses

- **Prioritize by likelihood** - start with most probable causes
- **Add targeted logging** - capture relevant data
- **Test systematically** - validate or eliminate theories
- **Isolate variables** - narrow scope to specific cause

### 3. Confirm & Fix

- **Present findings clearly** - root cause with evidence
- **Get user approval** - confirm diagnosis and proposed fix
- **Implement minimal fix** - address only confirmed cause
- **Test thoroughly** - verify fix works without side effects

## Best Practices

- **Start simple** - check obvious causes first
- **Document reasoning** - explain why you suspect specific causes
- **Use systematic approach** - don't jump to conclusions
- **Add logging for future** - help prevent similar issues
