---
layout: falloutnvrec
title: fopdoc
---
LAND
====

Landscape

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | DATA | Unknown | uint8[] |
 | VNML | Vertex Normals | struct |
 | VHGT | Vertex Height Map | struct |
 | VCLR | Vertex Colors | struct |
-* | | Layer Subrecord Collection | collection | See below for details.
 | VTEX | Textures | formid[] | An array of [LTEX](LTEX.md) record FormIDs, or null.

### VNML / VCLR

Each VNML / VCLR structure contains 1089 repeats of the following structure. The 1089 repeats are divided into 33 rows, and subdivided into 33 columns, forming a 33x33 grid.

Name | Type | Info
-----|------|-----
X | uint8 |
Y | uint8 |
Z | uint8 |

### VHGT

Count | Name | Type | Info
------|------|------|-----
 | Offset | float32 |
-* | Row | struct | There are 33 row structs. Each row struct contains 33 `uint8` fields, representing 33 columns.
 | Unused | byte[3] |

### Layer Subrecord Collection

Each layer can be a base layer or an alpha layer, which have different structures.

#### Base Layer

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | BTXT | Base Layer Header | struct |

##### BTXT / ATXT

Name | Type | Info
-----|------|-----
Texture | formid | FormID of a [LTEX](LTEX.md) record, or null.
Quadrant | uint8 | Enum - see below for values.
Unused | byte |
Layer | int16 |

###### Quadrant Enum Values

Value | Meaning
------|--------
0 | Bottom Left
1 | Bottom Right
2 | Top Left
3 | Top Right

#### Alpha Layer

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | ATXT | Alpha Layer Header | struct |
 | VTXT | Alpha Layer Cell Data | struct |

##### VTXT

The VTXT subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Position | uint16 |
Unused | byte[2] |
Opacity | float32 |
