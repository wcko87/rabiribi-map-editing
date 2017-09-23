# Entities

Entities are generally objects you can interact with in-game. This includes things like:
- Enemies
- Bosses
- Springs / Computer Desks
- NPCs

Entities have IDs in the 1000+ range.

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

# Direction Modifiers

If an entity uses direction modifiers, then use these events as modifiers instead:
- Right: `195`
- Left: `196`
- Up: `198`
- Down: `199`

Direction modifiers can be used along with type modifiers if you place the direction modifier in the event stack.

# Entity List

Names based off -debugshowevents tile names.

Boss NPCs are included in the list but I only tested Rita and Pandora due to them having shadow clone events.
Any boss NPC can be activated by other boss events, allowing for double boss encounters. Defeating any of them will exit boss mode, however.

If the entity is not listed here, it just spawns in an Erina. Usually a small one.

- **[1003] Four-way fire bar**
  - Rotates counter-clockwise.

- **[1004] Three-way fire bar**
  - Rotates counter-clockwise.
  - Faster than its four-way cousin.

- **[1005] Spike ball**
  - Floats left. Turns around when it hits a solid object.
  - Initial direction can be changed with up and down direction modifiers.

- **[1006] Super spike ball**
  - Floats left. Turns around when it hits a solid object.
  - Deals much, MUCH more damage and travels faster than event 1005.
  - Initial direction can be changed with up and down direction modifiers.

- **[1007] Wall climber**
  - Travels right. If not on a solid surface, travels in circles or until it finds a surface to follow, at which case it will travel along that surface.
  - Initial travel direction can be changed with all direction modifiers.

- **[1008] Blue death laser**
  - Fires left. Deals ludicrous amounts of damage.
  - Fires when Erina gets close.
  - Direction can be changed with right direction modifier.

- **[1009] Prologue Cocoa**

- **[1010] LED Face (Cave 2 emoji boss)**
  - Invisible unless activated through a boss event, but will still do collision damage.

- **[1011] Rumi**
- **[1012] Ashuri**
- **[1013] Rita**
- **[1014] Ribbon**
- **[1015] Forgotten Cave Cocoa**
- **[1016] Computer Cicini**

- **[1017] Cicini's desk "PC OBJ"**
  - Can be a variety of objects based on background, room color, and type. Too lazy to test right now. Most notable is type 12 being a spring.

- **[1018] Cicini**

- **[1019] Red laser**
  - Fires left. Deals significantly less damage than event 1008.
  - Direction can be changed with all direction modifiers.

- **[1020] Saya**
- **[1021] Syaro**

- **[1022] Pandora**
  - Type 5 is Shadow Pandora and behaves differently.

- **[1023] Nieve**
- **[1024] Nixie**
- **[1025] Aruraune**

- **[1027] "Into Town"**
  - No idea what this does.

- **[1028] Interactable NPC**
  - Appearance and dialogue is determined by type modifier. If no modifier is set, you will see error messages and a blank text box.

- **[1030] Seana**
- **[1031] Lilith**
- **[1032] Vanilla**
- Type 1 behaves like Chocolate for some attacks.

- **[1033] Chocolate**
- Type 0 (default) behaves like Vanilla for some attacks. Type 1 behaves like expected from her normal Ravine event.

- **[1035] Illusion Alius 1**
  - Has modifiers. Type 1 is Alius 2, type 2 is Alius 3, and type 3 is Alius 4.

- **[1036] Pink Kotri**
  - Has modifiers. Type 1 is green, type 2 is blue, and type 3 is pink.

- **[1037] Slimy Noah**
- **[1038] Irisu**
- **[1039] Miriam**
- **[1043] Miru**

- **[1045] Rita 2**
  - Type 5 is Shadow Rita

- **[1046] Lilli**
  - If activated in a boss event, it will fire at enemies.
  - Type 1 is Pixie.
  - Entity type affects the fired projectile.

- **[1053] Noah 3**

- **[1054] Keke Bunny**
  - Will have boss AI outside of boss events.

- **[1055] Sitting Mr. Tako**
  - Only faces left. Has a dialogue box when you speak to him, so you can maybe hide him behind a wall for a free text box or something.
  - Type 3 stands up and turns around to face you.

- **[1056] Blue Ordinary Cat**
  - Type-1 is the Red Ordinary Cat.
  - If you spawn one without the other, they will come with Meow Respawn.

- **[1096] Pink bunny slime**
  - Type 2 is a blue fairy with slime AI. When on the ground, it cycles through fairy colors.
  - Type 5 is a big bunny.
  - Type 6 is a large bunny.
  - Type 7 is a huge bunny.

