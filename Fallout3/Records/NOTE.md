---
layout: fallout3rec
title: fopdoc
---
NOTE
====

Note

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | ICON | Large Icon Filename | cstring | 
 | MICO | Small Icon FIlename | cstring |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
 | DATA | Type | uint8 | Enum - see values below.
-* | ONAM | Quest | formid | FormID of a [QUST](QUST.html) record.
 | XNAM | Texture | cstring |
 | TNAM | Text / Topic | cstring *or* formid | A text string, or the FormID of a [DIAL](DIAL.html) record.
 | SNAM | Sound / NPC | formid | FormID of a [SOUN](SOUN.html) or [NPC_](NPC_.html) record.
 
### DATA Enum Values

Value | Meaning
------|--------
0 | Sound
1 | Text
2 | Image
3 | Voice

