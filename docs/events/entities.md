# Entities

Entities are generally objects you can interact with in-game. This includes things like:
- Enemies
- Bosses
- Springs / Computer Desks
- NPCs

## Entity IDs and Types
Each Entity has an Entity ID and a Type.

For example, a bunny enemy (the first enemy you see in starting forest) has entity ID 1096.
- Entity ID 1096 with Type 0 is a small bunny enemy.
- Entity ID 1096 with Type 5 is a big bunny enemy. (seen near Cocoa1's boss fight)
- Entity ID 1096 with type 6/7 are huge bunny enemies (seen in night forest)

## Entity Events
The Event ID that spawns an entity is the same as the entity ID itself. Because Entity IDs are in the 1000+ range, they do not conflict with other event types. Thus placing an event with ID 1096 on the map will spawn a small bunny there.

If you want an entity of type k, place a "type specifier" event above the entity. The type specifier event has an ID of 5000+k.

For example, to place a Type 5 Bunny on the map, you place an event with ID 1096, and an event with ID 5005 just above it.

```
+----+
|5005|
|----|
|1096|
+----+
```

If no type specifier event is used for the entity, the entity defaults to Type 0.
