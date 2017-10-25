---
layout: fallout3rec
title: fopdoc
---
FURN
====

Furniture

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
+ | MNAM | Marker Flags | uint8[] |
