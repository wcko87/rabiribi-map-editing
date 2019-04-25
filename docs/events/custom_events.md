# Custom Events

These are events defined by GemaYue specifically for the map editor. These events only work in the beta version 1.8e or 1.85 onwards.

**Note:** If there are no modifier events (5000+) at position X+1 (1 tile right of the custom event), the custom events will then search upward for modifier events instead (Y-1 instead of X+1, Y-2 instead of X+2, etc.)

- **522 EV_NOPFLAG0**

    Disables effect of EV_NOPFLAG1 523

- **523 EV_NOPFLAG1**

    If Erina passes this event, other event tile will always trigger even if the required flag(s) are not set.

- **524 EV_NOEVENT0**

    Disable effect of  EVE_NOEVENT1 525 and EV_NOEVENT2 526

- **525 EV_NOEVENT1**

    If Erina passes this event, other event tiles will just set the event flag instead of starting the event.

- **526 EV_NOEVENT2**

    If Erina passes this event, other event tiles will just unset the event flag instead of starting the event.


- **527 EV_ITEMGETLV1**
- **528 EV_ITEMGETLV2**
- **529 EV_ITEMGETLV3**
- **530 EV_ITEMGETLV4**

    If Erina passes these events, it changes the levels of all uncollected items on the map.


- **531 EV_RESETFLAG**

    If Erina passes this event, it sets all event flags to 0.

- **532 EV_GIVESTATUS**

    If Erina passes this event, it gives her buff ID m for n seconds.
    - m is the value of the X+1 tile (i.e. eventID: 5000 + m)
    - n is the value of the X+2 tile (i.e. eventID: 5000 + n)
    - A list of buff IDs can be found in [buff_ids.csv](./buff_ids.csv)
    - n can be set to 0 to make this event remove the buff.


- **533 EV_NOSPAWN0**

    Disables the effect of EV_NOSPAWN1 534 and EV_NOSPAWN2 535

- **534 EV_NOSPAWN1**

    If Erina passes this event, disable any entities from respawning.

- **535 EV_NOSPAWN2**

    If Erina passes this event, replace any future spawned entity with entity ID k
    - k is the value of the X+1 tile + 1000 (i.e. eventID: 5000 + k - 1000).
    - (for example, for entity ID 1096, the value of the X+1 tile is 5096)


- **536 EV_GAMESPEED**

    If Erina passes this event, change the game speed to k.
    - k is the value of the X+1 tile (i.e. eventID: 5000 + k)
    - If k=1, then 1x speed. If k=2, 2x speed, and so on.
    - If k>100, the game slows down instead


- **537 EV_STORYMODE**
- **538 EV_SPEEDRUN**
- **539 EV_STANDARD**
- **540 EV_ALTERNATIVE**
- **541 EV_BUNNYHEAVEN**
- **542 EV_BUNNYHELL**

    If Erina passes these events, change game mode / rule


- **543 EV_SETDIFFICULTY**

    If Erina passes this event, change game difficulty to k.
    - k is the value of the X+1 tile (i.e. eventID: 5000+k)
    ```
    5000: Casual
    5001: Novice
    5002: Normal
    5003: Hard
    5004: Hell
    5005: Bunny Extinction
    5006: Unknown
    5007: Impossible
    5008+: Extra
    ```


- **544 EV_BOSSMODE**

    If Erina passes this event, force boss mode to true.

- **545 EV_NOBOSSMODE**

    If Erina passes this event, disable boss mode and remove screen scroll lock.

- **546 EV_NOBOSSMODE2**
    
    If Erina passed this event, remove screen scroll lock.


- **547 EV_DISABLEEVENT0**
    
    Disable effect of EV_DISABLEEVENT1 548

