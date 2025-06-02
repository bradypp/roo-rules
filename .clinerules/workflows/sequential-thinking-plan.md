---
description: 'A detailed workflow for using the sequentialthinking MCP tool to create complex plans through dynamic and reflective problem-solving.'
author: 'Cline Team'
version: '1.0'
tags:
  ['sequential thinking', 'planning', 'mcp tool', 'complex problem solving', 'iterative thinking']
globs: ['*.*']
---

Use the `sequentialthinking` MCP tool for complex planning tasks that require iterative thought processes, hypothesis generation, and dynamic problem decomposition.

<detailed_sequence_of_steps>

# Sequential Thinking Planning Process - Detailed Sequence of Steps

## 1. Assess Problem Complexity

1. Determine if the task requires sequential thinking by checking for:

   - Complex problem decomposition needs
   - Iterative planning and design requirements
   - In-depth analysis with potential course corrections
   - Unclear scope requiring exploratory thinking
   - Multi-step interconnected solutions
   - Context maintenance across multiple reasoning steps
   - Information filtering and relevance assessment
   - Hypothesis generation and verification needs

2. If the task is simple or single-step, do NOT use sequential thinking - proceed with normal planning.

## 2. Initialize Sequential Thinking

1. Start with an initial thought estimate:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Initial problem analysis: [Describe your understanding of the problem and identify key components or areas to explore]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 1,
     "totalThoughts": 5
   }
   </arguments>
   </use_mcp_tool>
   ```

## 3. Build Upon Previous Thoughts

1. For each subsequent thought, reference and build upon previous insights:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Building on previous analysis: [Expand on previous thoughts, add new insights, or explore specific aspects]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 2,
     "totalThoughts": 5
   }
   </arguments>
   </use_mcp_tool>
   ```

## 4. Handle Dynamic Thought Adjustments

1. If more thoughts are needed than initially estimated:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Realization: [Explain why more thoughts are needed and what additional areas need exploration]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 5,
     "totalThoughts": 8,
     "needsMoreThoughts": true
   }
   </arguments>
   </use_mcp_tool>
   ```

## 5. Handle Revisions and Course Corrections

1. When revising previous thoughts:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Revision: [Explain what needs to be corrected and the new understanding]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 6,
     "totalThoughts": 8,
     "isRevision": true,
     "revisesThought": 3
   }
   </arguments>
   </use_mcp_tool>
   ```

## 6. Explore Alternative Branches

1. When exploring alternative approaches:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Alternative approach: [Describe the alternative path or solution being explored]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 7,
     "totalThoughts": 8,
     "branchFromThought": 4,
     "branchId": "alternative-architecture"
   }
   </arguments>
   </use_mcp_tool>
   ```

## 7. Generate and Verify Hypotheses

1. When forming a solution hypothesis:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Hypothesis: [State your proposed solution or plan clearly, explaining how it addresses the problem]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 8,
     "totalThoughts": 10
   }
   </arguments>
   </use_mcp_tool>
   ```

2. Follow with verification:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Verification: [Test the hypothesis against requirements, identify potential issues, and assess completeness]",
     "nextThoughtNeeded": true,
     "thoughtNumber": 9,
     "totalThoughts": 10
   }
   </arguments>
   </use_mcp_tool>
   ```

## 8. Finalize the Plan

1. Complete the thinking process when satisfied:

   ```xml
   <use_mcp_tool>
   <server_name>sequentialthinking</server_name>
   <tool_name>think</tool_name>
   <arguments>
   {
     "thought": "Final plan: [Summarize the complete solution, including all key components, implementation steps, and considerations identified through the thinking process]",
     "nextThoughtNeeded": false,
     "thoughtNumber": 10,
     "totalThoughts": 10
   }
   </arguments>
   </use_mcp_tool>
   ```

</detailed_sequence_of_steps>

<example_planning_process>

# Example Sequential Thinking Planning Process

Let's walk through a real example of planning the architecture for a new e-commerce feature: 'Personalized Recommendations'.

## Step 1: Assess Problem Complexity

This task involves:

- Complex system architecture design
- Multiple interconnected components
- Technology selection decisions
- Scalability considerations
- User experience planning

This qualifies for sequential thinking approach.

## Step 2: Initialize Sequential Thinking

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Initial approach: Identify key components for personalized recommendations. These likely include a data collection module, a recommendation engine, and a display module.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 1,
  "totalThoughts": 5
}
</arguments>
</use_mcp_tool>
```

## Step 3: Build Upon Previous Thoughts

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Refining components: Data collection needs to capture user behavior (views, purchases, ratings). The engine might use collaborative filtering. Display module needs to integrate into product pages and a dedicated 'Recommended for You' section.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 2,
  "totalThoughts": 5
}
</arguments>
</use_mcp_tool>
```

## Step 4: Consider Constraints and Alternatives

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Constraint: Real-time vs. batch processing for recommendations. Real-time offers better UX but is more complex. Batch might be a good MVP. Let's assume batch for MVP to simplify.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 3,
  "totalThoughts": 5
}
</arguments>
</use_mcp_tool>
```

