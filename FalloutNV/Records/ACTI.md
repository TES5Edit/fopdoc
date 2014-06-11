ACTI Record
===========

Activator

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
- | FULL | Name | cstring | Activator name
- | | [Model Data](Subrecords/Model.md) | collection |
- | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
- | | [Destruction Data](Subrecords/Destruction.md) | collection |
- | SNAM | Sound - Looping | formid | FormID of a [SOUN](SOUN.md) record.
- | VNAM | Sound - Activation | formid | FormID of a [SOUN](SOUN.md) record.
- | INAM | Radio Template | formid | FormID of a [SOUN](SOUN.md) record.
- | RNAM | Radio Station | formid | FormID of a [TACT](TACT.md) record.
- | WNAM | Water Type | formid | FormID of a [WATR](WATR.md) record.
- | XATO | Activation Prompt | cstring |
