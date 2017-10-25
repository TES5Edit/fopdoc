---
layout: falloutnvrec
title: fopdoc
---
WRLD
====

Worldspace

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
 | XEZN | Encounter Zone | formid | FormID of an [ECZN](ECZN.md) record.
 | WNAM | Parent Worldspace | formid | FormID of a [WRLD](WRLD.md) record.
+ | PNAM | Parent Worldspace Flags | uint16 | See values below.
 | CNAM | Climate | formid | FormID of a [CLMT](CLMT.md) record.
 | NAM2 | Water | formid | FormID of a [WATR](WATR.md) record.
 | NAM3 | LOD Water Type | formid | FormID of a [WATR](WATR.md) record.
 | NAM4 | LOD Water Height | float32 |
 | DNAM | Land Data | struct |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | MNAM | Map Data | struct |
+ | ONAM | World Map Offset Data | struct |
 | INAM | Image Space | formid | FormID of an [IMGS](IMGS.md) record.
+ | DATA | Flags | uint8 | See values below.
+ | NAM0 | Min Object Bounds | struct |
+ | NAM9 | Max Object Bounds | struct |
 | ZNAM | Music | formid | FormID of a [MUSC](MUSC.md) record.
+ | NNAM | Canopy Shadow | cstring |
+ | XNAM | Water Noise Texture | cstring |
-* | IMPS | Swapped Impact | struct |
 | [IMPF](Subrecords/IMPF.md) | Footstep Material | struct |
- | OFST | Offset Data | uint32[] |

#### PNAM Values

Value | Meaning
------|--------
0x0001 | Use Land Data
0x0002 | Use LOD Data
0x0004 | Use Map Data
0x0008 | Use Water Data
0x0010 | Use Climate Data
0x0020 | Use Image Space Data

### DNAM

Name | Type | Info
-----|------|-----
Default Land Height | float32 |
Default Water Height | float32 |

### MNAM

Name | Type | Info
-----|------|-----
Useable X Size | int32 |
Useable Y Size | int32 |
NW Cell X Coordinate | int16 |
NW Cell Y Coordinate | int16 |
SE Cell X Coordinate | int16 |
SE Cell Y Coordinate | int16 |

### ONAM

Name | Type | Info
-----|------|-----
World Map Scale | float32 |
Cell X Offset | float32 |
Cell Y Offset | float32 |

### DATA Values

Value | Meaning
------|--------
0x01 | Small World
0x02 | Can't Fast Travel
0x04 | ??
0x08 | ??
0x10 | No LOD Water
0x20 | No LOD Noise
0x40 | Don't Allow NPC Fall Damage
0x80 | Needs Water Adjustment

### NAM0 / NAM9

Name | Type | Info
-----|------|-----
X | float32 | Value is divided by 4096.
Y | float32 | Value is divided by 4096.

### IMPS

Name | Type | Info
-----|------|-----
[Material Type](Values/Impact Material Types.md) | uint32 |
Old | formid | FormID of an [IPCT](IPCT.md) record.
New | formid | FormID of an [IPCT](IPCT.md) record, or null.
