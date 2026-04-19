# Bug Reports


### Critical

---

### High

<details>
  <summary>BUG-002: Player can use tools before they are unlocked by tutorial stage</summary>

  **Severity:** High
  
  **Priority:** High
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Tutorial has started
  - Current task has not yet unlocked all tools

  **Steps to Reproduce:**
  1. Start the tutorial
  2. Before reaching the stage that unlocks a specific tool, select it from inventory
  3. Use the tool on a valid tile

  **Expected Result:**
  Tool cannot be used until the tutorial stage that requires it is reached

  **Actual Result:**
  Player can select and use tools before they are unlocked by the current tutorial stage

  **Attachments:** -

</details>
<details>
  <summary>BUG-004: Tutorial can be broken by performing actions out of order</summary>

  **Severity:** High

  **Priority:** High
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - BUG-002 is reproducible (tools usable before unlocked)

  **Steps to Reproduce:**
  1. Start the tutorial
  2. Dig only 3 holes instead of 4
  3. Use the 3 holes to grow 4 flowers
  4. Complete the flower delivery step

  **Expected Result:**
  Tutorial enforces correct order of actions and requires all 4 holes to be dug before proceeding

  **Actual Result:**
  Tutorial accepts the completion condition even though actions were performed out of order. The tutorial only stops to require the 4th hole to be dug after the 4 flowers have already been grown, resulting in a broken but non-crashing state

  **Attachments:** -

</details>
<details>
  <summary>BUG-005: Item state is not reset when transitioning from tutorial to game</summary>

  **Severity:** High
  
  **Priority:** High
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Tutorial is completed

  **Steps to Reproduce:**
  1. During the tutorial, collect more items than normally possible (e.g. 6 flowers)
  2. Complete the tutorial
  3. Observe inventory at the start of Stage 1

  **Expected Result:**
  Inventory is reset to default state when transitioning from tutorial to Stage 1, since the tutorial takes place 6 years prior to the main game

  **Actual Result:**
  All items collected during the tutorial are carried over into the main game

  **Attachments:** -

</details>
<details>
  <summary>BUG-016: Requested flower color may never spawn, making stage uncompletable through no fault of the player</summary>

  **Severity:** High
  
  **Priority:** High
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Player has sacrificed exactly 4 or 9 flowers
  - Demon has requested a specific flower color

  **Steps to Reproduce:**
  1. Sacrifice 4 flowers on the pentagram
  2. Observe the color requested by the demon
  3. Attempt to find a flower matching the requested color (≥80% similarity)
  4. Observe available flowers on the map

  **Expected Result:**
  The game guarantees that a flower matching the requested color spawns within a reasonable time or after a set number of attempts, ensuring the stage remains completable

  **Actual Result:**
  Requested flower color is fully random and spawned flower colors are fully random — a matching flower may never appear, causing the player to fail the stage due to factors outside their control

  **Attachments:** -

</details>

---

### Medium

<details>
  <summary>BUG-003: Player can interact with the world during dialogue</summary>

  **Severity:** Medium
  
  **Priority:** Medium
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Dialogue is active

  **Steps to Reproduce:**
  1. Trigger any dialogue
  2. While dialogue is playing, attempt to use a tool on a tile

  **Expected Result:**
  All player interactions are disabled during dialogue, including tool usage

  **Actual Result:**
  Player can interact with the world during dialogue — only movement is disabled

  **Attachments:** -

</details>
<details>
  <summary>BUG-008: Game cannot be paused</summary>

  **Severity:** Medium
  
  **Priority:** Medium
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Any stage has started

  **Steps to Reproduce:**
  1. Start any stage
  2. Press Escape or any other key expecting a pause menu

  **Expected Result:**
  Game pauses and a pause menu is shown

  **Actual Result:**
  No pause functionality exists in the game

  **Attachments:** -

</details>
<details>
  <summary>BUG-009: No settings menu for audio and music control</summary>

  **Severity:** Medium
  
  **Priority:** Medium
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Game is launched

  **Steps to Reproduce:**
  1. Launch the game
  2. Look for a settings menu in main menu or in-game

  **Expected Result:**
  Settings menu is available with at least volume and music controls

  **Actual Result:**
  No settings menu exists — audio and music cannot be adjusted

  **Attachments:** -

</details>
<details>
  <summary>BUG-012: Map lacks landmarks, player can get lost</summary>

  **Severity:** Medium
  
  **Priority:** Low
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Any stage has started

  **Steps to Reproduce:**
  1. Start any stage
  2. Move away from the starting area
  3. Attempt to navigate back

  **Expected Result:**
  Map contains enough visual landmarks for the player to orient themselves

  **Actual Result:**
  Map is empty and visually repetitive — no landmarks exist to help the player navigate

  **Attachments:** -

