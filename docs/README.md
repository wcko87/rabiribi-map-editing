# Detailed Documentation

[Rabi-Ribi Map Editing Main Page](https://wcko87.github.io/rabiribi-map-editing/)

This is the detailed documentation for some of the more technical aspects of map editing (especially events). It's a little messy around here.

Basically we store id tables miscellaneous notes around here. Click around the various files in this directory to look through them.

## Event Basics:

How to use events
* Suppose you want to place a certain type of event (e.g. a heal point)
* First, remember the location of a known heal point (e.g. the big flower near aruraune)
* Then open up the corresponding map and go to that location and note down the event id.
* Place that event id in the map to get a heal point.

For some of the more technical events, some information may be found in the [events directory](./events)

## Item Basics:

The [table of item ids](./items/item_ids.csv) can be found in the detailed docs.

Note: In custom maps, picking up the Congratulations! trophy (item id 42) will display the time and end the game.

## Room Background/Type/Color Basics:

To modify these, make the corresponding layers visible and modify the name labels of the room tiles overlaid over the map.

* Room colors and background ids can be found from these text files:
  * [room_colors_original.txt](./room_colors_original.txt)
  * [room_background_ids_original.txt](./room_background_ids_original.txt)
  * Basically, these text files list the color/background being used in the original maps.
  
* Images of each of the backgrounds can be found [here](./room_background_images.md)
* Room type information can be found [here](./roomtypes.md)

Note: you may need to restart the game for changes in room backgrounds/types/colors to take effect properly.
