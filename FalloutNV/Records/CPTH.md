---
layout: falloutnvrec
title: fopdoc
---
CPTH
====

Camera Path

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
-* | [CTDA](Subrecords/CTDA.html) | Condition | struct |
 | ANAM | Related Camera Paths | struct |
+ | DATA | Camera Zoom | uint8 | Enum - see below for values.
-* | SNAM | Camera Shot | formid | FormID of a [CAMS](CAMS.html) record.

### ANAM

Name | Type | Info
-----|------|-----
Parent Camera Path | formid | FormID of a [CPTH](CPTH.html) record, or null.
Previous Sibling Camera Path | formid | FormID of a [CPTH](CPTH.html) record, or null.

### DATA Enum Values

Value | Meaning
------|--------
0 | Default
1 | Disable
2 | Shot List
