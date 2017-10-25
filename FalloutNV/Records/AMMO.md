---
layout: falloutnvrec
title: fopdoc
---
AMMO
====

Ammunition

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
+ | [DATA](#data) | Data | struct |
 | DAT2 | Data 2 | struct |
 | ONAM | Short Name | cstring |
 | QNAM | Abbreviation | cstring |
-* | RCIL | Ammo Effect | formid | FormID of an [AMEF](AMEF.html) record.

### DATA

Name | Type | Info
-----|------|-----
Speed | float32 |
Flags | uint8 | See below for values
Unused | byte[3] |
Value | int32 |
Clip Rounds | uint8 |

#### Flag Values

Flag | Meaning
-----|--------
0x01 | Ignores Normal Weapon Resistance
0x02 | Non-Playable

### DAT2

Name | Type | Info
-----|------|-----
Projectiles Per Shot | uint32 |
Projectile | formid | FormID of a [PROJ](PROJ.html) record, or null.
Weight | float32 |
Consumed Ammo | formid | FormID of an [AMMO](AMMO.html) or [MISC](MISC.html) record, or null.
Consumed Percentage | float32 |
