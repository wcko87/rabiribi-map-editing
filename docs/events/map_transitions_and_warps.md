# Map Transitions

(Will document this at some point in the future)

# Warp Stones

Note: This refers to the warp stones which bring up the warp stone select menu. The warpstone at plurkwood/forest night is not included.

A warp stone event has ID `32`. Which warp stone it is is specified by a type specifier event (i.e. ID+5000) just above the warp stone.

For example, the town warp stone has ID 5. The warp stone event is thus laid out like this:

```
+----+
|5005|
|----|
| 32 |
+----+
```

Each warp stone in Rabi-Ribi has a different ID.


### How Warp Stones work
**Short explanation**: The map you warp to is hardcoded in game. The actual location within the map depends on warp stone placement in map. If the target warp stone does not exist, you still warp but stay on the same tile.

**Proper explanation using an example**:
- Lets say from some other warp stone, you select Spectral Cave as your warp destination.
- According to the game's code, Spectral Cave is located in area0.
- Thus the game checks area0 and looks for the Spectral Cave warp stone.
    - If it finds the Spectral Cave warp stone in area0, it puts you at the location of the warp stone.
    - If it can't find the Spectral Cave warp stone in area0, it warps you to area0 anyway, but in the same tile as you were in before. We refer to this as a wrong warp.
