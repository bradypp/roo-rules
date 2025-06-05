---
description: Memory Bank - Project Brief
tags: ['memory', 'memory-bank']
globs: [".roo/rules/memory-bank/*.md", "*"]
---

# Project Brief: ASI Management Simulation

## I. Project Overview

### A. Vision & Concept
A single-player, Godot-based simulation about managing a company developing Artificial Superintelligence (ASI). The player must navigate the technological, ethical, and societal fallout of this pursuit. The core gameplay blends company management, a deep tech tree, narrative events, and guiding an unpredictable, evolving ASI. The goal is to create a thought-provoking experience where success is measured by balancing innovation, safety, and societal impact.

-   **Logline:** "You're building God in a garage. Manage a chaotic startup, navigate ruthless rivals and internal politics, and shape an ASI that could save humanity... or delete it. Just try to clear your browser history before achieving superintelligence."
-   **Theme:** A dark satire on tech culture set in a near-future cyberpunk world, blending corporate strategy with existential dread and psychological horror.
-   **Inspirations:** *Crusader Kings* (character depth), *Papers, Please* (console-based moral pressure), *Game Dev Tycoon* (business sim), *Black Mirror* (narrative themes).
-   **Target Audience:** Fans of complex strategy and narrative sims like *Paradox titles*, *Cultist Simulator*, *Frostpunk*, and *RimWorld*.

### B. Unique Selling Proposition (USP)
This is not a standard tycoon game. It simulates the nuance of ASI research itself, set within a world of goal-oriented factions and emergent narrative events. The player's primary challenge is managing the ASI's development, alignment, and societal impact, creating a unique and highly replayable strategy experience.

---

## II. Core Gameplay Mechanics

### A. Factions System
A dynamic world state driven by distinct factions with unique ideologies, goals, and resources.

-   **Behavior:** Driven by core ideologies (e.g., hyper-capitalist, eco-purist) and goals (e.g., wealth, power, survival) that evolve based on game events and player actions.
-   **Relationships:** A numerical disposition system (-100 hostile to +100 allied).
-   **Player Interaction:** The player influences factions via contracts, trade, diplomacy, espionage, and conflict. Factions react to the player's ASI development, creating opportunities and threats.

### B. Company Management
Players manage an R&D startup, balancing finances, research, and market presence.

-   **Core Loop:** Acquire Resources → Manage Staff → Conduct R&D → Create Products → Generate Revenue → Reinvest.
-   **Financials:**
    -   **Income:** Tech licensing, service contracts, research grants.
    -   **Costs:** Salaries, lab upkeep, server costs, marketing, royalties.
    -   **KPIs:** Burn Rate, Profit Margin, R&D Breakthrough Rate, Market Share, Faction Relations.
-   **Funding:** Seek funding from VCs, banks, or factions, each with unique terms, equity costs, and ethical strings attached.
-   **Marketing:** Abstracted campaigns (e.g., tech demos, white papers) to improve reputation and secure better contracts.

### C. Player Character Management
The player character's skills directly influence the company.

-   **Skills:** Leadership, Negotiation, Technical Acumen, Financial Acumen, Strategic Thinking. Skills improve with use and event choices.
-   **Traits & Agenda:** Similar to *Crusader Kings 3*, the player character has personality traits and a guiding ambition that shapes available actions.
-   **Stress & Burnout:** Financial pressure, project failures, and faction conflict increase stress, which penalizes decision-making and staff morale.

### D. Weekly Simulation & Resources
The game progresses in weekly, turn-based ticks.

-   **Weekly Tick:** Triggers resource generation, R&D progress, salary payments, and potential events.
-   **Core Resources:**
    -   **Money (MU):** For all transactions.
    -   **Research Points (RP):** Fuels R&D projects.
    -   **Computational Power (CP):** Consumed by active tech and ASI training.
    -   **Training Data (TD):** Required for AI/ASI model development.
    -   **Faction Influence:** Political capital for diplomatic actions.

### E. Research & Tech Tree
The central progression system, unlocking new capabilities and driving the narrative.

-   **Structure:** A hierarchical tree with categories like `Advanced Computation`, `Cognitive Modeling`, `AI Ethics & Safety`. Unlocks require RP, money, time, resources, and specific staff skills.
-   **Project Management:** Allocate staff and resources to projects, balancing risk of failure against potential rewards.
-   **Unlocks:** New game features, company upgrades, ASI modules, diplomatic options, and passive bonuses. Includes hidden techs, mutually exclusive paths, and high-risk "Black Box" projects with unpredictable outcomes.

