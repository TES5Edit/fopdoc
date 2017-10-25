---
layout: fallout3rec
title: fopdoc
---
DOOR
====

Door

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | SNAM | Sound - Open | formid | FormID of a [SOUN](SOUN.html) record.
 | ANAM | Sound - Close | formid | FormID of a [SOUN](SOUN.html) record.
 | BNAM | Sound - Looping | formid | FormID of a [SOUN](SOUN.html) record.
+ | FNAM | Flags | uint8 | See below for values.

### Flag Values

Value | Meaning
------|--------
0x01 | ??
0x02 | Automatic Door
0x04 | Hidden
0x08 | Minimal Use
0x10 | Sliding Door
