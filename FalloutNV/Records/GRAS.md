---
layout: falloutnvrec
title: fopdoc
---
GRAS
====

Grass

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | | [Model Data](Subrecords/Model.html) | collection |
+ | DATA | | struct |

### DATA

Name | Type | Info
-----|------|-----
Density | uint8 |
Min Slope | uint8 |
Max Slope | uint8 |
Unused | byte |
Unit From Water Amount | uint16 |
Unused | byte[2] |
Unit From Water Type | uint32 | Enum - see below for values.
Position Range | float32 |
Height Range | float32 |
Color Range | float32 |
Wave Period | float32 |
Flags | uint8 | See below for values.
Unused | byte[3] |
 
#### Unit From Water Type Enum Values

Value | Meaning
------|--------
0 | Above - At Least
1 | Above - At Most
2 | Below - At Least
3 | Below - At Most
4 | Either - At Least
5 | Either - At Most
6 | Either - At Most Above
7 | Either - At Most Below

#### Flag Values

Value | Meaning
------|--------
0x01 | Vertex Lighting
0x02 | Uniform Scaling
0x04 | Fit To Slope
