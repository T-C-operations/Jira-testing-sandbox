# Game Operations and QA Sandbox Laboratory

Welcome to my personal hands-on QA portfolio. Because I am an independent researcher, I do not have direct access to proprietary studio source code or production servers. Instead, I built this repository as a **Simulated QA Laboratory**. 

I leveraged my deep knowledge of multi-genre game mechanics alongside industry-standard documentation practices to construct a 1-to-1 blueprint of a professional studio pipeline. The test cases and triage logs below are modeled after live-service environments to demonstrate exactly how I track defects, verify database tables, and manage high-volume ticketing workflows.

### Laboratory Ecosystem
*   **Bug Tracking & Agile Pipeline:** Jira Software | Jira Service Management (Kanban Framework)
*   **Version Control Architecture:** GitHub (Integrated via Automated Smart Commits)
*   **Core Testing Domains:** Functional Manual Regression | Audio Attenuation Pipelines | Backend Database Validation

---

### Master Test Scripts Matrix

| Test Case ID | Target Component | Core Validation Focus | Final Verification Status |
| :--- | :--- | :--- | :--- |
| **TC-INV-001** | Inventory UI | Drag-and-Drop Item Physics & Spatial Spawning | **PASSED** |
| **TC-AUD-002** | Audio Pipeline | Indoor Dynamic Sound Occlusion & Attenuation | **FAILED** (Logged to Jira) |
| **TC-SURV-003** | Voxel Building | Base Grid Collapse & Terrain Gravitational Physics | **MIXED VALIDATION** |

---

### 📑 Detailed Test Script Execution Protocols

#### 📋 Test Case ID: TC-INV-001 (Inventory UI Asset Interaction)
*   **Pre-conditions:** Character Blueprint inventory capacity must be set to > 0. Master item data table must be populated with valid asset references.
*   **Execution Steps:**
    1. Open the player inventory screen overlay canvas.
    2. Locate a valid inventory item row (e.g., Weapon Asset ID 094).
    3. Drag the cursor from the inventory UI bounding box directly into the world environment space.
    4. Release the primary cursor input.
*   **Expected Result:** The UI asset clears from the inventory array, and an identical 3D static mesh actor dynamically instantiates into the world space with correct collision properties.
*   **Actual Result:** **PASSED.** Mesh spawns correctly on the ground grid coordinates.

#### Test Case ID: TC-AUD-002 (Dynamic Environmental Occlusion)
*   **Pre-conditions:** Audio Volume actor bounds must be aligned cleanly with interior safehouse geometry. Sound Attenuation configurations must be assigned to weather particles.
*   **Execution Steps:**
    1. Initiate an active outdoor weather event script (e.g., Heavy Rain Loop).
    2. Navigate the character pawn completely inside an enclosed residential safehouse structure.
    3. Ensure all doors, hatches, and structural window blueprints are closed.
*   **Expected Result:** Outdoor sound waves attenuate seamlessly by -12dB and apply a low-pass filter override at 1kHz. In-engine audio prioritizes interior situational cues (footsteps, item pickups).
*   **Actual Result:** **FAILED.** Tracking details logged inside active Jira defect tickets.

#### Test Case ID: TC-SURV-003 (Voxel Building Grid & Container Interconnectivity)
*   **Pre-conditions:** Character Blueprint inventory slots must contain active structural building assets. Target terrain chunk must be fully generated.
*   **Execution Steps:**
    1. Open the player crafting UI menu layout canvas.
    2. Place a secure storage chest actor mesh directly onto a structural base grid tile.
    3. Load the storage container array with random item codes until maximum weight capacity is reached.
    4. Use a demolition asset to destroy the underlying foundational base grid tile.
*   **Expected Result:** The storage chest asset updates its gravity variables, collapses down safely, drops its contents as separate physics loot nodes, and maintains server data integrity.
*   **Actual Result:** **MIXED VALIDATION.** Visual mesh drops, but item database tables remain locked at Null values.

---

### Master Defect and Triage Log

#### 1. Live-Service Systems and Perks (Component: Gameplay / Mechanics)
*   `[UNRESOLVED]` **Ticket 1:** Character and item models clipping through environment hook geometry during specific Survivor unhook animations. *(Dead by Daylight Simulation)*
*   `[RESOLVED]` **Ticket 2:** Movement modifier perk assets failing to pass corresponding Exhaustion cooldown tracking tokens back to the status array. *(Dead by Daylight Simulation)*
*   `[RESOLVED]` **Ticket 3:** Environmental weather scripts failing to pass proper temperature numerical arguments to standing water meshes. *(VEIN Simulation)*
*   `[RESOLVED]` **Ticket 4:** AI navigation components tracking stale threat noise coordinate nodes after player repositioning.

