MSTT
====

Moveable Static

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | | This is a field collection.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
+ | DATA | Unknown | uint8 |
 | SNAM | Sound | formid | FormID of a [SOUN](SOUN.md) record.

