---
layout: fallout3rec
title: fopdoc
---
RGDL
====

Ragdoll

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | NVER | Version | uint32 |
+ | DATA | General Data | struct |
+ | XNAM | Actor Base | formid | FormID of a CREA ([FO3](../../Fallout3/Records/CREA.html), [FNV](../../FalloutNV/Records/CREA.html)) or NPC_ ([FO3](../../Fallout3/Records/NPC_.html), [FNV](../../FalloutNV/Records/NPC_.html)) record.
+ | TNAM | Body Part Data | formid | FormID of a [BPTD](BPTD.html) BPTD ([FO3](../../Fallout3/Records/BPTD.html), [FNV](../../FalloutNV/Records/BPTD.html)) record.
 | RAFD | Feedback Data | struct |
 | RAFB | Feedback Dynamic Bones | uint16[] |
+ | RAPS | Pose Matching Data | struct |
 | ANAM | Death Pose | cstring |


### DATA

Name | Type | Info
-----|------|-----
Dynamic Bone Count | uint32 |
Unused | byte[4] |
Feedback Enabled | uint8 | Enum - see below for values.
Foot IK Enabled | uint8 | Enum - see below for values.
Look IK Enabled | uint8 | Enum - see below for values.
Grab IK Enabled | uint8 | Enum - see below for values.
Pose Matching | uint8 | Enum - see below for values.
Unused | byte |

#### Enabled Enum Values

Value | Meaning
------|--------
0 | No
1 | Yes

### RAFD

Name | Type | Info
-----|------|-----
Dynamic / Keyframe Blend Amount | float32 |
Hierarchy Gain | float32 |
Position Gain | float32 |
Velocity Gain | float32 |
Acceleration Gain | float32 |
Snap Gain | float32 |
Velocity Damping | float32 |
Snap Max Linear Velocity | float32 |
Snap Max Angular Velocity | float32 |
Snap Max Linear Distance | float32 |
Snap Max Angular Distance | float32 |
Position Max Linear Velocity | float32 |
Position Max Angular Velocity | float32 |
Projectile Position Max Velocity | int32 | Value is divided by 1000.
Melee Position Max Velocity | uint32 | Value is divided by 1000.

### RAPS

Name | Type | Info
-----|------|-----
Match Bone 1 | uint16 |
Match Bone 2 | uint16 |
Match Bone 3 | uint16 |
Flags | uint8 | See below for values.
Unused | byte |
Motors Strength | float32 |
Pose Activation Delay Time | float32 |
Match Error Allowance | float32 |
Displacement To Disable | float32 |

#### Flag Values

Value | Meaning
------|--------
0x01 | Disable On Move
