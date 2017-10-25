---
layout: fallout3rec
title: fopdoc
---
MSTT
====

Moveable Static

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
+ | DATA | Unknown | byte |
 | SNAM | Sound | formid | FormID of a SOUN ([FO3](../../Fallout3/Records/SOUN.html), [FNV](../../FalloutNV/Records/SOUN.html)) record.

