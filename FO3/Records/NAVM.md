NAVM
====

Navigation Mesh

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | NVER | Version | uint32 |
 | DATA | Data | struct |
-* | NVVX | Vertex | struct |
-* | NVTR | Triangle | struct |
-* | NVCA | Unknown | int16 |
-* | NVDP | Door | struct |
 | NVGD | Unknown | uint8[] |
-* | NVEX | External Connection | struct |
 
### DATA

Count | Name | Type | Info
------|------|------|-----
 | Cell | formid | FormID of a [CELL](CELL.md) record.
 | Vertex Count | uint32 |
 | Triangle Count | uint32 |
 | External Connections Count | uint32 |
 | NVCA Count | uint32 |
 | Doors Count | uint32 |
 
### NVVX

Count | Name | Type | Info
------|------|------|-----
 | X | float32 |
 | Y | float32 |
 | Z | float32 |

### NVTR

Count | Name | Type | Info
------|------|------|-----
-* | Vertex | int16 | There are 3 vertex fields.
-* | Triangle | int16 | 
 | Flags | uint32 | See below for values.

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Triangle 0 Is External
0x00000002 | Triangle 1 Is External
0x00000004 | Triangle 2 Is External
0x00000008 | ??
0x00000010 | ??
0x00000010 | ??
0x00000010 | ??
0x00000010 | ??
0x00000100 | ??
0x00000100 | ??
0x00000100 | ??
0x00000100 | ??
0x00001000 | ??
0x00001000 | ??
0x00001000 | ??
0x00001000 | ??
0x00010000 | ??
0x00010000 | ??
0x00010000 | ??
0x00010000 | ??
0x00100000 | ??
0x00100000 | ??
0x00100000 | ??
0x00100000 | ??
0x01000000 | ??
0x01000000 | ??
0x01000000 | ??
0x01000000 | ??
0x10000000 | ??
0x10000000 | ??
0x10000000 | ??
0x10000000 | ??

### NVDP

Count | Name | Type | Info
------|------|------|-----
 | Reference | formid | FormID of a [REFR](REFR.md) record.
 | Unknown | uint16 |
 | Unused | uint8[2] |
 
### NVEX

Count | Name | Type | Info
------|------|------|-----
 | Unknown | uint8[4] |
 |  Navigation Mesh | formid | FormID of a [NAVM](NAVM.md) record.
 | Triangle | uint16 |
