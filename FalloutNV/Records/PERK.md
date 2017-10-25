---
layout: falloutnvrec
title: fopdoc
---
PERK
====

Perk

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
+ | DESC | Description | cstring |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
-* | [CTDA](Subrecords/CTDA.md) | Condition | struct |
+ | DATA | Data | struct |
-* | | Effect | collection | See below for details.

### DATA (Data)

Name | Type | Info
-----|------|-----
Trait | uint8 | Enum - see below for values.
Min Level | uint8 |
Ranks | uint8 |
Playable | uint8 | Enum -see below for values.
Hidden | uint8 | Enum -see below for values.

#### Trait / Playable / Hidden Enum Values

Value | Meaning
------|--------
0 | No
1 | Yes

### Effect Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | PRKE | Header | struct |
+ | DATA | Effect Data | struct *or * formid |
-* | | Perk Conditions | collection | See below for details.
 | EPFT | Entry Point Function Type | uint8 | Decides the data type of the EPFD record.
 | EPFD | Entry Point Function Data | uint8[] *or* float32 *or* formid *or* null |
 | EPF2 | Button Label | cstring |
 | EPF3 | Script Flags | uint16 | See below for values.
 | | [Embedded Script](Subrecords/Script.md) | collection |
+ | PRKF | End Marker | null | Flag


#### PRKE

Name | Type | Info
-----|------|-----
Type | uint8 | Enum -see below for values.
Rank | uint8 |
Priority | uint8 |

##### Type Enum Values

Value | Meaning
------|--------
0 | Quest + Stage
1 | Ability
2 | Entry Point

#### DATA (Effect Data)

There are three possible DATA formats, based on the value of the Type field in the preceding PRKE subrecord.

##### Quest + Stage

Name | Type | Info
-----|------|-----
Quest | formid | FormID of a [QUST](QUST.md) record.
Quest Stage | uint8 |
Unused | byte[3] |

##### Ability

Name | Type | Info
-----|------|-----
Ability | formid | FormID of a [SPEL](SPEL.md) record.

##### Entry Point

Name | Type | Info
-----|------|-----
Entry Point | uint8 | Enum - see below for values.
Function | uint8 |
Perk Condition Tab Count | uint8 |

###### Entry Point Enum Values

Value | Meaning
------|--------
0 | Calculate Weapon Damage
1 | Calculate My Critical Hit Chance
2 | Calculate My Critical Hit Damage
3 | Calculate Weapon Attack AP Cost
4 | Calculate Mine Explode Chance
5 | Adjust Range Penalty
6 | Adjust Limb Damage
7 | Calculate Weapon Range
8 | Calculate To Hit Chance
9 | Adjust Experience Points
10 | Adjust Gained Skill Points
11 | Adjust Book Skill Points
12 | Modify Recovered Health
13 | Calculate Inventory AP Cost
14 | Get Disposition
15 | Get Should Attack
16 | Get Should Assist
17 | Calculate Buy Price
18 | Get Bad Karma
19 | Get Good Karma
20 | Ignore Locked Terminal
21 | Add Leveled List On Death
22 | Get Max Carry Weight
23 | Modify Addiction Chance
24 | Modify Addiction Duration
25 | Modify Positive Chem Duration
26 | Adjust Drinking Radiation
27 | Activate
28 | Mysterious Stranger
29 | Has Paralyzing Palm
30 | Hacking Science Bonus
31 | Ignore Running During Detection
32 | Ignore Broken Lock
33 | Has Concentrated Fire
34 | Calculate Gun Spread
35 | Player Kill AP Reward
36 | Modify Enemy Critical Hit Chance
37 | Reload Speed
38 | Equip Speed
39 | Action Point Regen
40 | Action Point Cost
41 | Miss Fortune
42 | Modify Run Speed
43 | Modify Attack Speed
44 | Modify Radiation Consumed
45 | Has Pip Hacker
46 | Has Meltdown
47 | See Enemy Health
48 | Has Jury Rigging
49 | Modify Threat Range
50 | Modify Thread
51 | Has Fast Travel Always
52 | Knockdown Chance
53 | Modify Weapon Strength Req
54 | Modify Aiming Move Speed
55 | Modify Light Items
56 | Modify Damage Threshold (defender)
57 | Modify Chance for Ammo Item
58 | Modify Damage Threshold (attacker)
59 | Modify Throwing Velocity
60 | Chance for Item on Fire
61 | Has Unarmed Forward Power Attack
62 | Has Unarmed Back Power Attack
63 | Has Unarmed Crouched Power Attack
64 | Has Unarmed Counter Attack
65 | Has Unarmed Left Power Attack
66 | Has Unarmed Right Power Attack
67 | VATS HelperChance
68 | Modify Item Damage
69 | Has Improved Detection
70 | Has Improved Spotting
71 | Has Improved Item Detection
72 | Adjust Explosion Radius
73 | Reserved

#### Perk Condition Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | PRKC | Run On | int8 |
+* | [CTDA](Subrecords/CTDA.md) | Condition | struct |

#### EPFD

The subrecord type is decided as described in the table below.

EPFT Value | EPFD Type | Info
-----------|-----------|-----
0 | uint8[] |
1 | float32 |
2 | struct | A struct consisting of two `float32` values.
3 | formid | FormID of a [LVLI](LVLI.md) record.
4 | null |
5 | struct | A struct consisting of a `uint32` [actor value](Values/Actor Values.md) enum followed by a `float32` value.

If the EPFT value is `2` and DATA's Function field (when DATA is an entry point) is `5`, the EPFD type is chosen as if the EPFT value were `5`.

#### EPF3 Flag Values

Value | Meaning
------|--------
0x0001 | Run Immediately

