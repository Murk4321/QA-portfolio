
## Main Menu

### High ###
<details> 
  <summary>TC-MM-001: Play button starts the game </summary>

  **Priority: High**
  
  **Steps:**
  1. Press the "Play" button in main menu
  
  **Expected Result:**
  Tutorial scene loads, player appears on the screen
  
  **Status:**
  Pass

</details>

### Medium ###

<details> 
  <summary>TC-MM-002: Quit button closes the game </summary>

  **Priority: Medium**
  
  **Steps:**
  1. Press the "Quit" button in main menu
  
  **Expected Result:**
  Game closes without issues
  
  **Status:**
  Pass

</details>

### Low ###

<details> 
  <summary>TC-MM-003: Disclaimer is shown in main menu </summary>

  **Priority: Low**
  
  **Steps:**
  1. Open the game
  
  **Expected Result:**
  "Disclaimer" block with text about possible bugs appears in bottom right corner
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-MM-004: Background animation is active </summary>

  **Priority: Low**
  
  **Steps:**
  1. Open the game
  2. Wait a few seconds
  
  **Expected Result:**
  NPCs and objects in the background are animated and moving.
  
  **Status:**
  Pass

</details>

---

## Tutorial

### High ###

<details> 
  <summary>TC-TUT-001: Current task UI element is shown </summary>

  **Priority: High**
  
  **Steps:**
  1. Press play button in main menu
  2. Check upper left corner
  
  **Expected Result:**
  Text "Current task: Listen to Grandpa" shown immediatel
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-002: Dialogue with Grandpa starts immediately </summary>

  **Priority: High**
  
  **Steps:**
  1. Press play button in main menu
       
  **Expected Result:**
  Dialogue with Grandpa starts immediately after entering the tutorial
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-003: Movement works </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finished first dialogue

  **Steps:**
  1. Press buttons W, A, S, D
  
  **Expected Result:**
  Player should move
  - W - up
  - A - left
  - S - Down
  - D - right
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-004: Inventory navigation works </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finished first dialogue

  **Steps:**
  1. Press buttons 1-6
  OR Scroll mouse wheel up and down
  
  **Expected Result:**
  - Inventory should highlight current chosen item and change chosen item depending on the input
  - Player equips chosen item
  
  **Status:**
  Pass

</details>

<details> 
  <summary>TC-TUT-005: Dig 4 holes - counter is working </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finished first dialogue
  
  **Steps:**
  1. Choose showel tool
  2. Press LMB on any nearby grass tile
  
  **Expected Result:**
  - Dig animation played
  - Grass tile is changed to dirt tile
  - UI counter increases by 1
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-006: Watering can doesn't work without water </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finished first dialogue
  - Watering can is empty (shows 0 in inventory)

  **Steps:**
  1. Choose watering can
  2. Press LMB on any nearby dirt tile
  
  **Expected Result:**
  Nothing happens
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-007: Filling watering can with water </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finished first dialogue
  
  **Steps:**
  1. Choose watering can
  2. Move towards pond
  3. Press RMB on any water tile
  
  **Expected Result:**
  Watering can fills up, shows 3 in the inventory
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-008: Watering dirt tiles </summary>

  **Priority: High**
  
  **Preconditions:**
  - Watering can is filled
  - Dug 4 holes with shovel
    
  **Steps:**
  1. Choose watering can
  2. Move towards dug dirt tiles
  3. Press LMB on any dirt tile
  
  **Expected Result:**
  - Counter on watering can decreases by 1
  - Counter in task UI element increases by 1
  - Water animation is played
  - Dirt tile changes to watered tile
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-009: Collecting wild flowers </summary>

  **Priority: High**
  
  **Preconditions:**
  - Watered 4 dug up dirt spots

  **Test Data:**
  
  **Steps:**
  1. Choose flower pouch
  2. Move towards any flower tile
  3. Press RMB on any nearby flower tile
  
  **Expected Result:**
  - Flower tile is replaced by grass tile
  - Counter on flower pouch increases by 1
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-010: Plant flowers </summary>

  **Priority: High**
  
  **Preconditions:**
  - Flower pouch has at least 1 flower
  - Watered 4 dug up spots
  
  **Steps:**
  1. Choose flower pouch
  2. Press LMB on any nearby watered dirt tile
  
  **Expected Result:**
  - Flower pouch counter decreases by 1
  - Watered dirt tile is replaced by planted dirt tile
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-012: Gather grown flowers </summary>

  **Priority: High**
  
  **Preconditions:**
  - Planted at least 1 flower
  - Flower finished growing
  
  **Steps:**
  1. Choose knife tool
  2. Press LMB on any nearby grown flower
  
  **Expected Result:**
  - Flower is removed from dirt
  - Flower appears in inventory slot 5 and becomes current chosen item
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-013: Placing 4 flowers </summary>

  **Priority: High**
  
  **Preconditions:**
  - Grown 4 flowers
  
  **Steps:**
  1. Pick up 4 flowers one by one
  2. Press LMB on any nearby grass tile holding a flower
  
  **Expected Result:**
  - Each flower gets put on chosen grass tile
  - After fourth flower game finishes the tutorial and moves to next scene
  
  **Status:**
  Pass

