---
layout: fallout3rec
title: fopdoc
---
RADS
====

Radiation Stage

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | DATA | | struct |

### DATA

Name | Type | Info
-----|------|-----
Trigger Threshold | uint32 |
Actor Effect | formid | FormID of a [SPEL](SPEL.html) record.

