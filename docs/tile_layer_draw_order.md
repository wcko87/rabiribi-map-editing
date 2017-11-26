# Tile Layer Draw Order

Layer 1 is the "main" layer. Most of the map geometry should be placed in layer 1.

The tile layers (layer 0 to 6) are drawn in this order:

(with layer 0 being the furthest in the back and layer 2 at the front)
```
Layer 0
Eggs
Layer 3
Layer 4
Layer 1
Layer 5
Items
Erina
Layer 6
Layer 2
```

Both layers 2 and 6 are hidden by the "hide layer 2" event.

![draw_layers](https://user-images.githubusercontent.com/27341392/33240322-41c51254-d2ef-11e7-9b80-999c2440468a.png)
