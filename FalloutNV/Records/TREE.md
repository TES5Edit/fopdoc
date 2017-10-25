---
layout: falloutnvrec
title: fopdoc
---
TREE
====

Tree

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | | [Model Data](Subrecords/Model.html) | collection |
+ | ICON | Large icon filename | cstring |
+ | MICO | Small icon filename | cstring |
+ | SNAM | SpeedTree Seeds | uint32[] |
+ | CNAM | Tree Data | struct |
+ | BNAM | Billboard Dimensions | struct |

### CNAM

Name | Type | Info
-----|------|-----
Leaf Curvature | float32 |
Minimum Leaf Angle | float32 |
Maximum Leaf Angle | float32 |
Branch Dimming Value | float32 |
Leaf Dimming Value | float32 |
Shadow Radius | int32 |
Rock Speed | float32 |
Rustle Speed | float32 |

### BNAM

Name | Type | Info
-----|------|-----
Width | float32 |
Height | float32 |
