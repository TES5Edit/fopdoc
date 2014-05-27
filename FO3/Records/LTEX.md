LTEX
====

Landscape Texture

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | ICON | Large icon filename | cstring |
+ | MICO | Small icon filename | cstring |
+ | TNAM | Texture | formid | FormID of a [TXST](TXST.md) record.
+ | HNAM | Havok Data | struct |
+ | SNAM | Texture Specular Exponent | uint8 |
-* | GNAM | Grass | formid | FormID of a [GRAS](GRAS.md) record.

### HNAM

Count | Name | Type | Info
------|------|------|-----
 | Material Type | uint8 | Enum - see below for values.
 | Friction | uint8 |
 | Restitution | uint8 |
 
#### Material Type Enum Values

Value | Meaning
------|--------
0 | Stone
1 | Cloth
2 | Dirt
3 | Glass
4 | Grass
5 | Metal
6 | Organic
7 | Skin
8 | Water
9 | Wood
10 | Heavy Stone
11 | Heavy Metal
12 | Heavy Wood
13 | Chain
14 | Snow
15 | Elevator
16 | Hollow Metal
17 | Sheet Metal
18 | Sand
19 | Broken Concrete
20 | Vehicle Body
21 | Vehicle Part Solid
22 | Vehicle Part Hollow
23 | Barrel
24 | Bottle
25 | Soda Can
26 | Pistol
27 | Rifle
28 | Shopping Cart
29 | Lunchbox
30 | Baby Rattle
31 | Rubber Ball
