INGR
====

Ingredient

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
+ | [ETYP](Fields/ETYP.md) | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | ENIT | Effect Data | struct |
+* | | [Effect](Fields/Effect.md) | | This is a field collection.

### ENIT

Count | Name | Type | Info
------|------|------|-----
 | Value | int32 |
 | Flags | uint8 | See below for values.
 | Unused | uint8[3] |
 
#### Flag Values

Value | Meaning
------|--------
0x01 | No Auto-Calculation
0x02 | Food Item
