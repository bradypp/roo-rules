---
description: Guidelines for using the memory MCP tool to maintain project knowledge across sessions
tags: ['memory', 'mcp', 'project-context']
globs: ['*']
---

# Memory MCP Tool Usage

## Core Principle

The memory MCP tool maintains project knowledge across sessions by tracking only essential project information. Focus exclusively on the current working project and avoid storing observations outside the defined scope.

## Tracked Information Categories

### 1. Project

- Core project requirements and goals
- Project scope and objectives
- Primary use cases and functionality
- Success criteria and constraints

### 2. Progress

- Current development status
- Completed features and components
- Known issues and blockers
- Next planned milestones

### 3. Context

- Current work focus
- Recent significant changes
- Active decisions and considerations
- Important project insights and learnings

### 4. Tasks

- Current task priorities
- Pending work items
- Dependencies between tasks
- Task completion status

### 5. Patterns

- System architecture decisions
- Key technical patterns in use
- Design principles and conventions
- Component relationships and structures

## Memory Operations

### Reading Project Memory

- Use `read_graph` to get complete project knowledge
- Use `search_nodes` with specific queries to find relevant information
- Use `open_nodes` to retrieve specific entities by name

### Creating Project Knowledge

- Use `create_entities` for new project components (project, tasks, patterns, etc.)
- Use `create_relations` to link related project concepts
- Focus on active voice relations (e.g., "depends on", "implements", "contains")

### Updating Project Knowledge

- Use `add_observations` to update existing entities with new information
- Use `delete_observations` to remove outdated information
- Use `delete_entities` only when project components are permanently removed

## Entity Structure Guidelines

### Entity Types

- `project` - Core project definition
- `progress_status` - Current development state
- `active_context` - Current work focus
- `task` - Specific work items
- `pattern` - Technical/design patterns
- `component` - System components
- `decision` - Key project decisions

### Naming Conventions

- Use descriptive, project-specific names
- Include context when necessary (e.g., "auth_state_manager")
- Avoid generic names that could apply to any project

## Workflow Integration

### Session Start

1. **Always** read existing project memory with `read_graph`
2. Search for relevant context based on current task
3. Update active context if work focus has changed

### During Development

- Add observations for significant discoveries or decisions
- Create new entities for new components or patterns
- Update progress status as features are completed

### Session End

- Update memory with project status
- Document any new patterns or decisions
- Clean up outdated observations

## Scope Restrictions

### DO Store

- Project-specific architecture and patterns
- Current development progress and status
- Active tasks and their relationships
- Key project decisions and their rationale
- Component interactions and dependencies

### DO NOT Store

- General programming knowledge
- Tool usage instructions
- Personal preferences unrelated to project
- Temporary debugging information
- External project information

## Example Usage

```typescript
// Creating project brief entity
create_entities({
  entities: [
    {
      name: 'ecommerce_project_brief',
      entityType: 'project_brief',
      observations: [
        'Build modern e-commerce platform with React and Node.js',
        'Support user authentication, product catalog, and payment processing',
        'Target launch: Q2 2024',
      ],
    },
  ],
});

// Linking task to component
create_relations({
  relations: [
    {
      from: 'user_auth_task',
      to: 'auth_system_pattern',
      relationType: 'implements',
    },
  ],
});
```

## Memory Maintenance

- Review and clean up outdated information regularly
- Keep observations current and relevant
- Remove completed tasks that no longer provide value
- Update patterns when implementation changes
- Maintain clear relationships between entities

## Integration with Other Tools

- Use memory context to inform code decisions
- Reference stored patterns when implementing new features
- Update memory after significant code changes
- Query memory before starting new development tasks