</details>
<details>
  <summary>BUG-013: No in-game exit option — game can only be closed via Alt+F4</summary>

  **Severity:** Medium
  
  **Priority:** Medium
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Any stage has started

  **Steps to Reproduce:**
  1. Start any stage
  2. Look for an option to exit the game without Alt+F4

  **Expected Result:**
  An in-game exit option is available (e.g. via pause menu or main menu)

  **Actual Result:**
  No in-game exit option exists — the only way to close the game during play is Alt+F4

  **Attachments:** -

</details>
<details>
  <summary>BUG-015: Scene transition timing is broken — screen briefly reappears before scene changes</summary>

  **Severity:** Medium
  
  **Priority:** Medium
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Player has met the condition to trigger the final scene transition

  **Steps to Reproduce:**
  1. Meet the win condition
  2. Observe the scene transition

  **Expected Result:**
  Screen fades out smoothly and transitions directly to the final scene

  **Actual Result:**
  Screen fades out, then briefly reappears at full brightness before the scene finally changes — causing a visible flash

  **Attachments:** -

</details>

---

### Low

<details>
  <summary>BUG-001: Visual issues in Main Menu</summary>

  **Severity:** Low
  
  **Priority:** Low
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Game is launched

  **Steps to Reproduce:**
  1. Launch the game
  2. Observe the main menu UI

  **Expected Result:**
  - Disclaimer text is readable
  - Disclaimer block does not compete visually with the Play button
  - Buttons have a clear interactive appearance (hover effect, visual affordance)

  **Actual Result:**
  - Disclaimer text has low readability: red text on grey background with black outline
  - Disclaimer block has high visual weight and draws attention away from the Play button
  - Buttons do not look interactive — no visual cues indicating they are clickable

  **Attachments:** Screenshot of main menu recommended

</details>
<details>
  <summary>BUG-006: Footstep particles render above NPCs instead of on the ground</summary>

  **Severity:** Low
  
  **Priority:** Low
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Player is moving near NPCs

  **Steps to Reproduce:**
  1. Start the game
  2. Walk near any NPC
  3. Observe the footstep particle effects

  **Expected Result:**
  Footstep particles render below NPCs, appearing to be on the ground

  **Actual Result:**
  Footstep particles render above NPCs, appearing to float over them

  **Attachments:** Screenshot recommended

</details>
<details>
  <summary>BUG-007: Character shadow flips to opposite side when rotating</summary>

  **Severity:** Low
  
  **Priority:** Low
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Tutorial or any stage has started

  **Steps to Reproduce:**
  1. Move the character in one direction
  2. Turn the character to face the opposite direction
  3. Observe the shadow on the character sprite

  **Expected Result:**
  Shadow remains on a consistent side relative to the light source

  **Actual Result:**
  Shadow flips to the opposite side when the character rotates, breaking visual consistency

  **Attachments:** Screenshot recommended

</details>
<details>
  <summary>BUG-010: Action availability indicator does not specify which mouse button to use</summary>

  **Severity:** Low
  
  **Priority:** Low
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Player is standing on or near an interactable tile

  **Steps to Reproduce:**
  1. Stand near any interactable tile (water, dirt, flower, etc.)
  2. Observe the action availability indicator

  **Expected Result:**
  Indicator specifies which mouse button (LMB or RMB) triggers the available action

  **Actual Result:**
  Indicator only shows that an action is available, without specifying LMB or RMB

  **Attachments:** Screenshot recommended

</details>
<details>
  <summary>BUG-011: Water tile edges are too straight and inconsistent with game art style</summary>

  **Severity:** Low
  
  **Priority:** Low
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Any stage with water tiles is active

  **Steps to Reproduce:**
  1. Start any stage
  2. Observe water tiles and their edges

  **Expected Result:**
  Water tile edges match the organic, hand-drawn aesthetic of the game

  **Actual Result:**
  Water tile edges are unnaturally straight and visually inconsistent with the rest of the art style

  **Attachments:** Screenshot recommended

</details>
<details>
  <summary>BUG-014: Flowers wither instantly with no animation</summary>

  **Severity:** Low
  
  **Priority:** Low
  
  **Environment:** Windows 10 22H2, 1080p

  **Preconditions:**
  - Player has sacrificed 10 flowers on the pentagram

  **Steps to Reproduce:**
  1. Sacrifice the 10th flower on the pentagram
  2. Observe any existing flowers on the map

  **Expected Result:**
  Flowers wither gradually with a visible wither animation

  **Actual Result:**
  Flowers disappear instantly with no animation — the transition is abrupt

  **Attachments:** -

</details>

---


