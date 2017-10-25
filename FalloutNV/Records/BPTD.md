---
layout: falloutnvrec
title: fopdoc
---
BPTD
====

Body Part Data

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | | [Model Data](Subrecords/Model.html) | collection |
+* | | Body Part | collection | See below for details.
+* | | Unnamed Body Part | collection | See below for details.
 | RAGA | Ragdoll | formid | FormID of a [RGDL](RGDL.html) record.

### Body Part Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | BPTN | Part Name | cstring |
+ | BPNN | Part Node | cstring |
+ | BPNT | VATS Target | cstring |
+ | BPNI | IK Data - Start Node | cstring |
+ | BPND | | struct |
+ | NAM1 | Limb Replacement Model | cstring |
+ | NAM4 | Gore Effects - Target Bone | cstring |
 | NAM5 | Texture File Hashes | ?? |

### Unnamed Body Part Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | BPNN | Part Node | cstring |
+ | BPNT | VATS Target | cstring |
+ | BPNI | IK Data - Start Node | cstring |
+ | BPND | | struct |
+ | NAM1 | Limb Replacement Model | cstring |
+ | NAM4 | Gore Effects - Target Bone | cstring |
 | NAM5 | Texture File Hashes | ?? |

### BPND

Name | Type | Info
-----|------|-----
Damage Multiplier | float32 |
Flags | uint8 | See below for values.
Part Type | uint8 | Enum - see below for values.
Health Percent | uint8 |
[Actor Value](Values/Actor Values.html) | int8 |
To Hit Chance | uint8 |
Explodable - Explosion Chance % | uint8 |
Explodable - Debris Count | uint16 |
Explodable - Debris | formid | FormID of a [DEBR](DEBR.html) record, or null.
Explodable - Explosion | FormID of a [EXPL](EXPL.html) record, or null.
Tracking Max Angle | float32 |
Explodable - Debris Scale | float32 |
Severable - Debris Count | int32 |
Severable - Debris | formid | FormID of a [DEBR](DEBR.html) record, or null.
Severable - Explosion | FormID of a [EXPL](EXPL.html) record, or null.
Severable - Debris Scale | float32 |
Gore Effects - Translate X | float32 |
Gore Effects - Translate Y | float32 |
Gore Effects - Translate Z | float32 |
Gore Effects - X Rotation | float32 |
Gore Effects - Y Rotation | float32 |
Gore Effects - Z Rotation | float32 |
Severable - Impact Dataset | formid | FormID of a [IPDS](IPDS.html) record, or null.
Explodable - Impact Dataset | formid | FormID of a [IPDS](IPDS.html) record, or null.
Severable - Decal Count | uint8 |
Explodable - Decal Count | uint8 |
Unused | byte[2] |
Limb Replacement Scale | float32 |

#### Flag Values

Value | Meaning
------|--------
0x01 | Severable
0x02 | IK Data
0x04 | IK Data - Biped Data
0x08 | Explodable
0x10 | IK Data - Is Head
0x20 | IK Data - Headtracking
0x40 | To Hit Chance - Absolute

#### Part Type Enum Values

Value | Meaning
------|--------
0 | Torso
1 | Head 1
2 | Head 2
3 | Left Arm 1
4 | Left Arm 2
5 | Right Arm 1
6 | Right Arm 2
7 | Left Leg 1
8 | Left Leg 2
9 | Left Leg 3
10 | Right Leg 1
11 | Right Leg 2
12 | Right Leg 3
13 | Brain
14 | Weapon
