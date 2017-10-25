---
layout: falloutnvrec
title: fopdoc
---
PROJ
====

Projectile

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.md) | collection |
 | | [Destruction Data](Subrecords/Destruction.md) | collection |
+ | [DATA](#data) | Data | struct
+ | NAM1 | Muzzle Flash Model Filename | cstring |
+ | NAM2 | Muzzle Flash Model Texture File Hashes | uint8[] |
+ | [VNAM](Values/Sound Levels.md) | Sound Level | uint32 | Enum - see link for values.

### DATA

Name | Type | Info
-----|------|-----
Flags | uint16 | See below for values.
Type | uint16 | Enum - see below for values.
Gravity | float32 |
Speed | float32 |
Range | float32 |
Light | formid | FormID of a [LIGH](LIGH.md) record, or null.
Muzzle Flash - Light | formid | FormID of a [LIGH](LIGH.md) record, or null.
Tracer Chance | float32 |
Explosion - Alt. Trigger - Proximity | float32 |
Explosion - Alt. Trigger - Timer | float32 |
Explosion | formid | FormID of an [EXPL](EXPL.md) record, or null.
Sound | formid | FormID of a [SOUN](SOUN.md) record, or null.
Muzzle Flash - Duration | float32 |
Fade Duration | float32 |
Impact Force | float32 |
Sound - Countdown | formid | FormID of a [SOUN](SOUN.md) record, or null.
Sound - Disable | formid | FormID of a [SOUN](SOUN.md) record, or null.
Default Weapon Source | formid | FormID of a [WEAP](WEAP.md) record, or null.
X Rotation | float32 |
Y Rotation | float32 |
Z Rotation | float32 |
Bouncy Multiplier | float32 |

#### Flag Values

Value | Meaning
------|--------
0x0001 | Hitscan
0x0002 | Explosion
0x0004 | Alt. Trigger
0x0008 | Muzzle Flash
0x0010 | ??
0x0020 | Can Be Disabled
0x0040 | Can Be Picked Up
0x0080 | Supersonic
0x0100 | Pins Limbs
0x0200 | Pass Through Small Transparent
0x0400 | Detonates
0x0800 | Rotation

#### Type Enum Values

Value | Meaning
------|--------
0 | ??
1 | Missile
2 | Lobber
3 | ??
4 | Beam
5 | ??
6 | ??
7 | ??
8 | Flame
9 | ??
10 | ??
11 | ??
12 | ??
13 | ??
14 | ??
15 | ??
16 | Continuous Beam


