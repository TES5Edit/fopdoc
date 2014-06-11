AMMO
====

Ammunition

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
 | | [Destruction Data](Subrecords/Destruction.md) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | [DATA](#data) | Data | struct |
 | ONAM | Short Name | cstring |

### DATA

Name | Type | Info
-----|------|-----
Speed | float32 |
Flags | uint8 | See below for values
Unused | byte[3] |
Value | int32 |
Clip Rounds | uint8 |

#### Flag Values

Flag | Meaning
-----|--------
0x01 | Ignores Normal Weapon Resistance
0x02 | Non-Playable

