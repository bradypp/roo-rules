---
description: 'A detailed workflow for using the sequentialthinking MCP tool to solve complex problems including code logic, debugging errors, algorithmic challenges, and intricate technical issues.'
author: 'Cline Team'
version: '1.0'
tags:
  [
    'sequential thinking',
    'problem solving',
    'mcp tool',
    'code logic',
    'debugging',
    'algorithms',
    'complex analysis',
  ]
globs: ['*.*']
---

Use the `sequentialthinking` MCP tool for complex problem-solving tasks that require systematic analysis, logical reasoning, and iterative refinement across various technical challenges.

<detailed_sequence_of_steps>

# Sequential Thinking Problem-Solving Process - Detailed Sequence of Steps

## 1. Assess Problem Complexity

1. Determine if the problem requires sequential thinking by checking for:

   - Complex algorithmic logic requiring step-by-step analysis
   - Multi-layered technical issues with interdependent components
   - Error patterns with multiple potential root causes
   - Performance optimization requiring systematic investigation
   - Code refactoring with broad impact considerations
   - Integration challenges across multiple systems
   - Logic design requiring careful consideration of edge cases
   - Technical decisions with multiple trade-offs to evaluate

2. If the problem has an obvious solution or is straightforward, do NOT use sequential thinking - proceed with direct implementation.

## 2. Define and Scope the Problem

1. Start with clear problem definition:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Problem definition: [Clearly articulate what needs to be solved, the current state vs. desired state, constraints, and success criteria]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 1,
     "totalThoughts": 7
   }
   </arguments>
   </use_mcp_tool>
   ```

## 3. Analyze Context and Constraints

1. Examine the broader context and limitations:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Context analysis: [Identify relevant code sections, system architecture, performance requirements, existing patterns, dependencies, and any technical or business constraints]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 2,
     "totalThoughts": 7
   }
   </arguments>
   </use_mcp_tool>
   ```

## 4. Break Down the Problem

1. Decompose into manageable components:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Problem decomposition: [Break the complex problem into smaller, interconnected sub-problems. Identify which parts are most critical or risky to address first]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 3,
     "totalThoughts": 7
   }
   </arguments>
   </use_mcp_tool>
   ```

## 5. Generate Solution Approaches

1. Develop multiple potential approaches:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Solution generation: [Brainstorm 2-3 different approaches to solving the problem. Consider different algorithms, architectural patterns, or implementation strategies with their trade-offs]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 4,
     "totalThoughts": 7
   }
   </arguments>
   </use_mcp_tool>
   ```

## 6. Evaluate and Select Approach

1. Analyze approaches systematically:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Approach evaluation: [Compare the different approaches against criteria like complexity, performance, maintainability, and risk. Select the most promising approach and explain the reasoning]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 5,
     "totalThoughts": 7
   }
   </arguments>
   </use_mcp_tool>
   ```

## 7. Design Implementation Strategy

1. Plan the implementation details:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Implementation strategy: [Define specific steps, identify potential pitfalls, plan for testing and validation, and consider rollback strategies if needed]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 6,
     "totalThoughts": 7
   }
   </arguments>
   </use_mcp_tool>
   ```

## 8. Validate and Refine Solution

1. Consider edge cases and validation:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Solution validation: [Review the complete solution for edge cases, error conditions, performance implications, and integration points. Confirm it addresses the original problem requirements]",
     "nextThoughtNeeded": false,
     "thoughtNumber": 7,
     "totalThoughts": 7
   }
   </arguments>
   </use_mcp_tool>
   ```

## 9. Handle Course Corrections

1. When initial approach proves insufficient:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Approach revision: [Explain what new information or complications have emerged, and how this changes the problem understanding or solution approach]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 8,
     "totalThoughts": 10,
     "isRevision": true,
     "revisesThought": 5,
     "needsMoreThoughts": true
   }
   </arguments>
   </use_mcp_tool>
   ```

## 10. Explore Alternative Solutions

