ALCH Record
===========

Ingestible

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
 | ICON | Large Icon Filename | cstring | 
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a SCPT record.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | ETYP | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | ENIT | Effect Data | struct |
+* | EFID | Base Effect | formid | FormID of a [MGEF](MGEF.md) record.
+* | EFIT | Effect Data | struct |
+* | CTDA | Condition | struct |
 
### ENIT

Count | Name | Type | Info
------|------|------|-----
 | Value | int32 |
 | Flags | uint8 | See below for flags.
 | Unused | uint8[3] | ??
 | Withdrawal Effect | formid | FormID of a [SPEL](SPEL.md) record, or null.
 | Addiction Chance | float32 |
 | Sound - Consume | formid | FormID of a [SOUN](SOUN.md) record.

#### Flag Values

Flag | Meaning
-----|--------
0x00000001 | No Auto-Calc (Unused)
0x00000002 | Food Item
0x00000004 | Medicine

### EFIT

Count | Name | Type | Info
------|------|------|-----
 | Magnitude | uint32 | 
 | Area | uint32 |
 | Duration | uint32 |
 | Type | uint32 | Values of `1`, `2` and `3` correspond to types of `Self`, `Touch` and `Target` respectively.
 | Actor Value | int32 | See below for values.
 
#### Actor Values

Value | Meaning
------|--------
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

### CTDA

Count | Name | Type | Info
------|------|------|-----
 | Type | uint8 |
 | Unused | uint8[3] |
 | Comparison Value |  |
 | Function | uint32 | 
 | Parameter #1 |  |
 | Parameter #2 |  |
 | Run On | uint32 | Values and what they correspond to are given below.
 | Reference |  |
 
#### Run On Values

Value | Meaning
------|--------
1 | Subject
2 | Target
3 | Reference
4 | Combat Target
5 | Linked Reference
