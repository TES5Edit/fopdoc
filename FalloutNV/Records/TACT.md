---
layout: falloutnvrec
title: fopdoc
---
TACT
====

Talking Activator

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | SNAM | Looping Sound | formid | FormID of a [SOUN](SOUN.html) record.
 | VNAM | Voice Type | formid | FormID of a [VTYP](VTYP.html) record.
 | INAM | Radio Template | formid | FormID of a [SOUN](SOUN.html) record.

