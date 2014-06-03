CPTH
====

Camera Path

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
-* | [CTDA](Fields/CTDA.md) | Condition | struct |
+* | ANAM | Related Camera Path | formid | FormID of a [CPTH](CPTH.md) record, or null. The first ANAM subrecord maps to the parent, the second maps to the previous sibling.
+ | DATA | Camera Zoom | uint8 | Enum - see below for values.
-* | SNAM | Camera Shot | formid | FormID of a [CAMS](CAMS.md) record.

### DATA Enum Values

Value | Meaning
------|--------
0 | Default
1 | Disable
2 | Shot List
