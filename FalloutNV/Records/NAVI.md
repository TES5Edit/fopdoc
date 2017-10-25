---
layout: falloutnvrec
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
Navigation Mesh | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.html), [FNV](../../FalloutNV/Records/NAVM.html)) record.
Location | formid | FormID of a CELL ([FO3](../../Fallout3/Records/CELL.html), [FNV](../../FalloutNV/Records/CELL.html)) or WRLD ([FO3](../../Fallout3/Records/WRLD.html), [FNV](../../FalloutNV/Records/WRLD.html)) record.
Grid X | int16 |
Grid Y | int16 |
Unknown | uint8[] |

### NVCI

Count | Name | Type | Info
------|------|------|-----
 | Unknown | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.html), [FNV](../../FalloutNV/Records/NAVM.html)) record.
-* | Unknown | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.html), [FNV](../../FalloutNV/Records/NAVM.html)) record.
-* | Unknown | formid | FormID of a NAVM ([FO3](../../Fallout3/Records/NAVM.html), [FNV](../../FalloutNV/Records/NAVM.html)) record.
-* | Door | formid | FormID of a REFR ([FO3](../../Fallout3/Records/REFR.html), [FNV](../../FalloutNV/Records/REFR.html)) record.
