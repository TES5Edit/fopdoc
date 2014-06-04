LIGH
====

Light

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | | [Model Data](Subrecords/Model.md) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | FULL | Name | cstring |
 | ICON | Large Icon Filename | cstring | 
 | MICO | Small Icon FIlename | cstring |
+ | DATA | | struct |
+ | FMAM | Fade Value | foat32 |
 | SNAM | Sound | formid | FormID of a [SOUN](SOUN.md) record.
 
### DATA

Name | Type | Info
------|------|------|-----
Time | int32 |
Radius | uint32 |
Color | rbga |
Flags | uint32 | See below for values.
Falloff Exponent | float32 |
FOV | float32 |
Value | uint32 |
Weight | float32 |
 
#### Flag Values

Value | Meaning
------|--------
0x00000001 | Dynamic
0x00000002 | Can be Carried
0x00000004 | Negative
0x00000008 | Flicker
0x00000010 | Unused
0x00000020 | Off By Default
0x00000040 | Flicker Slow
0x00000080 | Pulse
0x00000100 | Pulse Slow
0x00000200 | Spot Light
0x00000400 | Spot Shadow

