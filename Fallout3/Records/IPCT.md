---
layout: fallout3rec
title: fopdoc
---
IPCT
====

Impact

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
+ | DATA | | struct |
 | [DODT](Subrecords/DODT.html) | Decal Data | struct |
 | DNAM | Texture Set | formid | FormID of a [TXST](TXST.html) record.
 | SNAM | Sound 1 | formid | FormID of a SOUN ([FO3](../../Fallout3/Records/SOUN.html), [FNV](../../FalloutNV/Records/SOUN.html)) record.
 | NAM1 | Sound 2 | formid | FormID of a SOUN ([FO3](../../Fallout3/Records/SOUN.html), [FNV](../../FalloutNV/Records/SOUN.html)) record.

### DATA

Name | Type | Info
-----|------|-----
Effect - Duration | float32 |
Effect - Orientation | uint32 | Enum - see below for values.
Angle Threshold | float32 |
Placement Radius | float32 |
[Sound Level](Values/Sound Levels.html) | uint32 |
Flags | uint32 | See below for values.

#### Effect Orientation Enum Values

Value | Meaning
------|--------
0 | Surface Normal
1 | Projectile Vector
2 | Projectile Reflection

#### Flag Values

Value | Meaning
------|--------
0x00000001 | No Decal Data
