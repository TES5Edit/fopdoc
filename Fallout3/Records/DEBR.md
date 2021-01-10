---
layout: fallout3rec
title: fopdoc
---
DEBR Record
===========

Debris

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
+* | | Debris Model | collection | See below for details.

### Debris Model Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | DATA | Data | struct | See below for details.
- | [MODT](Subrecords/MODT.md) | Texture Filename Hashes | struct[] |

#### DATA Subrecord

Name | Type | Info
-----|------|-----
Percentage | uint8 |
Model Filename | cstring |
Flags | uint8 | See below for values.

##### Flag Values

Value | Meaning
------|--------
0x01 | Has Collision Data