- **[1097] Flower**
  - Only spawns after event ID 298 is set (EV_TELEPORT2)
  - Type 1 is a blue flower that shoots bubbles.
  - Type 2 is a red laser flower.
  - Type 5 is a big flower.
  - Type 6 is a large flower.
  - Type 7 is a huge flower.

- **[1098] Ball mouse (roly-poly)**
  - Only spawns after event ID 298 is set (EV_TELEPORT2)
  
- **[1099] Bee**

- **[1102] Duck**
  - Only spawns after event ID 298 is set (EV_TELEPORT2)

- **[1100] Rafflesia**
  - Type 1 is green and fires larges amounts of green bullets skywards, which fall back down a short time later.

- **[1101] Wisp**
  - Type 2+ are exploding Halloween DLC pumpkins.

- **[1103] Mushroom**
- **[1105] Brown Mushroom**
  - Same notes as pink bunny slime, including the fairy.

- **[1104] Dog**
  - Dog!

- **[1106] Worm**
  - Type 1 fires projectiles.

- **[1107] Cactus that follows you**

- **[1108] Eagle**
  - Type 1 fires excessively powerful bullets upon swooping.

- **[1109] Blue blob charger**
  - Type 1 is pink.

- **[1110] UPRPRC member with overalls and pink hair**

- **[1111] Purple bunny slime**
  - Fires projectiles
  - Same notes as pink bunny slime regarding size, but larger ones do not fire projectiles

- **[1112] Egg**
  - Type 1 is blue and fires projectiles
  - Type 2+ is yellow but behaves like blue

- **[1113] Dice**
  - Type affects the number on the block and how many fairies pop out, up to type 5.

- **[1114] UPRPRC fairy - black suit/ears (blue)**
  - Type affects the fairy color and behavior.
  - Type 1 is red, type 2 is yellow, type 3 is green, type 4 is purple, type 5 is gray.

- **[1115] Card soldier**

- **[1116] Bunny thwomp (Down)**
  - Type affects movement.
  - Type 1 moves left.
  - Type 2 moves up.
  - Type 3 moves right.
  - Type 4+ simply do not move at all.

- **[1117] UPRPRC hugger (red)**
  - Type affects color.
  - Type 1 is green, type 2 is blue, and type 3 is yellow.
  - Requires event flag 307 (FOREST UPRPRC) to spawn.

- **[1118] UPRPRC swimsuit gunner (red)**
  - Type affects color and attack pattern.
  - Type 1 is blue, type 2 is yellow, and type 3 is green.

- **[1119] UPRPRC debuff mage (blue)**
  - Type affects color and inflicted debuff.
  - Type 1 is red, type 2 is green, and type 3 is yellow.

- **[1120] UPRPRC bomber (red)**
  - Type affects color and bomb effects.
  - Type 1 is blue, type 2 is purple, and type 3 is green.

- **[1124] Open box**
  - And the crowd goes wild!

- **[1125] Vehicle**
  - Travels left. Can be forced to travel right with direction modifiers.
  - Type affects the vehicle sprite.

- **[1126] Skinny otaku (green jacket)**
  - Type affects jacket color and attack pattern. Type 1 is yellow and type 2 is blue.
  - Types above 2 will render them with CreSpirit secret base NPCs, but they will still attack.

- **[1127] Fat otaku (red shirt)**
  - Type 1 is black jacket.

- **[1128] Sandbag**

- **[1129] "STG FAIRY"**
  - A few are in Cocoa 2's arena, but I can't personally get them to spawn out of the box.
  - Type likely affects attack pattern as all of those are type 2.

- **[1130] Fake rock**
  - Type 1 is a fake snow poff. Landing spreads snow bullets.
  - Higher types appear to move much faster and aggressively.

- **[1131] Rock-tossing mole**

- **[1132] Five-way lab turret (down)**
  - Type affects direction.
  - Type 1 fires left, type 2 fires right, and type 3 fires up.

- **[1133] Tall lab bot**
  - Type 1 is Mr. Big Box.
  - Type 5 fires eye lasers with blue sparks that will turn 90 degrees to seek Erina.

- **[1134] Flying lab bot**

- **[1135] Small lab bot**
  - Type 1 is a miniature lab bot.

- **[1136] Robot Maid (pink)**
  - Type affects color and attack pattern.
  - Type 1 is blue, type 2 is yellow, and type 3 is green.
  - Type 4 is Rainbow Maid.

