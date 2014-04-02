ACTI Record
===========

Activator

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
- | FULL | Name | cstring | Activator name
- | | [Model Data](Fields/Model.md) | | This is a field collection.
- | SCRI | Script | formid | FormID of a SCPT record.
- | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
- | SNAM | Sound - Looping | formid | FormID of a SOUN record.
- | VNAM | Sound - Activation | formid | FormID of a SOUN record.
- | RNAM | Radio Station | formid | FormID of a TACT record.
- | WNAM | Water Type | formid | FormID of a WATR record.




