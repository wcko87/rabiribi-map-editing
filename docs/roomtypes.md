# Room Types
Room Types (in the `roomtype` object layer) affect how the camera scrolls. This is used to create long or large rooms that span multiple minimap tiles in the game.

### Room types:
```
0: unused room. will be automatically to set to -1 if above a positive-valued room
1: single room, no scroll
2: horizontal room
3: vertical room
4: free camera room (can be used for horizontal, vertical, or open room)
5: map transition room (draws an arrow in the minimap, connects with horizontal rooms)
-1: Prevents the camera from entering a room from above or below (it can still enter from the sides)
-2: Prevents the camera from entering a room from the left or right (it can still enter from above/below)
-3: Prevents the camera from entering a room from any direction.
```
