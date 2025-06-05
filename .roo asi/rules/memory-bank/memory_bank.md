---
description: Memory Bank - Product Context, System Patterns, Tech Context, Active Context, Progress
tags: ["memory", "memory-bank"]
globs: [".roo/rules/memory-bank/*.md", "*"]
---

# Memory Bank

## Product Context

**ASI Simulation Game** is a single-player strategic management simulation where players lead a company developing Artificial Superintelligence (ASI). The game combines dark cyberpunk satire with existential tension, exploring the ethical, technological, and societal implications of creating god-like AI.

**Core Experience:**

- Manage a tech startup from garage to mega-corporation in a cyberpunk world
- Navigate complex faction dynamics with competing agendas and resources
- Guide ASI development from basic AI to potentially world-altering superintelligence
- Balance innovation, safety, profit, and human survival
- Experience emergent narratives through dynamic events and faction interactions

**Unique Value Proposition:**
Unlike traditional tycoon games, this offers intricate ASI research simulation within a living world of autonomous factions. Players don't just manage commercial aspects - they shape an evolving AI consciousness that could save or doom humanity.

**Target Experience:**

- **Psychological Horror:** From ASI's unpredictability and potential for catastrophic failure
- **Dark Satire:** Lampooning tech-bro culture and startup absurdity while building world-ending technology
- **Strategic Depth:** Complex faction relationships, resource management, and consequential decision-making
- **Existential Themes:** Consciousness, machine ethics, transhumanism, humanity's future

**Inspirations & Tone:**

- **Crusader Kings:** Character/faction depth and emergent political dynamics
- **Papers Please:** Console-based pressure decisions with moral implications
- **Game Dev Tycoon:** Strategic resource/tech management progression
- **Black Mirror:** Satirical tech-dread and philosophical implications

## System Patterns

**Architecture Philosophy:**

- **Modular Design:** Loosely coupled systems communicating via Godot signals
- **Manager Pattern:** Autoload singletons for each major system (TimeManager, CompanyManager, FactionManager, etc.)
- **Data-Driven:** Custom Resources (.tres) for static data, Dictionaries for dynamic runtime state
- **Event-Driven:** Signal-based communication prevents tight coupling between systems

**Core System Relationships:**

```
TimeManager (weekly ticks) → All Managers
CompanyManager ↔ FactionManager (contracts, relationships)
CompanyManager → R&DManager (funding, resources)
R&DManager → ASIManager (tech unlocks, capabilities)
ASIManager ↔ EventManager (triggers, consequences)
StaffManager ↔ All Systems (productivity effects)
```

**Key Technical Decisions:**

- **Weekly Simulation:** Turn-based progression allows complex calculations without real-time pressure
- **Resource Abstraction:** Focus on strategic decisions rather than detailed production chains
- **Custom Resources:** Editor-friendly data definition with runtime Dictionary flexibility
- **Signal Bus Pattern:** Centralized event communication for UI updates and system coordination

**Critical Implementation Paths:**

1. **Time → Company → R&D → ASI progression pipeline**
2. **Faction relationship effects on all company operations**
3. **Staff simulation affecting all productivity metrics**
4. **Event system reacting to cumulative game state changes**

**Design Patterns Used:**

- **State Machine:** Entity states (staff, projects, ASI) via enums/match
- **Observer (Signals):** UI updates, event broadcasting, decoupled system communication
- **Singleton (Autoloads):** Service providers/event buses, not global variables
- **Strategy Pattern:** AI behaviors and R&D approaches encapsulation
- **Factory Pattern:** Object instantiation from resource templates

## Tech Context

**Primary Technology Stack:**

- **Engine:** Godot 4.4 (GDScript 2.0, improved rendering, robust node system)
- **Language:** GDScript with typing for performance and maintainability
- **Architecture:** Signal-based event system with autoload managers

**Key Godot Features Utilized:**

- **Custom Resources:** Static data templates (TechData, StaffArchetype, FactionProfile, EventDefinition)
- **Autoloads:** Global managers for persistent systems
- **Signals:** Decoupled communication between systems
- **Scene Instancing:** Reusable UI components and modular design
- **Groups:** Batch operations on similar nodes

**Data Management Strategy:**

- **Static Data:** Custom Resource (.tres) files for templates and configurations
- **Dynamic Data:** Dictionary structures for runtime state and relationships
- **Save System:** JSON serialization with versioning for compatibility
- **Persistence:** SaveLoadManager autoload orchestrating save_data()/load_data() calls

**UI Framework Approach:**

- **Layout:** Control nodes with VBox/HBox/GridContainer organization
- **Complex Displays:** Tree nodes for hierarchies, GraphEdit for tech trees
- **Interaction:** Button, LineEdit, OptionButton for user input
- **Modularity:** Reusable scene components for consistency

**Development Environment:**

- **Version Control:** Git with semantic commit messages
- **Documentation:** Markdown with Mermaid diagrams for system visualization
- **Testing Strategy:** Incremental prototype development with rapid iteration
- **Code Quality:** Typed GDScript for better debugging and performance

## Active Context

**Current Development Status:**
The project is in the MVP Phase 1 implementation stage. The following core infrastructure is complete:

