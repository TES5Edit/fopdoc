---
layout: fallout3rec
title: fopdoc
---
CLMT
====

Climate

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | WLST | Weather Types | struct |
 | FNAM | Sun Texture | cstring |
 | GNAM | Sun Glare Texture | cstring |
- | | [Model Data](Subrecords/Model.html) | collection |
+ | TNAM | Timing | struct |


### WLST

The WLST subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Weather | formid | FormID of a [WTHR](WTHR.html) record, or null.
Chance | int32 |
Global | formid | FormID of a [GLOB](GLOB.html) record, or null.

### TNAM

Name | Type | Info
-----|------|-----
Sunrise Begin | uint8 |
Sunrise End | uint8 |
Sunset Begin | uint8 |
Sunset End | uint8 |
Volatility | uint8 |
Moons / Phase Length | uint8 |
