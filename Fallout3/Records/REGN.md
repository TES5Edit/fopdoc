REGN
====

Region

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
+ | RCLR | Map Color | rgba |
 | WNAM | Worldspace | formid | FormID of a [WRLD](WRLD.md) record.
-* | | Region Area | collection | See below for details.
-* | Region Data Entry | collection | See below for details.

### Region Area Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | RPLI | Edge Fall-Off | uint32 |
- | RPLD | Region Point List Data | struct |

#### RPLD

The RPLD subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
X | float32 |
Y | float32 |

### Region Data Entry Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | RDAT | Data Header | struct |
- | RDOT | Objects | struct |
 | RDMP | Map Name | cstring |
- | RDGS | Grasses | struct |
 | RDMD | Music Type | uint32 | Enum - see below for values.
 | RDMO | Music | formid | FormID of a [MUSC](MUSC.md) record.
- | RDSD | Sound | struct |
- | RDWT | Weather Type | struct |

#### RDAT

Name | Type | Info
-----|------|-----
Type | uint32 | Enum - see below for values.
Flags | uint8 | See below for values.
Unused | byte[3] |

##### Type Values

Value | Meaning
------|--------
0 | ??
1 | ??
2 | Objects
3 | Weather
4 | Map
5 | Land
6 | Grass
7 | Sound
8 | ??
9 | ??

##### Flag Values

Value | Meaning
------|--------
0x01 | Override

#### RDOT

The RDOT subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Object | formid | FormID of a [TREE](TREE.md), [STAT](STAT.md) or [LTEX](LTEX.md) record.
Parent Index | uint16 |
Unused | byte[2] |
Density | float32 |
Clustering | uint8 |
Min Slope | uint8 |
Max Slope | uint8 |
Flags | uint8 | See below for values
Radius With Respect To Parent | uint16 |
Radius | uint16 |
Unknown | byte[4] |
Max Height | float32 |
Sink | float32 |
Sink Variance | float32 |
Size Variance | float32 |
X Angle Variance | uint16 |
Y Angle Variance | uint16 |
Z Angle Variance | uint16 |
Unknown | byte[6] |

##### Flag Values

Value | Meaning
------|--------
0x01 | Conform To Slope
0x02 | Paint Vertices
0x04 | Size Variance +/-
0x08 | X +/-
0x10 | Y +/-
0x20 | Z +/-
0x40 | Tree
0x80 | Huge Rock

#### RDGS

The RDGS subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Grass | formid | FormID of a [GRAS](GRAS.md) record.
Unknown | byte[4] |

#### RDMD Values

Value | Meaning
------|--------
0 | Default
1 | Public
2 | Dungeon

#### RDSD

The RDSD subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Sound | formid | FormID of a [SOUN](SOUN.md) record.
Flags | uint32 | See below for values.
Chance | uint32 |

##### Flag Values

Value | Meaning
------|--------
0x00000001 | Pleasant
0x00000002 | Cloudy
0x00000004 | Rainy
0x00000008 | Snowy

#### RDWT

The RDWT subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Weather | formid | FormID of a [WTHR](WTHR.md) record.
Chance | uint32 |
Global | formid | FormID of a [GLOB](GLOB.md) record, or null.