</details>

### Medium ###

<details> 
  <summary>TC-TUT-011: Wait for flowers to grow </summary>

  **Priority: Medium**
  
  **Preconditions:**
  - Planted at least 1 flower
  
  **Steps:**
  1. Wait for plants to grow
  
  **Expected Result:**
  Flowers should increase in size with time
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-TUT-014: Tools are unavailable until needed </summary>

  **Priority: Medium**
  
  **Steps:**
  1. Try to choose tool that is now required by current task
  
  **Expected Result:**
  Player can choose only required tools and can't use other
  
  **Status:**
  Fail

</details>

---

## Stage 1

### High ###

<details> 
  <summary>TC-S1-001: Stage 1 tasks are shown </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finish the tutorial
  
  **Steps:**
  1. Check upper left corner
  
  **Expected Result:**
  Task UI element is shown
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-002: Timer is working </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finished the tutorial
  
  **Steps:**
  1. Find a pentagram and timer above
  2. Observe the timer
  
  **Expected Result:**
  - Timer is visible
  - Timer is counting down from 1 minute 30 seconds
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-003: Placing a flower on pentagram </summary>

  **Priority: High**
  
  **Preconditions:**
  - Player has flower

  **Steps:**
  1. Choose flower item
  2. Press RMB on pentagram
  
  **Expected Result:**
  - Flower is removed from inventory
  - UI counter increases by 1
  - Timer resets back to 01:30
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-004: Exact color requested </summary>

  **Priority: High**
  
  **Preconditions:**
  - Sacrificed 4 or 9 flowers
  
  **Steps:**
  1. Sacrifice the last of 4 or 9 flowers
  2. Observe the area above timer
  
  **Expected Result:**
  - Pentagram demands a flower of exact color, colorful blob is shown above timer
  - Timer sets to 05:00
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-005: Accept flower of exact color </summary>

  **Priority: High**
  
  **Preconditions:**
  - Pentagram demands flower of exact color
  
  **Steps:**
  1. Choose flower item that has at least 80% similarity with requested color (euclidean distance is 0.35 or less)
  2. Press RMB on pentagram
  
  **Expected Result:**
  - Flower is removed from inventory
  - UI counter increases by 1
  - Timer resets back to 01:30
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-006: Dismiss flower of incorrect color </summary>

  **Priority: High**
  
  **Preconditions:**
  - Pentagram demands flower of exact color
  
  **Steps:**
  1. Choose flower item that has less than 80% similarity with requested color (euclidean distance is more than 0.35)
  2. Press RMB on pentagram
  
  **Expected Result:**
  - Flower is removed from inventory
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-007: Timer runs out </summary>

  **Priority: High**
  
  **Preconditions:**
  - Finished the tutorial
  - Player sacrificed less than 10 flowers
  
  **Steps:**
  1. Wait until timer above pentagram counts down to zero
  
  **Expected Result:**
  - Game over screen is shown
  - Game ends and puts player in main menu
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-008: Can't grow flowers after tenth </summary>

  **Priority: High**
  
  **Preconditions:**
  - Player sacrificed 10 flowers
  
  **Steps:**
  1. Try to plant a new flower
  
  **Expected Result:**
  - All existing flowers die
  - New flowers die after they're ~70% grown
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S1-009: Timer runs out after tenth flower </summary>

  **Priority: High**
  
  **Preconditions:**
  - Player sacrificed more than 10 flowers
  
  **Steps:**
  1. Wait until timer above pentagram counts down to zero
  
  **Expected Result:**
  - Dialogue with demon is shown
  - Stage 2 starts
  
  **Status:**
  Pass

</details>

---

## Stage 2

### High ###

