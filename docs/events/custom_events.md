# Custom Events

These are events defined by GemaYue specifically for the map editor. These events only work in the beta version 1.8e.

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
    - m is the value of the X+1 tile (i.e. ID 5000+m)
    - n is the value of the X+2 tile (i.e. ID 5000+n)


- **533 EV_NOSPAWN0**

    Disables the effect of EV_NOSPAWN1 534 and EV_NOSPAWN2 535

- **534 EV_NOSPAWN1**

    If Erina passes this event, disable any entities from respawning.

- **535 EV_NOSPAWN2**

    If Erina passes this event, replace any future spawned entity with entity ID k
    - k is the value of the X+1 tile + 1000 (i.e. ID 5000 + k - 1000).
    - (for example, for entity ID 1096, the value of the X+1 tile is 5096)


- **536 EV_GAMESPEED**

    If Erina passes this event, change the game speed to k.
    - k is the value of the X+1 tile (i.e. ID 5000+k)
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
    - k is the value of the X+1 tile (i.e. ID 5000+k)


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
    - k is the value of the X+1 tile (i.e. ID 5000 + k).
    
- **552 EV_FULLAP**

   If Erina passes this event, see amulet charge to full.

- **553 EV_FULLBPMP**

   If Erina passes this event, see Ribbon boost and mp to full.
