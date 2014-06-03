MISC
====

Misc Item

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | DATA | | struct |
 
### DATA

Name | Type | Info
-----|------|-----
Value | int32 |
Weight | float32 |