<details> 
  <summary>TC-S2-001: Task UI element shows "???" </summary>

  **Priority: High**
  
  **Preconditions:**
  - Started stage 2
  
  **Steps:**
  1. Enter stage 2
  2. Look at upper left corner
  
  **Expected Result:**
  UI element with tasks shows "Current task: ???"
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S2-002: Player can't grow flowers </summary>

  **Priority: High**
  
  **Preconditions:**
  - Enter stage 2
  
  **Steps:**
  1. Try to grow a flower
  
  **Expected Result:**
  Player can plant a flower but they die shortly after planting
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S2-003: Timer runs out on stage 2 </summary>

  **Priority: High**
  
  **Preconditions:**
  - Enter stage 2

  **Steps:**
  1. Wait until timer runs down to zero
  
  **Expected Result:**
  Stage 3 starts
  
  **Status:**
  Pass

</details>

---

## Stage 3

### High ###

<details> 
  <summary>TC-S3-001: New task is shown </summary>

  **Priority: High**
  
  **Preconditions:**
  - Enter stage 3

  **Test Data:**
  
  **Steps:**
  1. Enter stage 3
  2. Look at top left corner
  
  **Expected Result:**
  User observes new task "Kill a flob"
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S3-002: Kill another flob with knife </summary>

  **Priority: High**
  
  **Preconditions:**
  - Enter stage 3
  
  **Steps:**
  1. Choose knife
  2. Move towards any NPC flob
  3. Press RMB while looking in his direction
  
  **Expected Result:**
  - NPC is killed
  - Body moves into inventory slot 6
  - Knife sprite is replaced by bloody knife sprite
  - Music slows down
  - Player's eyes start to run around (craziness builds up)
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S3-004: Burying a body </summary>

  **Priority: High**
  
  **Preconditions:**
  - Flob was killed
  - Player has body in inventory
  
  **Steps:**
  1. Chose body item
  2. Move towards dirt tile or dig one up
  3. Press LMB on dirt tile
  
  **Expected Result:**
  - Dirt tile is replaced by bloody dirt tile
  - Body is removed from inventory
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S3-005: Growing demon flowers </summary>

  **Priority: High**
  
  **Preconditions:**
  - There is at least one bloodied tile on map
  - Player has at least one flower in pouch

  **Steps:**
  1. Move towards bloodied tile
  2. Select flower pouch
  3. Press RMB on bloodied tile
  4. Wait for flower to grow
  
  **Expected Result:**
  - Flower gets planted
  - After approximately 45 seconds it grows fully
  - Central part of flower starts to glow, indicating it's ready
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S3-006: Flobs flee after seeing crime </summary>

  **Priority: High**
  
  **Preconditions:**
  - Player killed one of NPCs
  
  **Steps:**
  1. Select body or bloodied knife
  2. Approach any NPC flob
  
  **Expected Result:**
  - NPC should run away
  - That NPC will run away if he sees you again
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S3-007: Sacrificing demon flowers</summary>

  **Priority: High**
  
  **Preconditions:**
  - Stage 3 started
  - Player has grown at least one flower
  
  **Steps:**
  1. Choose a flower in inventory
  2. Move towards pentagram
  3. Press RMB on pentagram
  
  **Expected Result:**
  - Flower is removed from inventory
  - UI task counter is increased by 1
  - Timer resets
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S3-008: Bad ending </summary>

  **Priority: High**
  
  **Preconditions:**
  - Entered stage 3
  
  **Steps:**
  1. Kill 10 NPC flobs
  
  **Expected Result:**
  With each kill:
  - Screen gradually darkens
  - Music gradually slows down
  - Screen shake gradually increases
  - Player eyes move faster and faster
  After 10th kill:
  - Move player to game over scene
  - Cause: went crazy
  
  **Status:**
  Pass

</details>
<details> 
  <summary>TC-S3-009: Good ending </summary>

  **Priority: High**
  
  **Preconditions:**
  - Sacrificed at least one demon flower
  
  **Steps:**
  1. Find blue flowers that were spawned in random place
  2. Collect the flowers with flower pouch
  3. Grow new flower using these flowers
  4. Sacrifice that flower after it's fully grown
  
  **Expected Result:**
  - Demon gets defeated
  - Victory dialogue starts
  - Player is moved to game over scene (win)
  
  **Status:**
  Pass

</details>

### Medium ##

<details> 
  <summary>TC-S3-003: Washing a knife </summary>

  **Priority: Medium**
  
  **Preconditions:**
  - Knife is bloody
  
  **Steps:**
  1. Choose a knife
  2. Move towards lake or pond
  3. Press LMB on any water tile
  
  **Expected Result:**
  - Bloody knife sprite is replaced by regular knife sprite
  
  **Status:**
  Pass

</details>
