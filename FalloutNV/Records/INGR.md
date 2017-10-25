---
layout: falloutnvrec
title: fopdoc
---
INGR
====

Ingredient

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
+ | [ETYP](Subrecords/ETYP.md) | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | ENIT | Effect Data | struct |
+* | | [Effect](Subrecords/Effect.md) | collection |

### ENIT

Name | Type | Info
-----|------|-----
Value | int32 |
Flags | uint8 | See below for values.
Unused | byte[3] |
 
#### Flag Values

Value | Meaning
------|--------
0x01 | No Auto-Calculation
0x02 | Food Item
