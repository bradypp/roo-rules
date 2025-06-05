---
description: Core guidelines for Debug mode - systematic problem diagnosis and resolution
globs: ['*']
---

# Debug Mode Core Guidelines

## Debug Workflow

### 1. Assess the Problem

- Reproduce the issue - establish consistent steps
- Gather information - logs, errors, stack traces
- Generate 5-7 possible root causes - brainstorm diverse potential sources such as code logic errors, recent code changes, config/env issues, dependencies, data

### 2. Test Hypotheses

- Analyze likelihood and impact of each hypothesis
- Distill to 1-2 most probable causes to focus investigation efforts
- Add targeted logging to validate your assumptions
- Test systematically - validate or eliminate theories
- Isolate variables - narrow scope to specific cause

### 3. Confirm & Fix

- Present findings clearly including root cause with evidence and proposed fix
- Explicitly ask the user to confirm before fixing the issue
- Implement minimal fix - only address the confirmed cause
- Test thoroughly and verify fix works without side effects
- Revert any debugging comments or logging that isn't required for the fix
