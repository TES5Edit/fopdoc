---
layout: fallout3rec
title: fopdoc
---
CELL
====

Cell

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
+ | DATA | Flags | uint8 | See below for values.
 | XCLC | Grid | struct |
 | XCLL | Lighting | struct |
 | [IMPF](Subrecords/IMPF.html) | Footstep Material | struct |
+ | | Light Template | collection | See below for details.
 | XCLW | Water Height | float32
 | XNAM | Water Noise Texture | cstring |
 | XCLR | Regions | formid[] | Array of [REGN](REGN.html) record FormIDs.
 | XCIM | Image Space | formid | FormID of an [IMGS](IMGS.html) record.
 | XCET | Unknown | byte |
 | XEZN | Encounter Zone | formid | FormID of an [ECZN](ECZN.html) record.
 | XCCM | Climate | formid | FormID of a [CLMT](CLMT.html) record.
 | XCWT | Water | formid | FormID of a [WATR](WATR.html) record.
 | XOWN | Owner | formid | Ownership data. FormID of a [FACT](FACT.html), [ACHR](ACHR.html) or [NPC_](NPC_.html) record.
 | XRNK | Faction rank | int32 | Ownership data
 | XCAS | Acoustic Space | formid | FormID of an [ASPC](ASPC.html) record.
 | XCMT | Unused | byte |
 | XCMO | Music Type | formid | FormID of a [MUSC](MUSC.html) record.


### DATA Flag Values

Value | Meaning
------|--------
0x01 | Is Interior Cell
0x02 | Has Water
0x04 | Invert Fast Travel Behaviour
0x08 | No LOD Water
0x10 | (Unknown)
0x20 | Public Place
0x40 | Hand Changed
0x80 | Behave Like Exterior

### XCLC

Name | Type | Info
-----|------|-----
X | int32 |
Y | int32 |
Force Hide Land | uint32 | Flags - see below for values.

#### Force Hide Land Flag Values

Value | Meaning
------|--------
0x00000001 | Quad 1
0x00000002 | Quad 2
0x00000004 | Quad 3
0x00000008 | Quad 4

### XCLL

Name | Type | Info
-----|------|-----
Ambient Color | rgba |
Directional Color | rgba |
Fog Color | rgba |
Fog Near | float32 |
Fog Far | float32 |
Directional Rotation XY | int32 |
Directional Rotation Z | int32 |
Directional Fade | float32 |
Fog Clip Distance | float32 |
Fog Power | float32 |

### Light Template

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | LTMP | Template | formid | Light template. FormID of an [LGTM](LGTM.html) record, or null.
+ | LNAM | Inherit | uint32 | Light template flags. See below for values.

#### LNAM Inherit Flag Values

Value | Meaning
------|--------
0x00000001 | Ambient Color
0x00000002 | Directional Color
0x00000004 | Fog Color
0x00000008 | Fog Near
0x00000010 | Fog Far
0x00000020 | Directional Rotation
0x00000040 | Directional Fade
0x00000080 | Fog Clip Distance
0x00000100 | Fog Power
