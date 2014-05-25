HDPT
====

Head Part

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
+ | DATA | Flags | uint8 | See below for values.
-* | HNAM | Extra Parts | formid | FormID of a [HDPT](HDPT.md) record.


### DATA Flag Values

Value | Meaning
------|--------
0x01 | Playable
