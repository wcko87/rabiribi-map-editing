# Rabi-Ribi Custom Maps

User-created Rabi-Ribi Maps can be found here:
- [**Custom Maps Portal**](https://wcko87.github.io/rabi-ribi-maps/)

# Rabi-Ribi Map Editor

This is not the work of one person. It is a collaborative effort of the [Rabi-Ribi Speedrunning Community](http://www.speedrun.com/rabiribi).
- [How the Map Editor came about](https://wcko87.github.io/acknowledgements/)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="https://discord.gg/dDfpNAr"><img src="https://discordapp.com/assets/f8389ca1a741a115313bede9ac02e2c0.svg" height="20" />Rabi-Ribi Speedrunning Discord</a>

# How to edit Rabi-Ribi maps

## Downloads

Download the following:
1. The [Rabi-Ribi Map Converter](https://ci.appveyor.com/project/wcko87/rbrb-map-converter/build/artifacts)
2. These [Tileset files](https://github.com/wcko87/rabiribi-map-editing/files/1283420/rabiribi-tilesets.zip)
3. The [Tiled map editor](http://www.mapeditor.org/)

![mapedit](https://user-images.githubusercontent.com/27341392/30008514-fea9b4f8-9152-11e7-9e5d-1bf9959714f6.png)

## How to use

Rabi-Ribi maps have the extension `.map`. Normally, these maps are found in `Rabi-Ribi/data/area` in your steam directory. We will explain how to modify the maps in this directory.

We use the Rabi-Ribi Map Converter to convert between the `.map` file format, which is used by Rabi-Ribi, and the `.json` file format, which is used by the Tiled Map Editor.

After downloading the Rabi-Ribi Map Converter, unzip it into any location you want.

In the rabiribi map converter directory, there are three folders:
1. `s1_original_maps`
2. `s2_editable_maps`
3. `s3_final_maps`

How it works:

- Copy the original Rabi-Ribi maps from `Rabi-Ribi/data/area` to `s1_original_maps`. These maps will never be modified by the converter.

- Double-clicking `original_to_editable.bat` will take all the maps in `s1_original_maps`, convert them to `.json` file format maps, and place them in `s2_editable_maps`.

- You can open these `.json` file format maps in `s2_editable_maps` in the Tiled Map Editor.

- Double-clicking `editable_to_final.bat` will take all the maps in `s2_editable_maps`, convert them back to Rabi-Ribi maps, and place them in `s3_final_maps`.

- You can copy these `s3_final_maps` back into Rabi-Ribi to try them out. (maps are placed in the `Rabi-Ribi\data\area` folder in your steam directory)

### NOTE: The Tileset files MUST be placed in the same directory as the .json files for the map editor to display correctly!
- I suggest placing the Tileset files in `s2_editable_maps`

<img class='gfyitem' data-id='MadeupNippyHamster'/>

# Guides

The following guides will help you get started with map editing.

### [Running Custom Maps](runningcustommaps)

### [Getting Started with the Editor](editorguide)

### [Detailed Documentation](https://github.com/wcko87/rabiribi-map-editing/tree/master/docs/)



# Frequently Asked Questions

#### Q: When I load a map in Tiled, I can't see any tiles at all! All I see are a bunch of numbers.

A: This happens when you don't put the tileset files in the same directory as the .json file. If your .json file is in `s2_editable_maps`, you should place the tileset files in `s2_editable_maps` as well.

#### Q: I get a conversion error when I try to convert my .json map back into a .map file. What happened?

A: A conversion error happens when you do something in Tiled that is not valid in Rabi-Ribi. I suggest reading the [Important Notes when working with the Map Editor](editorguide#important-notes) to find out what you should and should not do in Tiled.



# Other Stuff

### Demo

[**Random Map Editor Images!**](random_images)

<iframe id="introvideo" width="400" height="225" style="object-fit:cover" id="ytplayer" type="text/html" src="https://www.youtube.com/embed/fT418LWsdc4?rel=0&autoplay=0&showinfo=1"></iframe>

### Rabi-Ribi Custom Maps Portal

We have a custom maps portal for user-created Rabi-Ribi maps.
- [**Custom Maps Portal**](https://wcko87.github.io/rabi-ribi-maps/)

### Rabi-Ribi Live Memory Map Editor

This Live Map Editor is an alternative map editor for Rabi-Ribi. It can be used to edit the maps by setting the map tiles in-game.
- [**Live Memory Map Editor**](https://github.com/D3nD3nD3n/rbrb-Map-Viewer)

### Rabi-Ribi Randomizer

Rabi-Ribi also has a Randomizer, also brought to you by the Speedrunning Community.
- [**Rabi-Ribi Randomizer Website**](https://wcko87.github.io/rabiribi-randomizer/)

### Contact

For any queries, look for me (wcko87) on either [Twitter](https://twitter.com/wcko87), [YouTube](https://www.youtube.com/user/wcko87), [Twitch](https://www.twitch.tv/wcko87) or in the [Rabi-Ribi Speedrunning Discord](https://discord.gg/dDfpNAr).
