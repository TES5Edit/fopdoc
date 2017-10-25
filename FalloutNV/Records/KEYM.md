---
layout: falloutnvrec
title: fopdoc
---
KEYM
====

Key

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
+ | ICON | Large Icon Filename | cstring |
+ | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
 | DATA | | struct |
 | RNAM | Sound - Random/Looping | formid | FormID of a [SOUN](SOUN.html) record.

### DATA

Name | Type | Info
-----|------|-----
Value | int32 |
Weight | float32 |

