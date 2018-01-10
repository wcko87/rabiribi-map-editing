# Cutscene Emots
This is the example `story_emot.rbrb` from the example stage provided by GemaYue.

```
Emotion Control (New Update)
//VS RITA
7
[!T1][!C1Y>6<][!EB11][!EM13][!EE11]
[!C4B<5>][!T4][!EB47][!EM42][!EE46]

19001
[!C3B<6>][!EP30][!T3][!EB36][!EM33][!EE31]
[!T3][!EB36][!EM33][!EE36]
[!T3][!EB36][!EM35][!EE33]
```

One line of emots should be created per line of dialogue in story_text.rbrb

## Format Explanation

### `!C` Create a Character
`[!CXY<Z>]`, where X, Y and Z are replaced by:
- X: Conversation ID of created character. (1-6?)
- Y: Which character to create. (A-Z, see character list below)
- Z  Position of character, (0-9, by distance from opposite of facing side). (`-` changes text box color without a portrait or character name)
- Wrapping Z in `<>` causes the character to appear on the right facing left, `><` causes them to appear on the left facing right

| ID  | Character | ID  | Character | ID  | Character | ID  | Character |
|-----|-----------|-----|-----------|-----|-----------|-----|-----------|
| `A` | Rumi      | `H` | Saya      | `O` | Chocolate | `V` | Pixie     |
| `B` | Rita      | `I` | Cicini    | `P` | Kotri     | `W` | Lilli     |
| `C` | Nieve     | `J` | Syaro     | `Q` | Keke Bunny| `X` |OBJ_DRAGON3|
| `D` | Nixie     | `K` | Cocoa     | `R` | Seana     | `Y` | Erina     |
| `E` | Aruraune  | `L` | Ashuri    | `S` | Miriam    | `Z` | Ribbon    |
| `F` | Pandora   | `M` | Lilith    | `T` | Miru      | `]` |No Character|
| `G` | Irisu     | `N` | Vanilla   | `U` | Noah      |     |           |

### `!T` Select Speaking Character
`[!TX]`, where X is replaced by:
- X: Conversation ID of talking character.

### `!E` Set Character Emotion
`[!EXYZ]`, where X, Y and Z are replaced by:
- X: Emotion part to modify. (see list of emotion parts below)
- Y: Conversation ID of character to modify.
- Z: Emotion Value.  Refer to portrait viewer in artbook.

**Note:** Emotion values usually go from 0-9. But emotion values 10 and above can also be used by following the ASCII table. `:` is 10, `;` is 11, `<` is 12 etc.

| ID  | Emotion Part |
|-----|--------------|
| `B` | Eyebrow |
| `M` | Mouth |
| `E` | Eye |
| `R` | Blush (0-4) |
| `P` | Alternate form (Kotri green = 1, kotri blue = 2) |
| `I` | Item (0 or 1) |
| `T` | Tears (0 or 1) |

#### How to have a character speak without a portrait:
`[!EPX:]`, where X is replaced by:
- X: Conversation ID of character to speak.

### `!M` Move Character Portrait
`[!MXY]`, where X, Y are replaced by:
- X: Conversation ID of character to move
- Y: Position to move the character to (0-9)

--------------------
Additional Formats:

### `~C` Set Text Box Color
`[~CRGB]`, where R, G, B are replaced by:
- R, G, B: Red (0-9), Green (0-9) and Blue (0-9) respectively.
- For example: `[~C900]` is red, `[~C099]` is cyan.
- Only works if no talking character `]` is set. The talking character normally overrides the text box color with its own.

### `~E` Fade to Black
`[~E0]`:
- Causes the screen to fade to black permanently. Cannot be reversed.
- Screen remains black after the cutscene.
- All `[~EX]`, where `X` is a number, do the same thing.

### `~F` Replace speaking character's name:
`[~FX]`: where X is replaced by:

| X = ?       | Name               | X = ?       | Name    | X = ?       | Name      |
| :---------- | :----------------- | :---------- | :------ | :---------- | :-------- |
| <= `0`      | \<Character name\> | `7`         | GemaYue | `>` (14)    | Luei      |
| `1`         | Pixie              | `8`         | Saiste  | `?` (15)    | Cross     |
| `2`         | Lilli              | `9`         | AT2.    | `@` (16)    | DUMP      |
| `3`         | ???                | `:` (10)    | Sirluma | `A` (17)    | M4        |
| `4`         | Mr. Tako           | `;` (11)    | Laluk   | `B` (18)    | IAN       |
| `5`         | WAERO              | `<` (12)    | Skullo  | >= `C` (19) | \<Blank\> |
| `6`         | Jimbow             | `=` (13)    | Yarin   |             |           |

### `~G` (seems to control CGs)
`[~GX]`, where X is replaced by a number.

### `~M` Play music during cutscene
`[~MX]`, where X is replaced by:

| X = ?  | Music                      | X = ?  | Music              |
| :----- | :------------------------- | :----- | :----------------- |
| `0` | \<No change\>                 | `5`    | Kitty Attack       |
| `1` | Melting Point / Midstream Jam | `6`    | Full On Combat     |
| `2` | Get On With It                | `7`    | Bounce Bounce      |
| `3` | Sudden Death                  | `8`    | Brawl Breaks       |
| `4` | Hi-Tech Duel                  | `9`+   | Brawl Breaks Ver.2 |

----------------------------

# Some Examples

### Example 1
```
[!C1Y<4>][!T1][!EE13][!EB12][!EM14]
```
- `[!C1Y<4>]`: Create a left facing Erina
- `[!T1]`: set her as the speaker of the current line
- `[!EE13]`: set eyes to type 3
- `[!EB12]`: set eyebrows to type 2
- `[!EM14]`: set mouth to type 4
 
### Example 2
```
[!C2K>5<][!T2][!EI21][!EE22][!EB23][!EM21][!ER24]
```
- `[!C2K>5<]`: Create a right facing Cocoa
- `[!T2]`: set her as the speaker of the current line
- `[!EI21]`: set her accessory to on (goggles for cocoa)
- `[!EE22]`: set her eyes to type 2
- `[!EB23]`: set her eyebrows to type 3
- `[!EM21]`: set mouth to type 1
- `[!ER24]`: set blush to max

### Example 3
```
[!C1A>1<][!T1][!EP1:]
```
- Create a right facing Rumi without a portrait

### Example 4 - NPC Emot
```
17
[!T2][!C2]>5<][!EB22][!EM21][!EE21][~C594]
```
- `[!C2]>5<]`: Creates a blank character
- `[~C594]`: Sets text box color to a light green
- The rest of the format can be ignored.
