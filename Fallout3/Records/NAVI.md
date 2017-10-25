---
layout: fallout3rec
title: fopdoc
---
NAVI
====

Navigation Mesh Info Map

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | NVER | Version | uint32 |
-* | NVMI | Navigation Map Info | struct |
-* | NVCI | Unknown | struct |

### NVMI

Name | Type | Info
-----|------|-----
Unknown | byte[4] |
Navigation Mesh | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.md), [FNV](../../FalloutNV/Records/NAVM.md)) record.
Location | formid | FormID of a CELL ([FO3](../../Fallout3/Records/CELL.md), [FNV](../../FalloutNV/Records/CELL.md)) or WRLD ([FO3](../../Fallout3/Records/WRLD.md), [FNV](../../FalloutNV/Records/WRLD.md)) record.
Grid X | int16 |
Grid Y | int16 |
Unknown | uint8[] |

### NVCI

Count | Name | Type | Info
------|------|------|-----
 | Unknown | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.md), [FNV](../../FalloutNV/Records/NAVM.md)) record.
-* | Unknown | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.md), [FNV](../../FalloutNV/Records/NAVM.md)) record.
-* | Unknown | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.md), [FNV](../../FalloutNV/Records/NAVM.md)) record.
-* | Door | formid | FormID of a REFR ([FO3](../../Fallout3/Records/REFR.md), [FNV](../../FalloutNV/Records/REFR.md)) record.
