---
layout: fallout3rec
title: fopdoc
---
INGR
====

Ingredient

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
+ | [ETYP](Subrecords/ETYP.html) | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | ENIT | Effect Data | struct |
+* | | [Effect](Subrecords/Effect.html) | collection |

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
