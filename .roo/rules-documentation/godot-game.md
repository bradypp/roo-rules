---
description: Guidelines for documenting Godot game projects with focus on gameplay features, mechanics, and player experience
tags: ['godot', 'game-development', 'documentation']
globs: ['docs/game/**/*.md']
---

# Godot Game Documentation Guidelines

## Primary Focus:

- **Document overall gameplay and core mechanics** that define the game experience
- **Explain game systems and how they interact** at a high level
- **Focus on features and player capabilities** rather than detailed implementation
- **Include debugging and troubleshooting information** for common issues

## Documentation Areas:

### **Gameplay Overview**

- **Core mechanics** - fundamental gameplay systems and rules
- **Player progression** - how players advance and unlock content
- **Game modes** - different ways to play and their unique features
- **Victory/failure conditions** - what players are trying to achieve

### **Feature Documentation**

- **Major game features** - key systems that make the game unique
- **Player interactions** - controls, UI, and interaction methods
- **Game flow** - how levels, scenes, and gameplay states connect
- **Settings and options** - customization available to players

### **Technical Overview**

- **Scene organization** - high-level structure of game scenes
- **Key systems** - important scripts and their purposes
- **Asset organization** - how game assets are structured
- **Performance considerations** - factors that affect game performance

## Writing Approach:

### **High-Level Focus**

- **Describe what the system does** rather than how it's implemented
- **Use gameplay terms** instead of technical code details
- **Focus on player experience** and game feel
- **Keep implementation details minimal** and only when necessary

### **Maintenance-Friendly**

- **Avoid specific file paths** that might change frequently
- **Document system purposes** rather than exact implementations
- **Use general categories** instead of detailed breakdowns
- **Focus on stable, core concepts**

## Documentation Template:

```markdown
## [Game Feature/System Name]

**Purpose**: [What this system adds to the game]

### What It Does

- [Primary function from player perspective]
- [Secondary features and capabilities]
- [How it enhances gameplay]

### Key Mechanics

- [Important rules and behaviors]
- [Interactions with other systems]
- [Player strategies and tactics]

### Technical Notes

- [Brief implementation overview]
- [Important scenes or scripts involved]
- [Performance or platform considerations]
```

## Debugging Documentation:

### **Common Issues**

- **Gameplay problems** - typical player experience issues
- **Performance issues** - frame rate, loading, memory problems
- **Platform-specific issues** - differences between target platforms
- **Build and deployment issues** - common setup and distribution problems

### **Debug Tools and Methods**

- **In-game debugging** - tools for testing during gameplay
- **Development cheats** - shortcuts for testing specific scenarios
- **Performance monitoring** - how to track game performance
- **Log analysis** - understanding error messages and warnings

## Best Practices:

### **Keep It Simple**

- **Focus on player-facing features** rather than internal systems
- **Use clear, non-technical language** when possible
- **Group related concepts** together for easy reference
- **Prioritize information** that helps understand the game

### **Maintenance**

- **Update when major features change** rather than with every small tweak
- **Focus on stable, core systems** that are unlikely to change frequently
- **Document known issues** and their current status
- **Track Godot version compatibility** for major changes only

### **Godot-Specific Notes**

- **Scene purposes** - what each major scene accomplishes
- **Signal usage** - important game events and their triggers
- **Resource management** - how the game handles assets and memory
- **Export considerations** - platform-specific build requirements
