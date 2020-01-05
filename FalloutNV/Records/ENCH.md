---
layout: falloutnvrec
title: fopdoc
---
ENCH
====

Object Effect

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
+ | ENIT | Effect Data | struct |
+* | | [Effect](Subrecords/Effect.md) | collection |

### ENIT

Name | Type | Info
-----|------|-----
Type | uint32 |
Unused | byte[4] |
Unused | byte[4] |
Flags | uint8 |
Unused | byte[3] |
