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

