---
layout: fallout4rec
title: fopdoc
---
TXST
====

Texture Set

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | TX00 | Base Image / Transparency | cstring | The alpha channel holds the transparency data.
 | TX01 | Normal Map / Specular | cstring | The alpha channel holds the specular data.
 | TX03 | Glow Map | cstring |
 | TX04 | Parallax Map | cstring |
 | TX05 | Enviroment Map | cstring |
 | TX06 | Enviroment Map | cstring |
 | TX02 | Environment Map Mask | cstring |
 | TX07 | Enviroment Map | cstring |
 | [DODT](Subrecords/DODT.md) | Decal Data | struct |
+ | DNAM | Flags | uint16 | See below for values.
 | MNAM | Filename | cstring |
 

### DNAM Flag Values

Value | Meaning
------|--------
0x0001 | No Specular Map
