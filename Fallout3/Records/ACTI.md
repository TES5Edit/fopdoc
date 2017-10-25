---
layout: fallout3rec
title: fopdoc
---
ACTI Record
===========

Activator

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
- | FULL | Name | cstring | Activator name
- | | [Model Data](Subrecords/Model.html) | collection |
- | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
- | | [Destruction Data](Subrecords/Destruction.html) | collection |
- | SNAM | Sound - Looping | formid | FormID of a [SOUN](SOUN.html) record.
- | VNAM | Sound - Activation | formid | FormID of a [SOUN](SOUN.html) record.
- | RNAM | Radio Station | formid | FormID of a [TACT](TACT.html) record.
- | WNAM | Water Type | formid | FormID of a [WATR](WATR.html) record.




