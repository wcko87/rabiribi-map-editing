# Using the Tiled Map Editor for Rabi-Ribi

## Important Notes!
 
**Please read all of the following points carefully before getting started!**

Tiled is a pretty flexible map editor, and can do a lot of things not accepted by the Rabi-Ribi game.
Using the editor in the wrong way can cause either the converter to crash, or the map files to not work as expected.

1. If you are deleting tiles, don't use the blank tiles in the tileset. actually erase them properly with the erase tool (E)

2. Don't ever put collision tiles in the tile layers (tile0 to tile6) or graphical tiles in the collision layer. I have no idea what happens if you do, and it probably won't be good.

3. To create events and items, use the "rectangle" tool to create a 1-tile box where the event should be, and name the tile with the Event ID. (the name can be set on the properties panel on the left). If done correctly, the event id should show up above the tile.

4. Do not name an event or tileid something that is not a number. It will cause the converter to crash.

5. Make sure you turn on [**View -> Snapping -> Snap to Grid**](https://user-images.githubusercontent.com/27341392/30008566-5d1a0a60-9153-11e7-81cf-0d874c735f5c.png) (otherwise the events/items can be placed in floating positions, which will cause problems in conversion.)

6. Minimap data layers (roomcolor, roomtype, roombg) are hidden by default. click the eye icon next to the layers to toggle on their visibility. they work similar to events/items. Set their names to other numbers to change their values.

7. Do not delete/move/insert any objects in the minimap data layers. Only change their names.

8. You can re-order the layers in the editor for viewing convenience, they will not affect anything. but do not rename the layers.(edited)

9. Don't mess with map settings like map size.

10. Press X to flip a tile by the x-axis, Y to flip by the y-axis. Do not rotate tiles. Do not flip collision tiles.


# Quick Start Guide

When you open a map in Tiled, you should see something like this.

![expecttosee](https://user-images.githubusercontent.com/27341392/30276609-f61fd322-9737-11e7-82cf-f70c570e5af9.png)

The map data is stored in layers. The layer panel is on the right, and looks like the below image:

![layers](https://user-images.githubusercontent.com/27341392/30008490-cf24761e-9152-11e7-94d2-955ab89621a7.png)

**Note: You can re-order the layers in the menu, and hide/unhide layers. But do not rename any of the layers. Renaming the layers will cause the map conversion to fail.**

### Adding Tiles

There are 7 tile layers, `tiles0` to `tiles6`. These layers store tile data you can see in-game. The main layer you should be adding tiles to is `tiles1`. More details on the layers can be found in the detailed docs.

Here we take tiles from the tileset and add them to the `tiles1` layer.

![editor_adding_tiles](https://user-images.githubusercontent.com/27341392/30276612-f9f1f23c-9737-11e7-9df0-85c9e8b8c24a.png)

### Adding Collision

Tile layers are purely visual. For Erina to collide with the floor, you need to add collision tiles to the `collision` layer. **Note: Do not add collision data to tile layers, or tile data to the collision layer**.

![editor_adding_collision](https://user-images.githubusercontent.com/27341392/30276606-f5d4d1f6-9737-11e7-8a4a-86fff8f02dca.png)

### Adding Items

Before we add items and events, make sure **View -> Snapping -> Snap to Grid** is turned on, like in the image below:

![snap to grid](https://user-images.githubusercontent.com/27341392/30008566-5d1a0a60-9153-11e7-81cf-0d874c735f5c.png)

If Snap to Grid is not on, there will be conversion errors later.

To add items, we switch to the `items` object layer. To create a new item, use the *Rectangle* tool to create a 1-tile rectangle. Name the rectangle with the Item ID of the item you want. A list of Item IDs can be found in the detailed documentation.

Alternatively, you can copy-paste an existing item object and simply change the name.

![editor_adding_items](https://user-images.githubusercontent.com/27341392/30276607-f5d61c46-9737-11e7-8f8a-b285747bf04b.png)

### Adding Events

Almost everything else in the game is an event. More details on events will be explained later. To add an event, we switch to the `event` object layer. Create events the same way you create items.

In the following image, we create a "Start Point" event (event id 34), and a column of autosave events. (42 is an autosave event, and 44 is a no-save event, which allows autosave events to be triggered again)

![editor_adding_events](https://user-images.githubusercontent.com/27341392/30276605-f5ced0da-9737-11e7-8bea-c267c124e782.png)

### Editing Room Data

Finally, you can also edit room types, room colors and room backgrounds. The most important of the three is room types. Room types affect how the camera scrolls in the rooms.

In this case, we want to turn these rooms into a single long room. We do this going to the `roomtype` layer, selecting the rooms we want to change, and change the names of these objects to "2". Room type 2 represents long horizontal rooms. More information on room types can be found in the detailed docs.

**Note: Do not delete any objects in the `roombg`, `roomcolor` or `roomtype` layers. You should only change the names of the objects.**

![editor_roomtype](https://user-images.githubusercontent.com/27341392/30276604-f59e4370-9737-11e7-9274-5cb74c175e21.png)

The following section will explain more about Object Layers (events, items, roombg, roomcolor, roomtype).

# Understanding Object Layers

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