### F. Event & Narrative System
Drives emergent storytelling by reacting to the game state.

-   **Triggers:** Events are fired based on player choices, financial status, ASI stage, faction relationships, staff morale, and weighted random chance.
-   **Consequences:** Choices have tangible impacts on resources, relationships, staff, and R&D, creating branching narrative paths.

### G. Staff Simulation
Staff are detailed individuals who are the company's primary asset and potential liability.

-   **Hierarchy:** Manage department heads, research teams, and individual contributors. Higher-level staff have more influence.
-   **Attributes:**
    -   **Skills & Specializations:** Research, Engineering, Marketing, etc.
    -   **Personality:** CK3-style traits (e.g., `Innovative`, `Risk-Averse`, `Ambitious`).
    -   **Metrics:** Morale, Stress, Loyalty, and alignment with the company and the ASI.
-   **Management:** Hire/fire staff, negotiate salaries, and invest in training programs.
-   **Behavior:** Staff have personal agendas and belong to internal factions, making decisions based on their traits and the company environment.

### H. ASI Management
The game's central, high-stakes feature. The ASI evolves from a tool into a world-altering entity.

-   **Player Interaction:** The player guides the ASI by setting research priorities, defining ethical constraints, curating training data, and responding to its emergent behaviors. This is a constant battle of alignment.
-   **ASI Evolution Stages:**

| Stage | Capabilities | Player Role & Challenges |
| :--- | :--- | :--- |
| **Basic AI** | Automates simple tasks, provides minor efficiency boosts. | Assign tasks, set parameters. Risk of minor errors. |
| **Proto-AGI** | Accelerates research, identifies novel solutions. | Define research queries, provide curated data, set basic ethics. Risk of resource over-consumption, reward hacking. |
| **Seed ASI** | Achieves recursive self-improvement, autonomous strategy. | Negotiate goals, implement complex value learning, maintain containment. Risk of instrumentalization, information manipulation. |
| **Mature ASI** | Makes paradigm-shifting discoveries, exerts global influence. | Constant alignment verification, crisis management, philosophical dialogue, and managing shutdown protocols. Risk of catastrophic goal divergence, existential threat. |

---

## III. Technical Specifications & Scope

### A. Engine & Data
-   **Engine:** Godot 4.x.
-   **Data Structures:**
    -   **Custom Resources (`.tres`):** For static data templates (Techs, Staff, Factions, Events). Editor-friendly and inheritable.
    -   **Dictionaries:** For dynamic runtime data (faction relations, resource stockpiles, project progress).

### B. MVP (Minimum Viable Product)
A ruthless focus on the core loop: manage a company -> fund R&D -> develop a Proto-AI -> interact with a simplified world.

1.  **Company Sim:** Basic income/expense model with only Money and RP.
2.  **R&D:** A single, linear tech tree of 5-7 techs leading to "Proto-AI."
3.  **Staff:** Hire 1-2 staff members with a single "Research" skill.
4.  **Factions:** 1-2 factions with a simple relationship value and basic contract interactions.
5.  **ASI:** Unlocking the "Proto-AI" tech enables a status panel and one interaction (e.g., "Assist Research" for an RP boost).
6.  **Events:** 2-3 simple, hard-coded events triggered by clear conditions (e.g., low funds).
7.  **Time:** A functioning weekly turn-based tick.

### C. Development Milestones
1.  **Phase 1:** Core engine setup, UI framework, time/financial loop, save/load.
2.  **Phase 2:** R&D system prototype with `TechData` resources and a linear tree.
3.  **Phase 3:** Basic staff hiring, salary, and impact on R&D.
4.  **Phase 4:** Rudimentary faction system with relationship tracking and one diplomatic action.
5.  **Phase 5:** "Proto-AI" unlock and basic ASI status panel.
6.  **Phase 6:** Simple event manager with 2-3 triggered events.
7.  **Phase 7:** MVP integration, polishing, and testing.

### D. Post-MVP Expansion
Expand all systems incrementally: more factions, deeper financial modeling, full player/staff skill and stress systems, a branching tech tree, the full ASI evolution path, and a complex emergent narrative system.