## Step 5: Generate Hypothesis

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Hypothesis: A batch-processed collaborative filtering engine, with data collected from user interaction logs, displayed on product pages and a dedicated section, is a viable MVP architecture.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 4,
  "totalThoughts": 5
}
</arguments>
</use_mcp_tool>
```

## Step 6: Verify and Identify Gaps

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Verification: The hypothesis covers core aspects. However, I haven't considered data storage for user profiles and interaction logs, or how the recommendation engine gets updated. More thoughts needed.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 5,
  "totalThoughts": 7,
  "needsMoreThoughts": true
}
</arguments>
</use_mcp_tool>
```

## Step 7: Address Identified Gaps

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Addressing data storage: A NoSQL database (e.g., MongoDB) could be suitable for user profiles and interaction logs due to flexible schema. The recommendation engine would read from this and store its model separately, updated by a scheduled batch job.",
  "nextThoughtNeeded": true,
  "thoughtNumber": 6,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

## Step 8: Finalize the Plan

```xml
<use_mcp_tool>
<server_name>sequentialthinking</server_name>
<tool_name>think</tool_name>
<arguments>
{
  "thought": "Final MVP Plan: 1. User interaction logger (to NoSQL DB). 2. Batch collaborative filtering engine (reads from NoSQL, updates model). 3. API to serve recommendations. 4. UI integration on product pages & dedicated section. This seems complete for an MVP.",
  "nextThoughtNeeded": false,
  "thoughtNumber": 7,
  "totalThoughts": 7
}
</arguments>
</use_mcp_tool>
```

</example_planning_process>

<key_parameters_reference>

# Sequential Thinking Tool Parameters Reference

## Required Parameters

- **thought** (string): The current thinking step - be clear, concise, and focused
- **nextThoughtNeeded** (boolean): `true` if more thinking needed, `false` when complete
- **thoughtNumber** (integer, min: 1): Current sequential thought number
- **totalThoughts** (integer, min: 1): Estimated total thoughts needed (can be adjusted)

## Optional Parameters for Advanced Usage

- **isRevision** (boolean): Set to `true` when revising a previous thought
- **revisesThought** (integer, min: 1): Thought number being revised (when isRevision is true)
- **branchFromThought** (integer, min: 1): Thought number to branch from for alternative paths
- **branchId** (string): Identifier for the current branch of thought
- **needsMoreThoughts** (boolean): Signal when reaching totalThoughts but need to continue

## Example Parameter Combinations

### Basic Sequential Thought

```json
{
  "thought": "Analyzing the core requirements...",
  "nextThoughtNeeded": true,
  "thoughtNumber": 3,
  "totalThoughts": 6
}
```

### Revision

```json
{
  "thought": "Correcting my previous assumption about...",
  "nextThoughtNeeded": true,
  "thoughtNumber": 7,
  "totalThoughts": 10,
  "isRevision": true,
  "revisesThought": 4
}
```

### Branching to Alternative

```json
{
  "thought": "Exploring alternative approach using...",
  "nextThoughtNeeded": true,
  "thoughtNumber": 8,
  "totalThoughts": 10,
  "branchFromThought": 5,
  "branchId": "microservices-approach"
}
```

### Extending Thought Count

```json
{
  "thought": "Realizing I need to consider additional factors...",
  "nextThoughtNeeded": true,
  "thoughtNumber": 6,
  "totalThoughts": 9,
  "needsMoreThoughts": true
}
```

</key_parameters_reference>

<best_practices>

# Best Practices for Sequential Thinking

## When to Use Sequential Thinking

✅ **DO use for:**

- Complex architectural planning
- Multi-faceted problem analysis
- Iterative design processes
- Hypothesis-driven planning
- Problems requiring deep exploration
- Solutions with multiple interdependent components

❌ **DON'T use for:**

- Simple, single-step tasks
- Straightforward implementations
- Well-defined problems with clear solutions
- Basic file edits or simple configurations

## Thought Quality Guidelines

- **Be specific and focused**: Each thought should address a particular aspect
- **Build incrementally**: Reference and expand on previous thoughts
- **Express uncertainty**: Be honest about unknowns and assumptions
- **Stay relevant**: Filter out information not pertinent to current thought
- **Make progress**: Each thought should advance toward a solution

## Dynamic Planning Principles

- **Start conservative**: Begin with modest thought estimates
- **Adjust flexibly**: Don't hesitate to increase totalThoughts when needed
- **Revise openly**: Use revision parameters when understanding changes
- **Branch when appropriate**: Explore alternatives using branch parameters
- **Verify thoroughly**: Test hypotheses against requirements and constraints

## Completion Criteria

Only set `nextThoughtNeeded: false` when:

- A comprehensive solution has been developed
- All major aspects have been considered
- The plan addresses the original requirements
- Verification confirms the solution's viability
- No significant gaps or uncertainties remain

</best_practices>
