---
layout: fallout3rec
title: fopdoc
---
TACT
====

Talking Activator

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.md) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Subrecords/Destruction.md) | collection |
 | SNAM | Sound | formid | FormID of a [SOUN](SOUN.md) record.
 | VNAM | Voice Type | formid | FormID of a [VTYP](VTYP.md) record.
 
