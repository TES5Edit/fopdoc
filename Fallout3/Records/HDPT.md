---
layout: fallout3rec
title: fopdoc
---
HDPT
====

Head Part

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
+ | DATA | Flags | uint8 | See below for values.
-* | HNAM | Extra Parts | formid | FormID of a [HDPT](HDPT.md) record.


### DATA Flag Values

Value | Meaning
------|--------
0x01 | Playable
