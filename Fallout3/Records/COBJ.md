---
layout: fallout3rec
title: fopdoc
---
COBJ
====

Constructible Object

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
+ | DATA | | struct |
 
### DATA

Name | Type | Info
-----|------|-----
Value | int32 |
Weight | float32 |
 
