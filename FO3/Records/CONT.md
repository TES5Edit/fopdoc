CONT
====

Container

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | 
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | | This is a field collection.
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
-* | | [Item](Fields/Item.md) | | This is a field collection.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
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
 
