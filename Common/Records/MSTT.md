MSTT
====

Moveable Static

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.md) | collection |
 | | [Destruction Data](Subrecords/Destruction.md) | collection |
+ | DATA | Unknown | byte |
 | SNAM | Sound | formid | FormID of a [SOUN](SOUN.md) record.