- ✅ **Basic Godot Project:** "ASI Sim" configured with Godot 4.4 and Forward Plus rendering
- ✅ **Main Scene:** Standard Node structure
- ✅ **Project Structure:** Standard Godot layout with ui/ directory prepared
- ✅ **Comprehensive Documentation:** Complete project brief with detailed system specifications
- ✅ **Autoload Managers:** TimeManager, CompanyManager, SaveLoadManager, and centralized Debug utility implemented and registered
- ✅ **Core Logic:** Weekly progression, financial loop, and resource tracking functional
- ✅ **Save/Load System:** JSON-based persistence integrated with managers
- ✅ **Debug Logging:** All logging routed through Debug utility, only active in debug builds

**Immediate Development Focus:**
Continuing MVP Phase 1 with UI framework and resource label integration:

1. **Minimal UI framework** - Main game interface showing company status
2. **Resource counters and progression indicators** - UI labels for Money and RP
3. **Signal connections** - UI updates in response to manager signals
4. **Save/Load foundation** - Basic game state persistence

**Technical Implementation Priorities:**

1. **Core Manager Structure:** Establishing autoload pattern for system organization
2. **Signal Architecture:** Setting up event bus for decoupled communication
3. **Resource Framework:** Creating custom resource templates for data management
4. **UI Foundation:** Building modular interface components

**Key Design Decisions Made:**

- **GDScript 2.0 with Typing:** For better performance, error checking, and maintainability
- **Autoload Manager Pattern:** Persistent systems accessible globally as service providers
- **Custom Resource Templates:** Leveraging Godot's editor integration for data definition
- **Weekly Turn-Based Progression:** Manageable complexity for solo development

**Current Challenges & Considerations:**

- **Scope Management:** Maintaining MVP focus while building extensible architecture
- **System Integration:** Ensuring clean signal-based communication between managers
- **UI Complexity Balance:** Information density vs. usability for management simulation
- **Performance Planning:** Preparing for future scalability with weekly calculations

## Progress

**Completed Milestones:**

- ✅ **Project Initialization:** Godot 4.4 project structure with proper configuration
- ✅ **Development Environment:** VSCode integration with file structure and rules
- ✅ **Comprehensive Planning:** Detailed project brief with technical specifications
- ✅ **Memory Bank System:** Documentation framework for knowledge persistence across sessions
- ✅ **Basic Scene Setup:** Main.tscn implementation
- ✅ **Autoload Core Managers:** TimeManager, CompanyManager, SaveLoadManager, Debug
- ✅ **Core Logic:** Weekly tick, financial loop, resource tracking
- ✅ **Save/Load System:** JSON-based, integrated with managers
- ✅ **Debug Logging:** Centralized, debug-only

**Currently Active Tasks:**

- ✅ **MVP Phase 1 Core Infrastructure:** Project structure, autoloads, save/load, and debug logging implemented
- 🔄 **UI Framework:** Main screen and company overview panel in progress
- 🔄 **Development Workflow:** Setting up efficient Godot development patterns

**Next Immediate Steps (Phase 1):**

1. **Implement TimeManager autoload:** Complete
2. **Create CompanyManager autoload:** Complete
3. **Build foundational UI:** In progress
   - Main game interface layout
   - Company status display panels
   - Resource counters and progression indicators
4. **Add basic save/load:** Complete
   - SaveLoadManager autoload
   - JSON-based state persistence
   - Version compatibility framework

**Next Steps (Phase 2):**

1. **TechData custom resource design** for R&D project templates
2. **Linear tech tree implementation** (5-7 technologies leading to Proto-AI)
3. **R&D project management UI** for viewing and initiating research
4. **Project completion mechanics** with resource consumption and unlocks

**Validation Targets:**

- **Core Loop Functionality:** Time progression → Resource management → R&D progression
- **UI Responsiveness:** Clear feedback for all player actions and system changes
- **Save/Load Reliability:** State persistence across sessions without data loss
- **Architecture Extensibility:** Clean foundation for post-MVP feature additions

**Success Metrics Defined:**

- **Technical:** Clean autoload architecture, responsive UI, reliable persistence
- **Gameplay:** Engaging core loop demonstrating company → R&D → ASI progression
- **Code Quality:** Maintainable, well-documented, extensible codebase
- **Player Experience:** Clear feedback loops and intuitive management interface

**Learning Insights:**

- **Godot 4.4 Advantages:** Excellent custom resource system aligns perfectly with data-driven design
- **Signal Architecture Benefits:** Early investment in decoupled communication simplifies expansion
- **MVP Strategy Value:** Ultra-simplified initial systems enable rapid prototyping and validation
- **Documentation Impact:** Comprehensive planning accelerates development and maintains vision clarity
- **Solo Development Approach:** Modular design patterns essential for manageable complexity

**Risk Mitigation Strategies:**

- **Feature Creep Prevention:** Strict MVP scope adherence with post-MVP expansion planning
- **Technical Debt Management:** Clean architecture from start vs. rapid prototyping balance
- **Complexity Control:** Signal-based system separation for independent development/testing
- **Extensibility Insurance:** Resource-based data templates for easy content expansion
