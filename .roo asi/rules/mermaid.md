---
description: Guidelines for creating consistent and visually appealing Mermaid diagrams
tags: ['documentation', 'diagrams', 'mermaid']
globs: ['*.md']
---

# Mermaid Diagram Styling

## Visual Style Guidelines

- Use a dark color palette for backgrounds
- Apply consistent styling across all diagram nodes
- Use bold white text and borders for all nodes
- Use rounded corners for a modern appearance
- Use background colors that make sense for node purpose (red = fail, green = success)

## Example Diagram

```mermaid
graph TD
    A[Example] --> B[Node];
    style A fill:#2A892A,stroke:#FFF,stroke-width:2px,color:#FFF,font-weight:bold,rx:5
    style B fill:#262692,stroke:#FFF,stroke-width:2px,color:#FFF,font-weight:bold,rx:5
```

## Example Color Palette

- Success Green: #2A892A
- Purple: #8714D4
- Dark Blue: #262692
- Bright Orange: #DB4A15
- Deep Red: #CA1717
