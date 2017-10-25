---
layout: falloutnvrec
title: fopdoc
---
DEBR
====

Debris

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+* | | Debris Model | collection | See below for details.

### Debris Model Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | DATA | Data | struct |
+ | MODT | Texture File Hashes | ?? |

#### DATA

Name | Type | Info
-----|------|-----
Percentage | uint8 |
Model Filename | cstring |
Flags | uint8 | See below for values.

##### Flag Values

Value | Meaning
------|--------
0x01 | Has Collision Data
