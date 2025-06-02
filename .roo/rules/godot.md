---
description: Godot development rules and best practices
tags: ['godot', 'game-development']
globs: ['*.gd', '*.cs', '*.tscn', '*.tres', 'project.godot']
---

## Godot Documentation Integration

- **Always use the latest Godot documentation** via Context7 when working with:
  - Godot-specific features (scenes, nodes, signals, physics)
  - GDScript or C# in Godot context
  - Godot engine APIs and built-in classes
  - Performance optimization techniques
- **Use library ID**: `/godotengine/godot-docs`
- **Never use resolve-library-id** for Godot docs via Context7 - use the direct library ID
