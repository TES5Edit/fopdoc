LAND
====

Landscape

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | DATA | Unknown | uint8[] | 
-* | VNML | Vertex Normal | struct | There are 33 VNML structs.
 | VHGT | Vertex Height Map | struct |
-* | VCLR | Vertex Color |
-* | | Layer Field Collection | | A field collection, see below for details.
-* | VTEX | Texture | formid | FormID of an [LTEX](LTEX.md) record, or null.

### VNML / VCLR

Each VNML / VCLR structure contains 33 repeats of the following structure, so that the array of VNML / VCLR structs forms a 33x33 grid where each VNML / VCLR is a row, and each instance of the structure below is a column.

Count | Name | Type | Info
------|------|------|-----
 | X | uint8 |
 | Y | uint8 |
 | Z | uint8 |

### VHGT

Count | Name | Type | Info
------|------|------|-----
 | Offset | float32 |
-* | Row | struct | There are 33 row structs. Each row struct contains 33 `uint8` fields, representing 33 columns.
 | Unused | uint8[3] |
 
### Layer Field Collection

Each layer can be a base layer or an alpha layer, which have different structures.

#### Base Layer

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | BTXT | Base Layer Header | struct | 
 
##### BTXT / ATXT

Count | Name | Type | Info
------|------|------|-----
 | Texture | formid | FormID of a [LTEX](LTEX.md) record, or null.
 | Quadrant | uint8 | Enum - see below for values.
 | Unused | uint8 |
 | Layer | int16 |
 
###### Quadrant Enum Values

Value | Meaning
------|--------
0 | Bottom Left
1 | Bottom Right
2 | Top Left
3 | Top Right
 
#### Alpha Layer

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | ATXT | Alpha Layer Header | struct |
-* | VTXT | Alpha Layer Cell Data | struct |

##### VTXT

Count | Name | Type | Info
------|------|------|-----
 | Position | uint16 |
 | Unused | uint8[2] |
 | Opacity | float32 |

