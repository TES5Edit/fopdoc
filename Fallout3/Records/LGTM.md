---
layout: fallout3rec
title: fopdoc
---
LGTM
====

Lighting Template

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | DATA | Lighting | struct |

### DATA

Name | Type | Info
-----|------|-----
Ambient Color | rgba |
Directional Color | rgba |
Fog Color | rgba |
Fog Near | float32 |
Fog Far | float32 |
Directional Rotation XY | int32 |
Directional Rotation Z | int32 |
Directional Fade | float32 |
Fog Clip Distance | float32 |
Fog Power | float32 |
