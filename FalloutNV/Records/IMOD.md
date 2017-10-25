---
layout: falloutnvrec
title: fopdoc
---
IMOD
====

Item Mod

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | DESC | Description | cstring |
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
 | DATA | Data | struct |

### DATA

Name | Type | Info
-----|------|-----
Value | uint32 |
Weight | float32 |