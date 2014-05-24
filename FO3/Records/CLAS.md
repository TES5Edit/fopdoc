CLAS
====

Class

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | FULL | Name | cstring |
+ | DESC | Description | cstring |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
+ | DATA | | struct |
+* | ATTR | Attribute | uint8 | There are 7 attribute fields, one for each attribute. The mapping of fields to attributes is given below.

### DATA

Count | Name | Type | Info
------|------|------|-----
-* | Tag Skill | int32 | Enum - see below for values. There are 4 Tag Skill fields in this block.
 | Flags | uint32 | See below for values.
 | Buys/Sells and Services | uint32 | Flags. See below for values.
 | [Teaches]](Enums/Skills.md) | int8 | See the link for enum values.
 | Maximum Training Level | uint8 | 
 | Unused | uint8[2] |

#### Tag Skill Enum Values

Value | Meaning
------|--------
-1 | None
00 | Aggresion
01 | Confidence
02 | Energy
03 | Responsibility
04 | Mood
05 | Strength
06 | Perception
07 | Endurance
08 | Charisma
09 | Intelligence
10 | Agility
11 | Luck
12 | Action Points
13 | Carry Weight
14 | Critical Chance
15 | Heal Rate
16 | Health
17 | Melee Damage
18 | Damage Resistance
19 | Poison Resistance
20 | Rad Resistance
21 | Speed Multiplier
22 | Fatigue
23 | Karma
24 | XP
25 | Perception Condition
26 | Endurance Condition
27 | Left Attack Condition
28 | Right Attack Condition
29 | Left Mobility Condition
30 | Right Mobility Condition
31 | Brain Condition
32 | Barter
33 | Big Guns
34 | Energy Weapons
35 | Explosives
36 | Lockpick
37 | Medicine
38 | Melee Weapons
39 | Repair
40 | Science
41 | Small Guns
42 | Sneak
43 | Speech
44 | Throwing (unused)
45 | Unarmed
46 | Inventory Weight
47 | Paralysis
48 | Invisibility
49 | Chameleon
50 | Night Eye
51 | Detect Life Range
52 | Fire Resistance
53 | Water Breathing
54 | Rad Level
55 | Bloody Mess
56 | Unarmed Damage
57 | Assistance
58 | Electric Resistance
59 | Frost Resistance
60 | Energy Resistance
61 | EMP Resistance
62 | ??
63 | ??
64 | ??
65 | ??
66 | ??
67 | ??
68 | ??
79 | ??
70 | ??
71 | ??
72 | Ignore Negative Effects

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Playable
0x00000002 | Guard

#### Buys/Sells and Services Flags

Value | Meaning
------|--------
0x00000001 | Weapons
0x00000002 | Armor
0x00000004 | Alcohol
0x00000008 | Books
0x00000010 | Food
0x00000020 | Chems
0x00000040 | Stimpacks
0x00000080 | Lights?
0x00000100 | ??
0x00000200 | ??
0x00000400 | Miscellaneous
0x00000800 | ??
0x00001000 | ??
0x00002000 | Potions?
0x00004000 | Training
0x00008000 | ??
0x00010000 | Recharge
0x00020000 | Repair

### ATTR Map

ATTR Field | Attribute
-----------|----------
1st | Strength
2nd | Perception
3rd | Endurance
4th | Charisma
5th | Intelligence
6th | Agility
7th | Luck