1. When pursuing different technical approaches:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Alternative exploration: [Investigate a fundamentally different approach - perhaps using different algorithms, design patterns, or technologies]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 9,
     "totalThoughts": 10,
     "branchFromThought": 4,
     "branchId": "alternative-algorithm"
   }
   </arguments>
   </use_mcp_tool>
   ```

</detailed_sequence_of_steps>

<example_problem_solving_process>

# Example Sequential Thinking Problem-Solving Process

Let's walk through a real example: "Optimize a slow data processing pipeline that handles millions of records daily, causing user-facing timeouts."

## Step 1: Assess Problem Complexity

This problem involves:

- Performance optimization across multiple system layers
- Large-scale data processing considerations
- User experience impact analysis
- Multiple potential bottlenecks (database, algorithms, infrastructure)
- Trade-offs between speed, accuracy, and resource usage

This qualifies for sequential thinking approach.

## Step 2: Define and Scope the Problem

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Problem definition: Current data processing pipeline takes 45 minutes to process daily batch of 2M records, causing 30-second user-facing timeouts. Target: reduce to under 15 minutes while maintaining data accuracy and system stability.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 1,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

## Step 3: Analyze Context and Constraints

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Context analysis: Pipeline includes data validation, transformation, aggregation, and database updates. Current architecture: single-threaded Python script, PostgreSQL database, 4GB RAM limit. Constraints: must maintain data integrity, budget limitations for infrastructure upgrades.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 2,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

## Step 4: Break Down the Problem

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Problem decomposition: 1) Data loading and parsing (5 min), 2) Validation logic (15 min), 3) Business rule processing (20 min), 4) Database operations (5 min). The validation and business rule processing are the main bottlenecks.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 3,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

## Step 5: Generate Solution Approaches

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Solution generation: Approach 1) Parallel processing with multiprocessing to utilize multiple CPU cores. Approach 2) Algorithmic optimization by caching repeated calculations and using more efficient data structures. Approach 3) Database optimization with batch operations and indexing.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 4,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

## Step 6: Evaluate and Select Approach

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Approach evaluation: Parallel processing offers biggest impact (potential 4x speedup on 4-core system) with manageable complexity. Algorithmic optimization is lower risk but limited impact. Database optimization is important but secondary. Combining parallel processing with algorithmic improvements is the best strategy.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 5,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

## Step 7: Design Implementation Strategy

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Implementation strategy: 1) Refactor validation logic into pure functions for parallel execution, 2) Implement multiprocessing.Pool with chunk-based processing, 3) Add progress tracking and error handling, 4) Create fallback to single-threaded mode if needed, 5) Implement comprehensive testing with production data samples.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 6,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

## Step 8: Validate and Refine Solution

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Solution validation: The parallel processing approach addresses the main bottleneck and should achieve 3-4x speedup. Edge cases include memory constraints with large chunks and error propagation from worker processes. Solution includes monitoring, graceful degradation, and maintains data integrity requirements.",
  "nextThoughtNeeded": false,
  "thoughtNumber": 7,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

</example_problem_solving_process>

<problem_categories_reference>

# Common Problem Categories for Sequential Thinking

## Algorithmic Challenges

### Complex Logic Design

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Algorithm analysis: [Break down the algorithmic requirements, identify key operations, consider time/space complexity, and evaluate different approaches]",
  "nextThoughtNeeded": true,
  "thoughtNumber": 3,
  "totalThoughts": 8
}
</arguments>
</use_mcp_tool>
```

### Performance Optimization

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Performance bottleneck identification: [Profile the current implementation, identify hotspots, analyze resource usage patterns, and consider optimization strategies]",
  "nextThoughtNeeded": true,
  "thoughtNumber": 4,
  "totalThoughts": 8
}
</arguments>
</use_mcp_tool>
```

## System Design Problems

### Architecture Decisions

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Architecture evaluation: [Compare different architectural patterns, consider scalability requirements, evaluate technology trade-offs, and assess long-term maintainability]",
  "nextThoughtNeeded": true,
  "thoughtNumber": 5,
  "totalThoughts": 8
}
</arguments>
</use_mcp_tool>
```

### Integration Challenges

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Integration analysis: [Map data flows between systems, identify potential failure points, consider API compatibility, and plan error handling strategies]",
  "nextThoughtNeeded": true,
  "thoughtNumber": 6,
  "totalThoughts": 8
}
</arguments>
</use_mcp_tool>
```

## Code Quality Issues

### Refactoring Complex Code

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Refactoring strategy: [Analyze current code structure, identify improvement opportunities, plan incremental changes, and ensure backward compatibility]",
  "nextThoughtNeeded": true,
  "thoughtNumber": 7,
  "totalThoughts": 8
}
</arguments>
</use_mcp_tool>
```

### Debugging Complex Issues

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Root cause analysis: [Trace through the problem systematically, test hypotheses about potential causes, and isolate the source of the issue]",
  "nextThoughtNeeded": true,
  "thoughtNumber": 8,
  "totalThoughts": 8
}
</arguments>
</use_mcp_tool>
```

</problem_categories_reference>

<best_practices>

# Best Practices for Sequential Problem-Solving

## When to Use Sequential Thinking

✅ **DO use for:**

- Complex algorithmic design and optimization
- Multi-component system integration
- Performance problems requiring systematic analysis
- Code refactoring with broad impact
- Technical architecture decisions
- Debugging intricate, multi-layered issues
- Logic design with many edge cases
- Problems requiring multiple solution approaches

❌ **DON'T use for:**

- Simple bug fixes or syntax errors
- Straightforward feature implementations
- Well-documented configuration issues
- Basic CRUD operations
- Standard library usage questions

## Problem-Solving Principles

- **Define clearly**: Ensure the problem is well-understood before solving
- **Think in layers**: Separate concerns (UI, logic, data, infrastructure)
- **Consider trade-offs**: Evaluate performance vs. complexity vs. maintainability
- **Start simple**: Begin with the simplest solution that could work
- **Plan for failure**: Consider error cases and edge conditions
- **Validate assumptions**: Test that foundational assumptions are correct

## Solution Development Guidelines

- **Iterative refinement**: Build solutions incrementally and test frequently
- **Document reasoning**: Capture why certain approaches were chosen or rejected
- **Consider alternatives**: Don't commit to the first solution that seems viable
- **Think about maintenance**: Consider how the solution will be maintained over time
- **Plan for scale**: Consider how the solution will perform under different loads

## Completion Criteria

Only complete the problem-solving process when:

- Root cause or core challenge is clearly identified
- Solution approach is technically sound and feasible
- Implementation plan is detailed and realistic
- Edge cases and error conditions are considered
- Solution aligns with broader system requirements
- Approach has been validated against success criteria

</best_practices>
