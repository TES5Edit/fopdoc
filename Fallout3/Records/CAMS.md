---
layout: fallout3rec
title: fopdoc
---
CAMS
====

Camera Shot

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
+ | DATA | Data | struct |
 | MNAM | Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.

### DATA

Name | Type | Info
-----|------|-----
Action | uint32 | Enum - see below for values.
Location | uint32 | Enum - see below for values.
Target | uint32 | Enum - see below for values.
Flags | uint32 | See below for values.
Player Time Multiplier | float32 |
Target Time Multiplier | float32 |
Global Time Multiplier | float32 |
Max Time | float32 |
Min Time | float32 |
Target % Between Actors | float32 |

#### Action Enum Values

Value | Meaning
------|--------
0 | Shoot
1 | Fly
2 | Hit
3 | Zoom

#### Location / Target Enum Values

Value | Meaning
------|--------
0 | Attacker
1 | Projectile
2 | Target

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Position Follows Location
0x00000002 | Rotation Follows Target
0x00000004 | Don't Follow Bone
0x00000008 | First Person Camera
0x00000010 | No Tracer
0x00000020 | Start At Time Zero

