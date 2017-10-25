---
layout: fallout3rec
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
 | XEZN | Encounter Zone | formid | FormID of an [ECZN](ECZN.html) record.
 | WNAM | Parent Worldspace | formid | FormID of a [WRLD](WRLD.html) record.
+ | PNAM | Parent Worldspace Flags | struct |
 | CNAM | Climate | formid | FormID of a [CLMT](CLMT.html) record.
 | NAM2 | Water | formid | FormID of a [WATR](WATR.html) record.
 | NAM3 | LOD Water Type | formid | FormID of a [WATR](WATR.html) record.
 | NAM4 | LOD Water Height | float32 |
 | DNAM | Land Data | struct |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | MNAM | Map Data | struct |
+ | ONAM | World Map Offset Data | struct |
 | INAM | Image Space | formid | FormID of an [IMGS](IMGS.html) record.
+ | DATA | Flags | uint8 | See values below.
+ | NAM0 | Min Object Bounds | struct |
+ | NAM9 | Max Object Bounds | struct |
 | ZNAM | Music | formid | FormID of a [MUSC](MUSC.html) record.
+ | NNAM | Canopy Shadow | cstring |
+ | XNAM | Water Noise Texture | cstring |
-* | IMPS | Swapped Impact | struct |
 | [IMPF](Subrecords/IMPF.html) | Footstep Material | struct |
- | OFST | Offset | uint32[] |

### PNAM

Name | Type | Info
-----|------|-----
Flags | uint8 | See values below.
Unknown | byte |

#### Flag Values

Value | Meaning
------|--------
0x01 | Use Land Data
0x02 | Use LOD Data
0x04 | Use Map Data
0x08 | Use Water Data
0x10 | Use Climate Data
0x20 | Use Image Space Data
0x40 | ??
0x80 | Needs Water Adjustment

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
[Material Type](Values/Impact Material Types.html) | uint32 |
Old | formid | FormID of an [IPCT](IPCT.html) record.
New | formid | FormID of an [IPCT](IPCT.html) record, or null.
