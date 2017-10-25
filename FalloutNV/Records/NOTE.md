---
layout: falloutnvrec
title: fopdoc
---
NOTE
====

Note

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
 | DATA | Type | uint8 | Enum - see values below.
-* | ONAM | Quest | formid | FormID of a [QUST](QUST.md) record.
 | XNAM | Texture | cstring |
 | TNAM | Text / Topic | cstring *or* formid | A text string, or the FormID of a [DIAL](DIAL.md) record.
 | SNAM | Sound / Actor | formid | FormID of a [SOUN](SOUN.md), [NPC_](NPC_.md) or [CREA](CREA.md) record.

### DATA Enum Values

Value | Meaning
------|--------
0 | Sound
1 | Text
2 | Image
3 | Voice

