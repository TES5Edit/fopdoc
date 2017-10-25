---
layout: falloutnvrec
title: fopdoc
---
LSCR
====

Load Screen

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | ICON | Large icon filename | cstring |
+ | MICO | Small icon filename | cstring |
+ | DESC | Description | cstring |
-* | LNAM | Location | struct |
 | WMI1 | Load Screen Type | formid | FormID of a [LSCT](LSCT.html) record.

### LNAM

Name | Type | Info
-----|------|-----
Direct | formid | FormID of a [CELL](CELL.html) or [WRLD](WRLD.html) record, or null.
Indirect - World | formid | FormID of a [WRLD](WRLD.html) record, or null.
Indirect - Grid Y | int16 |
Indirect - Grid X | int16 |
