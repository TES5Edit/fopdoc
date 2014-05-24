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
+ | DATA | Data | struct |
+* | ATTR | Attribute | uint8 | There are 7 attribute fields, one for each attribute. The mapping of fields to attributes is given below.

### DATA

Count | Name | Type | Info
------|------|------|-----
-* | Tag Skill | int32 | Enum - see below for values. There are 4 Tag Skill fields in this block.
 | Flags | uint32 | See below for values.
 | [Buys/Sells and Services](Values/Services.md) | uint32 | Flags. See the link for values.
 | [Teaches](Values/Skills.md) | int8 | See the link for enum values.
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
