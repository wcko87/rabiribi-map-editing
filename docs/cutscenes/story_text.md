# Cutscene Text
This is the example `story_text.rbrb` from the example stage provided by GemaYue.

```
English
//VS RITA
7
Ms. Rita?@Is this the end of the example?
You are right. Before the ending...@Let's try a scroll screen boss battle!@A cut feature during development!

19001
Welcome to the example map!@Which contain many special trigger events!@You can even customize the character dialog!
Go to "custom" and@"custom\Erina and the example stage" folders@for more details! 
Also, by using -debugshowevents as launch options.@You can study more things in this map!
```

# Format Explanation

The numbers before each cutscene represents the cutscene ID. Each event in the game triggers a different cutscene ID.

Each new line creates a new dialog box in the cutscene.

### Special Characters

|Character | Icon |
|--|--|
| `@` | Line break (within the same dialog box) |

#### Button Icons
|Character | Icon |
|--|--|
| `*0` | Right Arrow |
| `*1` | Down Arrow |
| `*2` | Left Arrow |
| `*3` | Up Arrow |
| `*4` | Jump |
| `*5` | Boost Attack |
| `*6` | Magic Attack |
| `*7` | Hammer Attack |
| `*8` | Change Magic Type - Left |
| `*9` | Change Magic Type - Right |
| `*;` | Item/Magic Menu |
| `*:` | Pause/Status Screen |

**Note:** The icons show up to the left of where the character is placed, as shown in the image below:

Text:
```
1:*1 2:*2 3:*3 4:*4 5:*5 6:*6 7:*7 8:*8 9:*9@::*: ;:*; <:*< =:*= >:*> ?:*? At:*@
```
![item_icons](https://user-images.githubusercontent.com/27341392/34705385-10b621d0-f53b-11e7-962f-abcbfe4c5491.png)

(the image can be a little misleading. e.g. the Right arrow appears to the left of the 0:, instead of after it)
