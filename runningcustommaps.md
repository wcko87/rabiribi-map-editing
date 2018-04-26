# How to play Custom Rabi-Ribi Maps

([Alternative guide by NuclearCheese for running Custom Maps](http://steamcommunity.com/sharedfiles/filedetails/?id=1170578077))

1. Create custom map folder `Rabi-Ribi\custom\<your map name>`
2. Add map files (`area0.map`,`area1.map` etc etc) to the custom map folder (`Rabi-Ribi\custom\<your map name>`)
3. In Rabi-Ribi, press **F5** or **F6** to open the [custom maps menu](https://user-images.githubusercontent.com/27341392/30108930-ee520480-9336-11e7-9a82-bf40ca1ae89e.png). Select the custom map and start a new game.

![instructions_custom_maps](https://user-images.githubusercontent.com/27341392/39337459-aa31db66-49ef-11e8-9663-5c0c4c9f19e5.png)

(You need Rabi-Ribi v1.8e / v1.85 or higher for the custom maps menu. The custom maps menu does not exist for v1.8 and below.)

### Alternate Method: Replacing maps (not recommended)
This was the original method before the 1.8e beta / 1.85 started supprting custom maps.
1. Replace the maps in `Rabi-Ribi\data\area\` (remember to back up the maps before you do this)
2. Start up Rabi-Ribi and start a new game normally.

Note: Even if you do not back up your maps, you can easily restore your original maps by using the Verify Game Integrity option on steam.

# Modifying Character Dialogue and Cutscenes

Rabi-Ribi (1.8e/1.85 onwards) includes the ability to modify cutscenes and character dialogue for custom maps. By default, the game makes use of the files in `Rabi-Ribi\localize` for its cutscenes. If you create the files `story_emot.rbrb` and `story_text.rbrb` and place them in your custom map folder (`Rabi-Ribi\custom\<your map name>\`) together with your map, these ifles will be used for dialogue/cutscenes instead.

More information on the contents of these files can be found in the [Detailed Documentation](https://github.com/wcko87/rabiribi-map-editing/tree/master/docs/cutscenes).

# Custom Tilesets

Rabi-Ribi (1.8e/1.85 onwards) includes the ability to replace the current tileset with a custom tileset. If `tile1_a.png` is placed in the `Rabi-Ribi\custom\<your map name>\` folder, the game will use that instead of the default tileset.

# Debug Mode

Rabi-Ribi (1.8e/1.85 onwards) contains a Debug mode, which displays all event triggers in-game. To turn this on, add `-debugshowevents` to the launch options.
