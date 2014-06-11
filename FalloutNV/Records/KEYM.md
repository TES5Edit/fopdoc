KEYM
====

Key

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
+ | ICON | Large Icon Filename | cstring |
+ | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Subrecords/Destruction.md) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
 | DATA | | struct |
 | RNAM | Sound - Random/Looping | formid | FormID of a [SOUN](SOUN.md) record.

### DATA

Name | Type | Info
-----|------|-----
Value | int32 |
Weight | float32 |

