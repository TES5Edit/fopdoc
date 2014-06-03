LSCR
====

Load Screen

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | ICON | Large icon filename | cstring |
+ | MICO | Small icon filename | cstring |
+ | DESC | Description | cstring |
-* | LNAM | Location | struct |

### LNAM

Name | Type | Info
-----|------|-----
Cell | formid | FormID of a [CELL](CELL.md) or [WRLD](WRLD.md) record.
Unused | uint8[8] |