#### 2. Technical Audio Pipelines (Component: Audio / Cues & Assets)
*   `[IN PROGRESS]` **Ticket 5:** Core vehicle sound wave engine loop asset containing audible digital clicks at boundary seam points. *(ATS / Logistics Simulation)*
*   `[IN PROGRESS]` **Ticket 6:** Interior safehouse volume actors failing to override global attenuation settings and apply sound occlusion low-pass filters.

#### 3. Database Configurations and Player Support (Component: Database / Configuration)
*   `[RESOLVED]` **Ticket 7:** Unassigned audio profile reference tokens inside master item configuration data tables causing silent melee interactions.
*   `[UNRESOLVED]` **Ticket 8:** Cross-referencing payment ledgers and performing manual profile database overrides for missing player Auric Cell transactions. *(Live Support Simulation)*
*   `[IN PROGRESS]` **Ticket 9:** Triaging client hardware driver routing conflicts and operating system security/privacy permissions for proximity voice chat communications.
*   `[UNRESOLVED]` **Ticket 10:** Server item lists failing to clear properly when players drop containers on the ground, causing severe game lag on high-population servers. *(VEIN Simulation)*
*   `[IN PROGRESS]` **Ticket 11:** Auditing player transaction and trade logs to track down items lost during server crashes to manually restore them to player accounts.

---

### Game Knowledge and Personal Playtime Metrics

Gaming has been a foundational part of my life since childhood, stretching back to the original PlayStation era. Over the decades, I expanded my horizon from a console player into a dedicated variety gamer with a deep backlog across almost every major genre. I don't just play games to pass the time; I actively explore and learn while analyzing game design systems. 

Gaming initially served as an essential support system and outlet when my health was bad and I was confined to my home during my youth. Over the years, I have actively participated in numerous alpha phases, beta cycles, and Early Access titles. I am driven by technical curiosity and a commitment to experiencing games for my own analytical and personal reasons. 

Today, gaming remains an integral part of my daily life. I spend my free time sharing this passion with my special needs son, playing his favorite titles—including *Dead by Daylight* and *Rocket League*—multiple times a day whenever possible. I am incredibly grateful to share this hobby and deep bond with him.

#### Asymmetrical Multiplayer | Dead by Daylight Veteran (2016 – Present)
*   **Systems Evolution:** Active player and community veteran since the game's launch in 2016. Extensive experience analyzing both legacy builds and modern patches, systematically tracking meta shifts and balancing updates across the title's entire lifecycle.
*   **Mechanics Mastery:** Strong technical grasp of complex perk interactions, vaulting speed variables, Exhaustion/Haste priority tracking tokens, and spatial audio cues.

#### City Simulations & Management Builders | Alpha & Beta Lifecycle Tracking
*   **Titles Analyzed:** *Planet Zoo, Eco, Two Point Hospital, Two Point Campus, The Sims, Farming Simulator,* etc.
*   **Systems Evolution:** Years of firsthand experience playing complex simulation mechanics from early alpha builds to full release. Actively track shop inventory grid placements, menu screen UI layouts, and progression lock-step architectures.
*   **Data Verification:** Solid conceptual understanding of player-driven economies, item resource gathering systems, and checking backend configuration sheets for calculation errors.

#### Open-World Survival & Physics Engines | Early Access Optimization Analysis
*   **Titles Analyzed:** *Grand Theft Auto, VEIN, Rocket League, Subnautica, 7 Days to Die, Astroneer,* etc.
*   **Logistics Analysis:** Extensive runtime analyzing vehicle physics, trunk storage capacity limitations, structural base-building grid snapping, voxel terrain deformation, and character clipping anomalies across early alpha versions and final release patches.
*   **Audio Fluency:** Supported games like *Astroneer* from day-one Early Access to completion. Equipped with a trained ear from Full Sail University to track environmental sound attenuation, clipping audio loops, and client-side audio hardware connection errors.

---

### Interview Reference: Portfolio Methodology

To maintain absolute transparency during the interview process, here is a breakdown of how this laboratory operates:

*   **No Live-Server Access:** I do not possess backend server access to the commercial titles listed above. The logs, database entries, and transaction ledger references are fully simulated scenarios based on my 5-year logistics logic and lifetime game knowledge. 
