---
layout: fallout3rec
title: fopdoc
---
NAVM
====

Navigation Mesh

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | NVER | Version | uint32 |
 | DATA | Data | struct |
 | NVVX | Vertices | struct |
 | NVTR | Triangles | struct |
 | NVCA | Unknown | int16[] | Unknown, may be triangle IDs.
 | NVDP | Doors | struct |
 | NVGD | Unknown | uint8[] |
 | NVEX | External Connections | struct |

### DATA

Name | Type | Info
-----|------|-----
Cell | formid | FormID of a [CELL](CELL.html) record.
Vertex Count | uint32 |
Triangle Count | uint32 |
External Connections Count | uint32 |
NVCA Count | uint32 |
Doors Count | uint32 |

### NVVX

The NVVX subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
X | float32 |
Y | float32 |
Z | float32 |

### NVTR

The NVTR subrecord consists of an array of objects with the following structure.

Count | Name | Type | Info
------|------|------|-----
 | Vertex 1 | int16 |
 | Vertex 2 | int16 |
 | Vertex 3 | int16 |
 | Edge - Vertices 1,2 | int16 |
 | Edge - Vertices 2,3 | int16 |
 | Edge - Vertices 3,1 | int16 |
 | Flags | uint32 | See below for values.

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Triangle 0 Is External
0x00000002 | Triangle 1 Is External
0x00000004 | Triangle 2 Is External
0x00000008 | ??
0x00000010 | ??
0x00000020 | ??
0x00000040 | ??
0x00000080 | ??
0x00000100 | ??
0x00000200 | ??
0x00000400 | ??
0x00000800 | ??
0x00001000 | ??
0x00002000 | ??
0x00004000 | ??
0x00008000 | ??
0x00010000 | ??
0x00020000 | ??
0x00040000 | ??
0x00080000 | ??
0x00100000 | ??
0x00200000 | ??
0x00400000 | ??
0x00800000 | ??
0x01000000 | ??
0x02000000 | ??
0x04000000 | ??
0x08000000 | ??
0x10000000 | ??
0x20000000 | ??
0x40000000 | ??
0x80000000 | ??

### NVDP

The NVDP subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Reference | formid | FormID of a [REFR](REFR.html) record.
Unknown | uint16 |
Unused | byte[2] |

### NVEX

The NVEX subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
Unknown | byte[4] |
Navigation Mesh | formid | FormID of a [NAVM](NAVM.html) record.
Triangle | uint16 |
