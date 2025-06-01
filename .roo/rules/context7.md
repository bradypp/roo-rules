---
description: Guidelines for effectively using the context7 MCP tool for retrieving up-to-date documentation
globs: ['*']
---

# Context7 MCP Tool Usage

## General Documentation Retrieval

- **Use `resolve-library-id`** first to get the correct Context7-compatible library ID (unless otherwise specified or library id is given)
- **Focus documentation requests** on specific topics when possible to get more relevant results
- **Adjust token limits** based on complexity - use higher token counts for comprehensive API references
- **Before any kind of planning, research or task creation** - always get relevant up-to-date documentation using context7

## Godot Documentation

- **Always access latest Godot documentation** via Context7 when working with:
  - Godot-specific features (scenes, nodes, signals)
  - GDScript or C# in Godot context
  - Godot engine APIs and built-in classes
- **Use library ID**: `/godotengine/godot-docs`
- **Skip resolve-library-id**: Never use `resolve-library-id` for Godot docs - use the direct library ID
