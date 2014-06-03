CONT
====

Container

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | 
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | collection | 
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
-* | | [Item](Fields/Item.md) | collection | 
 | | [Destruction Data](Fields/Destruction.md) | collection |
 | [DATA](#data) | Data | struct | 
 | SNAM | Sound - Open | formid | FormID of a [SOUN](SOUN.md) record.
 | QNAM | Sound - Close | formid | FormID of a [SOUN](SOUN.md) record.
 

### DATA

Name | Type | Info
-----|------|-----
Flags | uint8 | See below for values.
Weight | float32 | 
 
#### Flag Values

Value | Meaning
------|--------
0x01 | ??
0x02 | Respawns
 
