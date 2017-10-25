---
layout: fallout4rec
title: fopdoc
---
Effect Subrecord Collection
=======================

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EFID | Base Effect | formid | FormID of a [MGEF](../MGEF.md) record.
+ | [EFIT](#efit) | Effect Data | struct |
 | [CTDA](CTDA.md) | Condition | struct |

### EFIT

Name | Type | Info
-----|------|-----
Magnitude | uint32 |
Area | uint32 |
Duration | uint32 |
Type | uint32 | See below for values.
Actor Value | int32 | See below for values.
 
#### Type Enum Values

Value | Meaning
------|--------
0 | Self
1 | Touch
2 | Target
 
#### Actor Values

Value | Meaning
------|--------
-1 | None
0 | Aggression
1 | Confidence
2 | Energy
3 | Responsibility
4 | Mood
5 | Strength
6 | Perception
7 | Endurance
8 | Charisma
9 | Intelligence
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
69 | ??
70 | ??
71 | ??
72 | Ignore Negative Effects


