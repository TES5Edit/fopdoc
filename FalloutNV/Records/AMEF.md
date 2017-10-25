---
layout: falloutnvrec
title: fopdoc
---
AMEF
====

Ammo Effect

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
 | DATA | Data | struct |

### DATA

Name | Type | Info
-----|------|-----
Type | uint32 | Enum - see values below.
Operation | uint32 | Enum - see values below.
Value | float32 |

#### Type Values

Value | Meaning
------|--------
0 | Damage Mod
1 | DR Mod
2 | DT Mod
3 | Spread Mod
4 | Weapon Condition Mod
5 | Fatigue Mod

#### Operation Values

Value | Meaning
------|--------
0 | Add
1 | Multiply
2 | Subtract
