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

# Format Explanation

Create a character format: `[!CXY<Z>]`
- X determines the conversation ID of the created character. (1-6?)
- Y determines which character is created. (A-Z)
- Z determines distance from opposite of facing side. (0-9, `-` changes text box color without a cutin or character name)
- Wrapping Z in `<>` causes the character to face left, `><` faces right
 
Edit character emotions format: `[!EXYZ]`
- X determines which part to modify.
- Y determines which character to modify based on their conversation ID.
- Z determines emotion value.  Refer to portrait viewer in artbook.
 
Select speaking character: `[!TX]`
- X determines talking character by their conversation ID.
 
Emotion parts:
```
B Eyebrow
M Mouth
E Eye
R Blush (0-4)
P Alternate form (Kotri green = 1, kotri blue = 2)
I Item (0 or 1)
```
 
Created character:
```
A Rumi
B Rita
C Nieve
D Nixie
E Aruraune
F Pandora
G Irisu
H Saya
I Cicini
J Syaro
K Cocoa
L Ashuri
M Lilith
N Vanilla
O Chocolate
P Kotri
Q Keke Bunny
R Seana
S Miriam
T Miru
U Noah
V Pixie
W Lilli
X OBJ_DRAGON3
Y Erina
Z Ribbon
```
 
# Examples

**Example 1**: `[!C1Y<4>][!T1][!EE13][!EB12][!EM14]`
- Create a left facing Erina
- set her as the speaker of the current line
- set her eyes to type 3
- set eyebrows to type 2
- set mouth to type 4
 
**Example 2**: `[!C2K>5<][!T2][!EI21][!EE22][!EB23][!EM21][!ER24]`
- Create a right facing Cocoa
- set her as the speaker of the current line
- set her accessory to on (goggles for cocoa)
- set her eyes to type 2
set her eyebrows to type 3
set mouth to type 1
set blush to max
