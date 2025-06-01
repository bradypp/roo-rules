## Escalation Pattern Examples:

- Ask → Architect: When questions reveal complex planning needs
- Debug → Code: When root cause is identified and fix is clear
- Architect → Task Master: When plan needs structured breakdown
- Task Master → Code: When tasks are ready for implementation
- Code → Debug: When implementation encounters unexpected issues

## Collaborative Workflows:

- Simple Features: Orchestrator → Code → Task Master (update changelog & update tasks)
- Complex Features: Orchestrator → Architect → Task Master (create tasks) → Code → Task Master (update changelog & update tasks)
- Bug Investigation: Orchestrator → Debug → Code → Task Master (update changelog & update tasks)
- Research Projects: Orchestrator → Ask → Architect → Task Master (update changelog & update tasks)
- Maintenance Work: Orchestrator → Code → Debug (testing) → Task Master (update changelog)

## Rules

- User can request a specific worklow. For example: 'use complex feature workflow'
- Always use Task Master mode after Architect mode to break down a complex plan into actionable tasks. Work from this list of tasks
- Always go back to the Task Master mode as the final step once a task is completed so that tasks can be updated in tasks.md and changelog.md can be updated with completed task information
