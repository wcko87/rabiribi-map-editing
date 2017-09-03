# Rabi-Ribi Map Editor

Brought to you by the [Rabi-Ribi Speedrunning Community](http://www.speedrun.com/rabiribi).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://discord.gg/dDfpNAr"><img src="https://discordapp.com/assets/f8389ca1a741a115313bede9ac02e2c0.svg" height="20" />Rabi-Ribi Speedrunning Discord</a>

## How to edit rabi ribi maps:
### Downloads
Download the following:
1. The [Rabi-Ribi Map Converter](https://ci.appveyor.com/project/wcko87/rbrb-map-converter/build/artifacts)
2. These [tileset files](https://cdn.discordapp.com/attachments/304270436911284224/353697835788664832/rabiribi-tilesets.zip)
3. The [Tiled map editor](http://www.mapeditor.org/)

### How to use
In the rabiribi map converter directory, there are three folders:
1. `s1_original_maps`
2. `s2_editable_maps`
3. `s3_final_maps`

Place the original Rabi-Ribi maps in `s1_original_maps`. These maps will never be modified by the converter.
- Double-clicking `original-to-editable.bat` will take all the maps in `s1_original_maps`, convert them to `.json` file format maps, and place them in `s2_editable_maps`.
- You can open the `.json` file format maps in the tiled map editor, as long as the **tileset files are also placed in the same directory as the `.json` files**.
- Double-clicking `editable_to_final.bat` will take all the maps in `s2_editable_maps`, convert them back to rabi ribi maps, and place them in `s3_final_maps`.
- You can copy these `s3_final_maps` back into Rabi-Ribi to try them out. (maps are placed in the `Rabi-Ribi\data\area` folder in your steam directory)


### Important Notes when working with the Map Editor
 
Please read all of the following points carefully before getting started.
Tiled is a pretty flexible map editor, and can do a lot of things not accepted by the Rabi-Ribi game.
Using the editor in the wrong way can cause either the converter to crash, or the map files to not work as expected.

1. If you are deleting tiles, don't use the blank tiles in the tileset. actually erase them properly with the erase tool (E)

2. Don't ever put collision tiles in the tile arrays or tile tiles (lol) in the collision array. I have no idea what happens if you do, and it probably won't be good
(tile tiles refers to the stuff you see, collision tiles refer to map collision hitboxes)

3. To create events and items, use the "rectangle" tool to create a 1-tile box where the event should be, and name the tile with the eventid. (the name can be set on the properties panel on the left). If done correctly, the event id should show up above the tile

4. Do not name an event or tileid something that is not a number. it will cause the converter to crash

5. Please turn on **view -> snapping -> Snap to Grid** (otherwise the events/items can be placed in floating positions, which will be awkward and doesn't actually convert properly)

6. Minimap data layers (roomcolor, roomtype, roombg) are hidden by default. click the eye icon next to the layers to toggle on their visibility. they work similar to events/items. set their names to other integers to change their values.

7. Do not delete/move/insert any objects in the minimap data layers. Only change their names.

8. You can re-order the layers in the editor for viewing convenience, they will not affect anything. but do not rename the layers.(edited)

9. Don't mess with map settings like map size etc

10. Press X to flip a tile by the x-axis, Y to flip by the y-axis. Do not rotate tiles. Do not flip collision tiles.

### Demo

<iframe width="560" height="420" src="http://www.youtube.com/embed/fT418LWsdc4?color=white&theme=light"></iframe>

### Custom Maps Portal

https://wcko87.github.io/rabi-ribi-maps/

### Contact

For any queries, look for me (wcko87) on either [Twitter](https://twitter.com/wcko87), [YouTube](https://www.youtube.com/user/wcko87), [Twitch](https://www.twitch.tv/wcko87) or in the [Rabi-Ribi Speedrunning Discord](https://discord.gg/dDfpNAr).
