# Game Operations & QA Sandbox Laboratory

Welcome to my personal hands-on testing and quality assurance portfolio. I set up this active workspace to practice manual regression cycles, check database entries, and handle player support tickets using industry-standard tools.

## My Portfolio Setup
* **Bug Tracking Tools:** Jira Software & Jira Service Management (Using a standard Kanban board layout).
* **Version Control:** Linked my GitHub repository to my Jira board to practice using automated Smart Commits to sync code updates directly to active tickets.
* **My Testing Focus:** Running structured manual test scripts, writing step-by-step reproduction paths, and cross-referencing asset data tables.

---

## Master QA Regression Test Scripts

### Test Case ID: TC-INV-001 (Inventory UI Asset Interaction)
* **Pre-conditions:** Character Blueprint must have inventory capacity set to > 0. Master item data table populated with valid asset references.
* **Execution Steps:**
  1. Open the player inventory screen overlay canvas.
  2. Locate a valid inventory item row (e.g., Weapon Asset ID 094).
  3. Drag the cursor from the inventory UI bounding box directly into the world environment space.
  4. Release the primary cursor input.
* **Expected Result:** The UI asset clears from the inventory array, and an identical 3D static mesh actor dynamically instantiates into the world space with correct collision properties.
* **Actual Result:** Passed. Mesh spawns correctly on the ground grid coordinates.

### Test Case ID: TC-AUD-002 (Dynamic Environmental Occlusion)
* **Pre-conditions:** Audio Volume actor bounds aligned cleanly with interior safehouse geometry. Sound Attenuation configurations assigned to weather particles.
* **Execution Steps:**
  1. Initiate an active outdoor weather event script (e.g., Heavy Rain Loop).
  2. Navigate the character pawn completely inside an enclosed residential safehouse structure.
  3. Ensure all doors, hatches, and window structural blueprints are closed.
* **Expected Result:** Outdoor sound waves attenuate seamlessly by -12dB and apply a low-pass filter override at 1kHz. In-engine audio prioritizes interior situational audio cues (footsteps, item pickups).
* **Actual Result:** Failed. Tracking details logged inside active Jira defect tickets.

### Test Case ID: TC-DBD-003 (Asymmetrical Perk Interaction Tracking)
* **Pre-conditions:** Survivor loadout assigned with active movement modifier tokens (e.g., Exhaustion / Haste triggers). 
* **Execution Steps:**
  1. Trigger an accelerated physical navigation interaction (e.g., Fast Vaulting a window mesh asset).
  2. Monitor the active Status Effect HUD layout display elements immediately upon exit frame animation.
  3. Verify the execution of corresponding cooling timers inside the backend database registry.
* **Expected Result:** Haste velocity values modify to 1.5x multiplier for 3 seconds, and an instant 40-second Exhaustion tracking token forces down onto the status data table array.
* **Actual Result:** Mixed validation. Visual UI clears but database variables stay at Null values.

---

## Master Defect & Triage Log

### 1. Live-Service Systems & Perks (Component: Gameplay / Mechanics)
* **[Unresolved] Ticket 1:** Character and item models clipping through environment hook geometry during specific Survivor unhook animations.
* **[Resolved] Ticket 2:** Movement modifier perk assets failing to pass corresponding Exhaustion cooldown tracking tokens back to the status array.
* **[Resolved] Ticket 3:** Environmental weather scripts failing to pass proper temperature numerical arguments to standing water meshes.
* **[Resolved] Ticket 4:** AI navigation components tracking stale threat noise coordinate nodes after player repositioning.

### 2. Technical Audio Pipelines (Component: Audio / Cues & Assets)
* **[In Progress] Ticket 5:** Core vehicle sound wave engine loop asset containing digital clicks at boundary seam points.
* **[In Progress] Ticket 6:** Interior safehouse volume actors failing to override global attenuation settings and apply sound occlusion low-pass filters.

### 3. Database Configurations & Player Support (Component: Database / Configuration)
* **[Resolved] Ticket 7:** Unassigned audio profile reference tokens inside master item configuration data tables causing silent melee interactions.
* **[Unresolved] Ticket 8:** Cross-referencing payment ledgers and performing manual profile database overrides for missing player Auric Cell transactions.
* **[In Progress] Ticket 9:** Triaging client hardware driver routing conflicts and operating system security privacy permissions for proximity voice chat communications.

---

## Subject Matter Expertise & Platform Metrics: Dead by Daylight

To back my entry-level testing setup with real-world player knowledge, below is my active live-service experience representing a decade of personal familiarity with Dead by Daylight's mechanics and gameplay loops.

* **Account Lifespan:** Active player and community veteran since 2016 (Continuous familiarity tracking game patches and balance updates).
* **Role Competency:** Deep understanding of both asymmetrical execution loops (High-tier Survivor perk coordination and Killer pathfinding behaviors).
* **Mechanics Mastery:** Strong grasp of how perks interact, including vaulting speeds, Exhaustion/Haste cooldown priorities, and audio cues for skill checks.
* **Live Sandbox Testing:** My personal hours in the Fog serve as the direct baseline data for the custom test scripts and database forms hosted inside this workspace.
