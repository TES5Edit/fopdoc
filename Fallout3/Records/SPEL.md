---
layout: fallout3rec
title: fopdoc
---
SPEL
====

Actor Effect

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
+ | SPIT | | struct |
+* | | [Effect](Subrecords/Effect.html) | collection |

### SPIT

Name | Type | Info
-----|------|-----
Type | uint32 | Enum - see below for values.
Cost | uint32 | Unused
Level | uint32 | Unused
Flags | uint8 |
Unused | byte[3] |

#### Type Values

Value | Meaning
-----|--------
0 | Actor Effect
1 | Disease
2 | Power
3 | Lesser Power
4 | Ability
5 | Poison
6 | ??
7 | ??
8 | ??
9 | ??
10 | Addiction

#### Flag Values

Value | Meaning
-----|--------
0x01 | No Auto-Calc
0x02 | Immune To Silence 1?
0x04 | PC Start Effect
0x08 | Immune To Silence 2?
0x10 | Area Effect Ignores LOS
0x20 | Script Effect Always Applies
0x40 | Disable Absorb / Reflect
0x80 | Force Touch Explode
