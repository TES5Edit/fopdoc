AMMO
====

Ammunition

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
 | ICON | Large Icon Filename | cstring | 
 | MICO | Small Icon FIlename | cstring |
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | [DATA](#data) | Data | struct 
 | ONAM | Short Name | cstring |
 
### DATA

Name | Type | Info
-----|------|-----
Speed | float32 |
Flags | uint8 | See below for values
Unused | uint8[3] |
Value | int32 |
Clip Rounds | uint8 |
 
#### Flag Values

Flag | Meaning
-----|--------
0x01 | Ignores Normal Weapon Resistance
0x02 | Non-Playable
 
