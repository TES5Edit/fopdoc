---
layout: falloutnvrec
title: fopdoc
---
Destruction Subrecord Collection
============================

The DEST, DSTD, DMDL, DMDT and DSTF subrecords hold destruction data, and always appear together.

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | DEST | Header | struct |
-* | | Destruction Stage | collection | See below for details.

### DEST

Name | Type | Info
-----|------|-----
Health | int32 |
Count | uint8 |
Flags | uint8 | See below for values.
unknown | byte[2] | ??

#### DEST Flag Values

Value | Meaning
------|--------
0x01 | VATS Targetable

### Destruction Stage

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | DSTD | Stage Data | struct |
- | DMDL | Stage Model Filename | cstring |
- | DMDT | Stage Model Texture Files Hashes | ?? | ??
- | DSTF | Stage End Marker | null |


#### DSTD

Name | Type | Info
-----|------|-----
Health Percentage | uint8 |
Index | uint8 |
Damage Stage | uint8 |
Flags | uint8 | See below for values.
Self Damage per Second | int32 |
Explosion | formid | FormID of a [EXPL](../EXPL.md) record or null.
Debris | formid | FormID of a [DEBR](../DEBR.md) record or null.
Debris Count | int32 |

##### DSTD Flag Values

Value | Meaning
------|--------
0x01 | Cap Damage
0x02 | Disable
0x04 | Destroy
