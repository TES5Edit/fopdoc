ALCH Record
===========

Ingestible

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Subrecords/Destruction.md) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | [ETYP](Subrecords/ETYP.md) | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | [ENIT](#enit) | Effect Data | struct |
+* | | [Effect](Subrecords/Effect.md) | collection |

### ENIT

Name | Type | Info
-----|------|-----
Value | int32 |
Flags | uint8 | See below for flags.
Unused | byte[3] |
Withdrawal Effect | formid | FormID of a [SPEL](SPEL.md) record, or null.
Addiction Chance | float32 |
Sound - Consume | formid | FormID of a [SOUN](SOUN.md) record, or null.

#### Flag Values

Flag | Meaning
-----|--------
0x01 | No Auto-Calc (Unused)
0x02 | Food Item
0x04 | Medicine

