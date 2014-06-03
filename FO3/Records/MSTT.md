MSTT
====

Moveable Static

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | collection |
 | | [Destruction Data](Fields/Destruction.md) | collection |
+ | DATA | Unknown | byte |
 | SNAM | Sound | formid | FormID of a [SOUN](SOUN.md) record.

