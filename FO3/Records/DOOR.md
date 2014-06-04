DOOR
====

Door

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.md) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Subrecords/Destruction.md) | collection |
 | SNAM | Sound - Open | formid | FormID of a [SOUN](SOUN.md) record.
 | ANAM | Sound - Close | formid | FormID of a [SOUN](SOUN.md) record.
 | BNAM | Sound - Looping | formid | FormID of a [SOUN](SOUN.md) record.
+ | FNAM | Flags | uint8 | See below for values.

### Flag Values

Value | Meaning
------|--------
0x01 | ??
0x02 | Automatic Door
0x04 | Hidden
0x08 | Minimal Use
0x10 | Sliding Door
