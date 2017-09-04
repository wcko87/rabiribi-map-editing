# Events - Water

There are 4 water related events:
```
102: No Water
103: Water
104: Water -Lv-
105: Water Up Ver
```

When Erina touches 103 Water, the game will search straight downward from that event for a 104 Water -Lv- event, and set the water level to that height. If there are multiple water level events directly below, the water level will be set to the highest one. If there are no water level events directly below, it will essentially turn off the water.

When Erina touches 105 Water Up Ver, the game will search straight upward from that event for a 104 Water -Lv- event, and set the water level to that height. If there are multiple water level events directly above, the water level will be set to the lowest one. If there are no water level events directly above, it will fill the entire map with water.

When Erina touches 102 No Water, the water is removed.

Video: [water.mp4](https://cdn.discordapp.com/attachments/304270436911284224/348209420460752896/water.mp4)

Event Layout corresponding to video:

![water](https://cdn.discordapp.com/attachments/304270436911284224/348209462483615766/water.png)
