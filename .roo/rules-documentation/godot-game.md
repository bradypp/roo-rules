---
description: Guidelines for documenting Godot game projects with focus on gameplay features, mechanics, and player experience
tags: ['godot', 'game-development', 'documentation']
globs: ['docs/game/**/*.md']
---

# Godot Game Documentation Guidelines

## Game Documentation Focus:

- **Document gameplay and core mechanics** that define the player experience
- **Explain game systems and interactions** from a player perspective
- **Focus on player capabilities** rather than code implementation
- **Use gameplay terminology** instead of technical details

## Game-Specific Documentation Areas:

### Gameplay Systems

- **Core mechanics** - fundamental gameplay rules and systems
- **Player progression** - advancement, unlocks, and achievement systems
- **Game modes** - different play styles and their unique features
- **Victory/failure conditions** - objectives and win/lose states

### Player Experience

- **Controls and interactions** - how players interact with the game
- **UI and interface** - menus, HUD elements, and navigation
- **Game flow** - level progression and scene transitions
- **Settings and customization** - player configuration options

### Technical Game Systems

- **Scene organization** - major scenes and their purposes
- **Asset structure** - how game resources are organized
- **Performance factors** - elements that affect game performance

## Game Documentation Template:

```markdown
## [Game Feature/System Name]

**Purpose**: [What this adds to the player experience]

### Player Experience

- [What players can do with this feature]
- [How it affects gameplay and strategy]

### Game Mechanics

- [Rules and behaviors from player perspective]
- [Interactions with other game systems]

### Technical Notes (when relevant)

- [Key scenes or systems involved]
- [Performance or platform considerations]
```

## Godot-Specific Debugging:

### **Game Issues**

- **Gameplay problems** - player experience issues and common complaints
- **Performance issues** - frame rate drops, loading problems, memory usage
- **Platform differences** - mobile vs desktop vs web platform issues
- **Build problems** - export settings and deployment issues

### **Godot Debug Tools**

- **In-game debugging** - using Godot's built-in debugging during gameplay
- **Scene inspection** - understanding scene hierarchy and node behavior
- **Performance profiling** - monitoring frame rate and resource usage
- **Signal debugging** - tracking game events and their triggers

## Godot Game Documentation Specifics:

- **Scene purposes** - what each major scene accomplishes in the game
- **Signal patterns** - important game events and communication between systems
- **Resource organization** - how sprites, sounds, and other assets are managed
- **Export settings** - platform-specific build requirements and optimizations
- **Version compatibility** - document only when major Godot version changes affect gameplay
