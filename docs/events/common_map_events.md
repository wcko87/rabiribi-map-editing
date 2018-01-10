# Misc. Events

- **[34] Start point**
  - Spawns Erina here.  In custom maps, the game will look for this event in area0.map

- **[45] Heal point**
  - Spawns a glowing heal point.  When Erina stands near this, her HP recovers.

- **[224] Save point**
  - Spawns a save point.  Typically built in a 2 wide by 3 tall rectangle with a 5001 on top, like in the image below.
  
    ![savepoint](https://user-images.githubusercontent.com/27341392/30837013-7d1ca802-a294-11e7-896e-fd9b12494ad7.png)

- **[250] Easter egg**
  - Spawns an easter egg item.
  - If a **[250] easter egg** is placed within a collidable block and next to a **[3] Bomb chain block**, the block with the easter egg also acts as a bomb chain block, and can be blown up with bombs.


# Tile modifier events

These are events that you typically place directly on tiles in order to add destructables to the map.

If a block disappears, any collision attached to it also disappears. Conversely, if a block appears, then any collision attached to it will only take effect after it appears.

- **[1] Wood block**
  - Block can be destroyed by hammer attacks.

- **[2] Bomb block**
  - Block can be destroyed by explosives.

- **[3] Bomb chain block**
  - Block can be destroyed by explosives, and will cause a chain reaction with other blocks with event 3 on them.
  - The chain reaction doesn't need to be on solid tiles, and will follow the path set. Example:
  
    ![paintdotnet_2017-09-10_01-48-03](https://user-images.githubusercontent.com/19506837/30246509-1df76ac8-95ca-11e7-8eaf-ff68adec8a48.png)
  - The chain will follow all event 3 blocks despite only having two blocks to destroy along the way.

- **[6] Fairy block**
  - Block can be destroyed by Ribbon shots.

- **[7] Ice block**
  - Erina will destroy these blocks on contact if she has the Fire Orb.

- **[8] Cracked block**
  - If Erina steps on this block, it makes a snapping sound, then disappears a short amount of time later.
  
- **[9] Low difficulty block**
  - These blocks only show up on difficulties Normal and below.
  - If the difficulty is increased above normal (e.g. by event 543) in-game, the blocks vanish instantly.
  - If the difficulty is decreased to normal and below in-game, the blocks don't reappear until a map transition or autosave reload.

- **[192] Reset breakable blocks**
  - Passing through this resets breakable blocks.
  
- **[30] Low Item% block**
  - These blocks are only visible in Low Item% mode. Upon reaching 10% item collection rate, they disappear.

- **[237] Timer block**
  - These blocks are normlly replaced with a dashed outline without collision.  Upon collecting a timer item, they temporarily appear and become solid.

- **[238] Timer item**
  - Upon collecting this, timer blocks are temporarily made solid.  The time can be controlled by placing a type modifier event above it (5000+).

- **[160] Boss gate**
  - This block becomes solid when boss mode is activated, and disappears afterwards.

- **[108] Rainbow Crystal gate**
  - This block is solid until defeating the Rainbow Crystal boss.

- **[110] Pandora gate**
  - This block is solid until defeating Pandora. If Pandora is defeated on the same screen, this block remains solid until leaving the screen.

- **[455] Keke Bunny gate**
  - This block disappears and re-appears during certain attacks used by Keke Bunny.

- **[197] Spikes**
  - Touching this event damages Erina. Damage varies based on background and difficulty level.
  - Does not need to be on a solid tile to deal damage.

- **[109] Ignore spikes**
  - Allows Erina to touch certain sides of a spike tile without taking damage. Place around spike tiles as needed. Example:
  
    ![paintdotnet_2017-09-10_01-43-46](https://user-images.githubusercontent.com/19506837/30246488-82aa2c2c-95c9-11e7-9d5d-d9fcd978ac52.png)

- **[512 .. 515] Hall of Memories DLC area color blocks (red/blue/green/purple)**
  - Defeating the corresponding miniboss breaks these blocks.
  - How to use it as a switch/door: Let's take event ID 512 for example. (same applies for 513, 514, 515)
    - Touching an event ID 512 tile while the flag EV_NOEVENT1 is on (event 525) instantly breaks all blocks with event ID 512 on it.
    - Touching an event ID 512 tile while the flag EV_NOEVENT2 is on (event 526) will only cause event ID 512 blocks to return after a map transition or autosave reload.
    - In a sense, event ID 512 is used for both the "switch" and the "door"

  - *Note: This does not only work for 512 .. 515. The following event IDs can also be used as blocks:*
  ```
  512 - EV_MEMORYRED
  513 - EV_MEMORYBLUE
  514 - EV_MEMORYGREEN
  515 - EV_MEMORYPURPLE

  451 - EV_PLURKMIDBOSS
  453 - EV_PLURKTAKO2
  455 - EV_PLURKBLOCK
  441 - EV_AFTERRED3

  464 - EV_SAYAEX
  496 - EV_HW
  487 - EV_HILLENTER

  works in reverse:
  434 - EV_VOIDBLOCK
  446 - EV_LIBBLOCK
  ```
  (Some of these events only work if the DLC is installed)

# Trigger events

Events you typically place in a column or surrounding the entrance to an area, so that Erina has to pass through them to trigger something.

- See [music_ids_and_triggers.csv](music_ids_and_triggers.csv) for a list of music triggers.
  - Walking past a music trigger event changes the currently playing music.

- **[42] Auto save**
  - When Erina passes this event, the game triggers an autosave.  Autosave is then disabled until Erina passes an autosave reset event.

- **[44] Auto save reset**
  - When Erina passes this event, auto save events are reenabled.

- **[100] Dark Zone**
  - When Erina passes this event, darkness is activated. (you can't see without the Light Orb)

- **[101] No Dark Zone**
  - When Erina passes this event, darkness is disabled.

- **[193] Hide layer 2**
  - Makes layer 2 and 6 invisible.

- **[194] Show layer 2**
  - Makes layer 2 and 6 visible.


# Warps

Events that move Erina to a different location. More types of warps can be found in [map_transitions_and_warps.md](map_transitions_and_warps.md).

- **[80] Door (warp upwards)**
- **[81] Door (warp downwards)**
  - Doors are created simply by placing event 80 or 81 just above the floor.
  - Doors will warp the player exactly two screens upwards (event 80) or downwards (event 81).

- **[483] Take fall damage and reset**
  - Passing through this tile causes Erina to take damage and be warped to where she came from (as seen in the Ravine DLC area).