- **[1137] Spider**
  - Drops to spawn location when Erina gets close.
  - Type 1 spawns already dropped.
  - Can use left and right direction modifier to force it to spin a certain way regardless of where Erina enters from.

- **[1138] Riverbank running swarmers**
  - Type 2 is the Halloween variant.

- **[1139] Hug fairy (blue)**
  - Type affects color and movement pattern.
  - Type 1 is yellow, type 2 is red, and type 3 is green.

- **[1140] Cyber cube (blue)**
  - Type affects color and attack pattern.
  - Type 1 is green, type 2 is yellow, type 3 is red, type 4 is silver.
  - Types 3 and 4 deal large damage.

- **[1141] Irisu clone**
  - Size is random and cannot be controlled.

- **[1142] Rainbow Crystal boss core**

- **[1143] Rainbow Crystal boss part (red)**
  - For use with Rainbow Crystal boss core.
  - Type affects color.
  - No idea how to actually put these together right now.

- **[1144] UPRPRC Tank (yellow)**
  - Type affects color and attack pattern.
  - Type 1 is blue and type 2 is green.

- **[1145] Bouncy cat (gray)**
  - Type affects color and jump height.
  - Type 1 is blue and jumps higher, type 2 is the Halloween version.
  - Requires event flag 257 (MEET FAIRY) to spawn.

- **[1146] Spark ball (rainbow)**
  - Type affects color, speed, and power.
  - Type 1 is blue, type 2 is yellow, and type 3 is green.
  - Type 4+ is rainbow and very slow.

- **[1147] UPRPRC mage (blue)**
  - Type affects color and attack pattern.
  - Type 1 is red, type 2 is green, and type 3 is yellow.

- **[1148] Snow ball (normal)**
  - Hops at Erina and splits when near.
  - Type 1 is a snow ball fragment.

- **[1149] Elemental magic ball (Light blue)**
  - Type affects color and attack pattern.
  - Type 1 is dark blue, and type 2 is red.

- **[1150] UPRPRC fairy - white suit/ears (blue)**
  - Type affects the fairy color and behavior.
  - Type 1 is red, type 2 is yellow, type 3 is green, type 4 is purple, type 5 is gray.
  - Basically the same thing as entity 1114.

- **[1151] Pyramid eye**
  - For use with 1152 (Pyramid laser)

- **[1152] Pyramid laser**
  - Type 0 moves horizontally on the row it is spawned on
  - Type 1 moves vertically on the column it is spawned on
  - Changes direction by reaching an instance of event 198
  - If it detects Erina, it temporarily activates boss mode and causes all instances of 1151 (Pyramid eye) to shoot at Erina
  - Cannot detect Erina if she is standing on event 200 tiles

- **[1153] UPRPRC Speed Up mage**

- **[1154] City NPC (Salary man)**
  - Used in one of the Stele cutscenes. Has no animations, but will turn to face Erina.
  - Type affects sprite, unsure how far it affects to

- **[1155] Aurora Palace laser**
  - Fires in regular intervals based on difficulty.

- **[1156] Meaty Bone (boomerang)**
  - Type 1 fires exploding bones which can destroy bomb blocks.
  - Type 5 is large.
  - Type 6 is huge.

- **[1157] Plurkwood bullet spitter**

- **[1158] Plurkwood mouth slime**
  - Type 5 is large.
  - Type 6 is huge.

- **[1159] Plurkwood bat**
  - Type affects initial movement pattern, up to 3.
  - Type 4+ is stationary.

- **[1160] Fish (yellow)**
  - Type affects color and AI.
  - Type 1 is blue, type 2 is green.
  - Types above 2 print weird sprites but do not fire bullets. For example, type 3 is a bunny ghost.

- **[1161] Mummy ball**

- **[1162] Five floating energy swords**

- **[1163] Library crystal (red)**
  - Type affects color and attack pattern.
  - Type 1 is orange, type 2 is yellow, type 3 is green, type 4 is cyan, type 5 is blue, type 6 is purple, and type 7 is silver.

- **[1164] Bunny ghost**
  - Higher type modifier makes it deal more damage.

### Unimplemented, semi-functional events

- **[1001] "Small Slime"**
  - Small Erina that behaves like a bunny slime enemy.

- **[1002] "Rush thing"**
  - Small Erina that runs left. Turns around when it hits a solid object.

- **[1047] Cat Golem Head**
  - Just kinda floats around.

- **[1048] Cat Golem Hand**
  - Probably for use with Cat Golem. I haven't tried them both together.

- **[1165, 1166] Blank**
  - Spreadsheet says these are actual events but I can't get anything out of them.

