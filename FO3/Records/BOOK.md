BOOK
====

Book

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Male Biped Model Data](Fields/Model.md) | | This is a field collection.
 | ICON | Large icon filename | cstring | 
 | MICO | Small icon filename | cstring | 
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
+ | DESC | Description | cstring |
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | DATA | Data | struct |

### DATA

Count | Name | Type | Info
------|------|------|-----
 | Flags | uint8 |
 | Skill | int8 | Enum
 | Value | int32 |
 | Weight | float32 |

#### Flag Values

Value | Meaning
------|--------
0x01 | Unknown
0x02 | Can't be taken

#### Skill Enum Values

Value | Meaning
------|--------
-1 | None
0 | Barter
1 | Big Guns
2 | Energy Weapons
3 | Explosives
4 | Lockpick
5 | Medicine
6 | Melee Weapons
7 | Repair
8 | Science
9 | Small Guns
10 | Sneak
11 | Speech
12 | Throwing (unused)
13 | Unarmed
