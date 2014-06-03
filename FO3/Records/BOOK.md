BOOK
====

Book

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | collection |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
+ | DESC | Description | cstring |
 | | [Destruction Data](Fields/Destruction.md) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | DATA | Data | struct |

### DATA

Name | Type | Info
-----|------|-----
Flags | uint8 |
[Skill](Values/Skills.md) | int8 | See the link for enum values.
Value | int32 |
Weight | float32 |

#### Flag Values

Value | Meaning
------|--------
0x01 | Unknown
0x02 | Can't be taken
