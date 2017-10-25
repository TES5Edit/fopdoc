---
layout: fallout3rec
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

### LNAM

Name | Type | Info
-----|------|-----
Cell | formid | FormID of a [CELL](CELL.html) or [WRLD](WRLD.html) record.
Unused | byte[8] |

