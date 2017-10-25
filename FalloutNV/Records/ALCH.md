---
layout: falloutnvrec
title: fopdoc
---
ALCH Record
===========

Ingestible

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
+ | [ETYP](Subrecords/ETYP.html) | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | [ENIT](#enit) | Effect Data | struct |
+* | | [Effect](Subrecords/Effect.html) | collection |

### ENIT

Name | Type | Info
-----|------|-----
Value | int32 |
Flags | uint8 | See below for flags.
Unused | byte[3] |
Withdrawal Effect | formid | FormID of a [SPEL](SPEL.html) record, or null.
Addiction Chance | float32 |
Sound - Consume | formid | FormID of a [SOUN](SOUN.html) record, or null.

#### Flag Values

Flag | Meaning
-----|--------
0x01 | No Auto-Calc (Unused)
0x02 | Food Item
0x04 | Medicine

