NAVI
====

Navigation Mesh Info Map

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | NVER | Version | uint32 |
-* | NVMI | Navigation Map Info | struct |
-* | NVCI | Unknown | struct |

### NVMI

Name | Type | Info
-----|------|-----
Unknown | byte[4] | 
Navigation Mesh | formid | FormID of a [NAVM](NAVM.md) record.
Location | formid | FormID of a [CELL](CELL.md) or [WRLD](WRLD.md) record.
Grid X | int16 |
Grid Y | int16 |
Unknown | uint8[] |

### NVCI

Count | Name | Type | Info
------|------|------|-----
 | Unknown | formid | FormID of a [NAVM](NAVM.md) record.
-* | Unknown | formid | FormID of a [NAVM](NAVM.md) record.
-* | Unknown | formid | FormID of a [NAVM](NAVM.md) record.
-* | Door | formid | FormID of a [DOOR](DOOR.md) record.
