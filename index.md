# Rabi-Ribi Map Editor

Brought to you by the [Rabi-Ribi Speedrunning Community](http://www.speedrun.com/rabiribi).

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://discord.gg/dDfpNAr"><img src="https://discordapp.com/assets/f8389ca1a741a115313bede9ac02e2c0.svg" height="20" />Rabi-Ribi Speedrunning Discord</a>

# How to edit rabi ribi maps:
### Downloads
Download the following:
1. The [Rabi-Ribi Map Converter](https://ci.appveyor.com/project/wcko87/rbrb-map-converter/build/artifacts)
2. These [Tileset files](https://cdn.discordapp.com/attachments/304270436911284224/353697835788664832/rabiribi-tilesets.zip)
3. The [Tiled map editor](http://www.mapeditor.org/)

![mapedit](https://user-images.githubusercontent.com/27341392/30008514-fea9b4f8-9152-11e7-9e5d-1bf9959714f6.png)

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

2. Don't ever put collision tiles in the tile layers (layer0 to layer6) or graphical tiles in the collision layer. I have no idea what happens if you do, and it probably won't be good.

3. To create events and items, use the "rectangle" tool to create a 1-tile box where the event should be, and name the tile with the eventid. (the name can be set on the properties panel on the left). If done correctly, the event id should show up above the tile

4. Do not name an event or tileid something that is not a number. it will cause the converter to crash

5. Please turn on [**view -> snapping -> Snap to Grid**](https://user-images.githubusercontent.com/27341392/30008566-5d1a0a60-9153-11e7-81cf-0d874c735f5c.png) (otherwise the events/items can be placed in floating positions, which will be awkward and doesn't actually convert properly)

6. Minimap data layers (roomcolor, roomtype, roombg) are hidden by default. click the eye icon next to the layers to toggle on their visibility. they work similar to events/items. set their names to other integers to change their values.

7. Do not delete/move/insert any objects in the minimap data layers. Only change their names.

8. You can re-order the layers in the editor for viewing convenience, they will not affect anything. but do not rename the layers.(edited)

9. Don't mess with map settings like map size etc

10. Press X to flip a tile by the x-axis, Y to flip by the y-axis. Do not rotate tiles. Do not flip collision tiles.

# Understanding Events, Item Ids, Minimap tiles

When you first open up the map editor, you might notice a lot of numbers.

![mapeditor](https://user-images.githubusercontent.com/27341392/30008300-b79449c2-9150-11e7-8425-54c32eba09d3.png)

These numbers belong to Object layers. There are [five object layers](https://user-images.githubusercontent.com/27341392/30008490-cf24761e-9152-11e7-94d2-955ab89621a7.png).
* `events`: Event Triggers. Most of the things that "happen" in game come from event tiles.

  Events include, but is not limited to:
  * Cutscene Start Triggers
  * Boss Triggers
  * Music Triggers
  * Enemies, and other entities like springs, computers etc.
  * Easter Eggs
  * Save points, heal points, warp stones
  * Bomb blocks, Hammer blocks, ribbon blocks
  * Map transitions
  * Environmental lighting effects
  * etc etc etc...
* `items`: Item ids. Only items exist in this layer.
* `roombg`: The background for each room
* `roomcolor`: The color of the minimap tile for the room
* `roomtype`: Determines if the room is a single room, or a vertical/horizontal/large room, for camera scrolling.

More detailed information on these layers can be found in the [Detailed Documentation](https://github.com/wcko87/rabiribi-map-editing/tree/master/docs).

# Frequently Asked Questions

##### Q: When I load a map in Tiled, I can't see any tiles at all! All I see are a bunch of numbers.

A: This happens when you don't put the tileset files in the same directory as the .json file. If your .json file is in `s2_editable_maps`, you should place the tileset files in `s2_editable_maps` as well.

##### Q: I get a conversion error when I try to convert my .json map back into a .map file. What happened?

A: A conversion error happens when you do something in Tiled that is not valid in Rabi-Ribi. I suggest reading the [Important Notes when working with the Map Editor](#important-notes-when-working-with-the-map-editor) to find out what you should and should not do in Tiled.

# Other Stuff

### Demo

[**Random Map Editor Images!**](random_images)

<iframe id="introvideo" width="400" style="object-fit:cover" id="ytplayer" type="text/html" src="https://www.youtube.com/embed/fT418LWsdc4?rel=0&autoplay=0&showinfo=1"></iframe>

### Custom Maps

We have a custom maps portal for user-created Rabi-Ribi maps.

[**Custom Maps Portal**](https://wcko87.github.io/rabi-ribi-maps/)

### Contact

For any queries, look for me (wcko87) on either [Twitter](https://twitter.com/wcko87), [YouTube](https://www.youtube.com/user/wcko87), [Twitch](https://www.twitch.tv/wcko87) or in the [Rabi-Ribi Speedrunning Discord](https://discord.gg/dDfpNAr).
