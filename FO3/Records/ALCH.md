ALCH Record
===========

Ingestible

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
 | ICON | Large Icon Filename | cstring | 
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | [ETYP](Fields/ETYP.md) | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | [ENIT](#enit) | Effect Data | struct |
+* | | [Effect](Fields/Effect.md) | | This is a field collection.

### ENIT

Count | Name | Type | Info
------|------|------|-----
 | Value | int32 |
 | Flags | uint8 | See below for flags.
 | Unused | uint8[3] | ??
 | Withdrawal Effect | formid | FormID of a [SPEL](SPEL.md) record, or null.
 | Addiction Chance | float32 |
 | Sound - Consume | formid | FormID of a [SOUN](SOUN.md) record.

#### Flag Values

Flag | Meaning
-----|--------
0x01 | No Auto-Calc (Unused)
0x02 | Food Item
0x04 | Medicine

