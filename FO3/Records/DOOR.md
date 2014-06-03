DOOR
====

Door

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Fields/Destruction.md) | collection |
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
