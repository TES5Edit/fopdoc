---
layout: falloutnvrec
title: fopdoc
---
CONT
====

Container

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
-* | | [Item](Subrecords/Item.html) | collection |
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | [DATA](#data) | Data | struct |
 | SNAM | Sound - Open | formid | FormID of a [SOUN](SOUN.html) record.
 | QNAM | Sound - Close | formid | FormID of a [SOUN](SOUN.html) record.
 | RNAM | Sound - Random/Looping | formid | FormID of a [SOUN](SOUN.html) record.


### DATA

Name | Type | Info
-----|------|-----
Flags | uint8 | See below for values.
Weight | float32 |

#### Flag Values

Value | Meaning
------|--------
0x01 | ??
0x02 | Respawns

