---
layout: fallout3rec
title: fopdoc
---
BOOK
====

Book

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
+ | DESC | Description | cstring |
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
+ | DATA | Data | struct |

### DATA

Name | Type | Info
-----|------|-----
Flags | uint8 |
[Skill](Values/Skills.html) | int8 | See the link for enum values.
Value | int32 |
Weight | float32 |

#### Flag Values

Value | Meaning
------|--------
0x01 | Unknown
0x02 | Can't be taken