- **548 EV_DISABLEEVENT1**
    
    If Erina passed this event, disable any event start (to prevent event  that unrelated to event tile 
    from starting, for example Cicini's dialog after Erina pick up Air Jump) 

- **549 EV_NOENDBOSSEVENT0**
    
    disable the effect of EV_NOENDBOSSEVENT1 550

- **550 EV_NOENDBOSSEVENT1**
    
    If Erina passed this event, any town member boss will just teleport and leave after defeated by Erina. 
    Instead of using the end boss cutscene. 

- **551 EV_SETMUSICSPEED**
    
    IF Erina passed these events, change music speed to k%.
    - k is the value of the X+1 tile (i.e. eventID: 5000 + k).
    - Music speed for each sound test icon:
    ```
    Halloween:      38.5 %
    Instant Death:  50.0 %
    Chaos Rod:      66.7 %
    Giant:          85.0 %
    No water orb:   90.0 %
    Default:       100.0 %
    Speed Up:      112.5 %
    Shrink:        120.0 %
    Miru:          130.0 %
    Cocoa Bomb:    150.0 %
    Boss defeat:   170.0 %
    ```
    
- **552 EV_FULLAP**

   If Erina passes this event, see amulet charge to full.

- **553 EV_FULLBPMP**

   If Erina passes this event, see Ribbon boost and mp to full.

- **554 EV_MOVEDOWN**

    if Erina passes this event, start a event that increase Erina's yaxis position by 720x4px. (i.e. move 4 screens down)
    - this event is repeatable
    - if the game can't move the player 4 screens down, this event does nothing.
    - the screen fades out and fades back in like a map transition. Erina has time to fall about 4 screens during the transition cutscene.

- **555 EV_MOVEUP**

    if Erina passes this event, start a event that decrease Erina's yaxis position by 720x4px. (i.e. move 4 screens up)
    - this event is repeatable.
    - if the game can't move the player 4 screens up, this event does nothing.
    - the screen fades out and fades back in like a map transition. Erina has time to fall about 4 screens during the transition cutscene.
    - **warning**: If there is nothing for erina to fall on after transitioning 4 screens up, she falls back onto the event before the transition cutscene ends, softlocking the game.

- **556 EV_SETSPIKEDMG**

    IF Erina passes this event, set all spikes damage to k.
    - k is the value of the X+1 tile. (i.e. eventID: 5000 + k)
    - If k = 0, disable this effect.

- **557 EV_PLAYMUSIC**

    IF Erina passes this event, play music ID k. (useful for playing music with ID>31)
    - k is the value of the X+1 tile. (i.e. eventID: 5000 + k)

- **558 EV_CHANGEITEM**

    IF Erina passes this event, set item ID k's Level to n. 
    - k is the value of the X+1 tile. (i.e. eventID: 5000 + k)
    - n is the value of the X+2 tile. (i.e. eventID: 5000 + n)
    - (If n is 0, remove the item)
    - This can be used to set the levels of plus necklace(23), bunny amulet(33), donuts(37), cakes(38), golden carrots(39), and cocoa bombs(40) above their normal values.
    
- **559 EV_SETHAMMEREXP**
    
    IF Erina passes this event, set hammer exp to k.
    - k is the value of the X+1 tile * 100 (i.e. eventID: 5000 + k/100)

- **560 EV_SETFAIRYEXP**
    
    IF Erina passes this event, set Ribbon relationship exp to k.
    - k is the value of the X+1 tile * 100 (i.e. eventID: 5000 + k/100)

- **561 EV_SETBOMBEXP**
    
    IF Erina passes this event, set carrot bomb exp to k.
    - k is the value of the X+1 tile * 100 (i.e. eventID: 5000 + k/100)
    
- **562 EV_SETUPWIND0**
    
    IF Erina passes this event, turn off upward wind (status will not save to save file)

- **563 EV_SETUPWIND1**

    IF Erina passes this event, turn on upward wind (status will not save to save file)
    - Upward wind is the effect during the Pixie & Lilli boss fight
    
- **564 EV_CHANGECHARACTER**

    IF Erina passes this event, her sprite turns into that of entity N, where N is value of modifier.
    Modifier is 5000 + N and has to be set in the X+1 tile.
    e.g. Erina turns into Cicini when passing through a 564 event with 5018 modifier next to it. (18 being Cicini ID).
    IF no modifier is set, Erina will turn back to Erina again when crossing event 564.
    
- **565 EV_CUSTOMTEXT**

    Displays custom text LINE N at this tile where N is value of modifier. Modifier is 5000 + N and has to be set in the X+1 tile. Custom text is stored in story_text.rbrb (a rbrb file start at line0, not 1).
    e.g. To display dialogue line 10 from story_text.rbrb you need event 565 and modifier 5009 next to it.
      
- **573 EV_EGGBLOCK**
    
    This event has to be attached to a collision tile. The block breaks if egg collected >= N, Where N is value of modifier (For example, 5005 mean need 5 egg to break).
    
- **574 EV_EVENTBLOCK**

    This event has to be attached to a collision tile. The block breaks if event N is flagged, Where N is value of modifier (for example Cocoa1 Battle is 256, so modifier is 5256)

- **575 EV_EVENTBLOCKR**

    This event has to be attached to a collision tile. The block spawns if event N is flagged, where N is value of modifier (for example Cocoa1 Battle is 256, so modifier is 5256).
    
- **576 EV_TRIGGERBLOCK1**
- **577 EV_TRIGGERBLOCK2**
- **578 EV_TRIGGERBLOCK3**
- **579 EV_TRIGGERBLOCK4**
- **580 EV_TRIGGERBLOCK5**

    These events have to be attached to collision tiles. They are similar to DLC 2 blocks in Hall of Mmemories II (events 512 to 515) except they work outside of DLCs. They work as switch and doors.
    They break if event N is not flagged, Where N is this event id.
    e.g. To break a block which has collision and event 576 attached, Erina needs to pass through a 576 event.

- **581 EV_TRIGGERBLOCKR1**
- **582 EV_TRIGGERBLOCKR2**
- **583 EV_TRIGGERBLOCKR3**
- **584 EV_TRIGGERBLOCKR4**
- **585 EV_TRIGGERBLOCKR5**

    These events work in reverse. They spawn if event N is flagged, where N is this event id.
    e.g. To make a block which has collision and event 581 attached appear, Erina needs to pass through a 581 event.
