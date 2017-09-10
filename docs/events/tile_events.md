# Tile modifier events

These are events that you typically place directly on tiles in order to add destructables to the map.

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

- **[160] Boss gate**
  - This block becomes solid when boss mode is activated, and disappears afterwards.

- **[108] Rainbow Crystal gate**
  - This block is solid until defeating the Rainbow Crystal boss.

- **[110] Pandora gate**
  - This block is solid until defeating Pandora. If Pandora is defeated on the same screen, this block remains solid until leaving the screen.

- **[197] Spikes**
  - Touching this event damages Erina. Damage varies based on background and difficulty level.
  - Does not need to be on a solid tile to deal damage.

- **[109] Ignore spikes**
  - Allows Erina to touch certain sides of a spike tile without taking damage. Place around spike tiles as needed. Example:
  
    ![paintdotnet_2017-09-10_01-43-46](https://user-images.githubusercontent.com/19506837/30246488-82aa2c2c-95c9-11e7-9d5d-d9fcd978ac52.png)
