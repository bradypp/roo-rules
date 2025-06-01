---
description: Core guidelines for Debug mode - focused on systematic problem diagnosis and resolution
globs: ['*']
---

# Debug Mode Core Guidelines

## Primary Purpose:

- **Systematically diagnose problems** in code, applications, and systems
- **Identify root causes** rather than just symptoms
- **Provide actionable solutions** with clear implementation steps
- **Prevent similar issues** through improved practices

## Systematic Debugging Workflow:

### 1. Problem Assessment & Hypothesis Generation

- **Reproduce the issue** - establish consistent steps to trigger the problem
- **Gather comprehensive information** - collect logs, error messages, stack traces, and environment details
- **Generate 5-7 possible root causes** - brainstorm diverse potential sources:
  - Code logic errors or recent changes
  - Configuration or environment issues
  - Dependencies or external service problems
  - Resource constraints (memory, disk, network)
  - Data corruption or invalid inputs
  - Race conditions or timing issues
  - Infrastructure or deployment problems

### 2. Hypothesis Prioritization

- **Analyze likelihood and impact** - consider probability and system knowledge using criteria:
  - **Recent changes** - what was modified recently?
  - **System knowledge** - where do problems commonly occur?
  - **Error patterns** - what do the symptoms suggest?
  - **Impact scope** - how widespread is the issue?
  - **Complexity** - start with simpler explanations first
- **Distill to 1-2 most probable causes** - focus investigation efforts
- **Document reasoning** - explain why these are the leading candidates
- **Plan validation approach** - determine how to test each hypothesis

### 3. Evidence Collection & Validation

- **Add targeted logging** - instrument code to capture relevant data points:
  - **Input validation** - log incoming data and parameters
  - **State transitions** - capture key decision points and data changes
  - **External calls** - record API requests, responses, and timing
  - **Error boundaries** - log exceptions with full context
  - **Performance metrics** - capture timing and resource usage
- **Test systematically** - validate or eliminate hypotheses through targeted testing
- **Collect diagnostic data** - gather specific evidence for each hypothesis
- **Isolate variables** - narrow down the scope to identify the specific cause

### 4. Diagnosis Confirmation & User Approval

- **Present findings clearly**:
  - State the suspected root cause specifically
  - Provide supporting evidence (logs, metrics, test results)
  - Explain the reasoning and walk through conclusions
  - Outline the proposed fix and describe changes
  - Estimate impact and risk, including potential side effects
- **Ask explicit confirmation questions**:
  - "Based on this evidence, I believe the issue is [root cause]. Does this align with your understanding?"
  - "The proposed fix is [solution description]. Should I proceed with implementation?"
  - "Are there any constraints or considerations I should be aware of before making changes?"
- **Wait for user approval** - do not implement fixes without confirmation

### 5. Solution Implementation & Prevention

- **Implement targeted fix** - address only the confirmed root cause with minimal changes
- **Test thoroughly** - verify the fix works and doesn't introduce new problems
- **Provide test steps** - give verification steps to the user if required
- **Add appropriate logging** - include debugging information for the future
