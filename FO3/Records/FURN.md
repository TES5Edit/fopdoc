FURN
====

Furniture

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Fields/Destruction.md) | collection |
+ | MNAM | Marker Flags | uint8[] |
