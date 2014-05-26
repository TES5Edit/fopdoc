GRAS
====

Grass

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | | [Model Data](Fields/Model.md) | | This is a field collection.
+ | DATA | | struct |

### DATA

Count | Name | Type | Info
------|------|------|-----
 | Density | uint8 |
 | Min Slope | uint8 |
 | Max Slope | uint8 |
 | Unused | uint8 |
 | Unit From Water Amount | uint16 |
 | Unused | uint8[2] |
 | Unit From Water Type | uint32 | Enum - see below for values.
 | Position Range | float32 |
 | Height Range | float32 |
 | Color Range | float32 |
 | Wave Period | float32 |
 | Flags | uint8 | See below for values.
 | Unused | uint8[3] |
 
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
