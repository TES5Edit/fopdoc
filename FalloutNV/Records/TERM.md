---
layout: falloutnvrec
title: fopdoc
---
TERM
====

Terminal

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
+ | DESC | Description | cstring |
 | SNAM | Sound - Looping | formid | FormID of a [SOUN](SOUN.html) record.
 | PNAM | Password Note | formid | FormID of a [NOTE](NOTE.html) record.
+ | DNAM | | struct |
-* | | Menu Item | collection | See below for details.

### DNAM

Name | Type | Info
-----|------|-----
Base Hacking Difficulty | uint8 | Enum - see below for values.
Flags | uint8 | See below for values.
Server Type | uint8 | Enum - see below for values.
Unused | byte |

#### Base Hacking Difficulty Enum Values

Value | Meaning
------|--------
0 | Very Easy
1 | Easy
2 | Average
3 | Hard
4 | Very Hard
5 | Requires Key

#### Flag Values

Value | Meaning
------|--------
0x01 | Leveled
0x02 | Unlocked
0x04 | Alternate Colors
0x08 | Hide Welcome Text When Displaying Text

#### Server Type Enum Values

Value | Meaning
------|--------
0 | -Server 1-
1 | -Server 2-
2 | -Server 3-
3 | -Server 4-
4 | -Server 5-
5 | -Server 6-
6 | -Server 7-
7 | -Server 8-
8 | -Server 9-
9 | -Server 10-

### Menu Item Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | ITXT | Item Text | cstring |
+ | RNAM | Result Text | cstring |
+ | ANAM | Flags | uint8 | See below for values.
 | INAM | Display Note | formid | FormID of a [NOTE](NOTE.html) record.
 | TNAM | Sub Menu | formid | FormID of a [TERM](TERM.html) record.
+ | | [Embedded Script](Subrecords/Script.html) | collection |
-* | [CTDA](Subrecords/CTDA.html) | Condition | struct |

#### AMAN Flag Values

Value | Meaning
------|--------
0x01 | Add Note
0x02 | Force Redraw
