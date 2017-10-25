---
layout: fallout3rec
title: fopdoc
---
DODT Subrecord
==========

## Format

Name | Type | Info
-----|------|-----
Min Width | float32 |
Max Width | float32 |
Min Height | float32 |
Max Height | float32 |
Depth | float32 |
Shininess | float32 |
Parallax Scale | float32 |
Parallax Passes | uint8 |
Flags | uint8 | See below for values.
Unused | byte[2] | 
Color | rgba |
 
### Flag Values

Value | Meaning
------|--------
0x01 | Parallax
0x02 | Aplha - Blending
0x04 | Alpha - Testing
