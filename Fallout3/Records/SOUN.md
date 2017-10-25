---
layout: fallout3rec
title: fopdoc
---
SOUN
====

Sound

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FNAM | Sound Filename | cstring |
+ | SNDD *or* SNDX | Sound Data | struct |
- | ANAM | Attenuation Points | int16[5] | Each int16 represents a separate point on an attenuation curve.
 | GNAM | Reverb Attenuation Control | int16 |
 | HNAM | Priority | int32 |

### SNDD

Name | Type | Info
-----|------|-----
Minimum Attenuation Distance | uint8 | Multiplied by 5.
Maximum Attenuation Distancce | uint8 | Multiplied by 100.
Frequency Adjustment Percentage | int8 |
Unused | byte |
Flags | uint32 | See below for values.
Static Attenuation cdB | int16 |
Stop Time | uint8 |
Start Time | uint8 |
Attenuation Point 1 | int16 | The first point on the attenuation curve.
Attenuation Point 2 | int16 | The second point on the attenuation curve.
Attenuation Point 3 | int16 | The third point on the attenuation curve.
Attenuation Point 4 | int16 | The fourth point on the attenuation curve.
Attenuation Point 5 | int16 | The fifth point on the attenuation curve.
Reverb Attenuation Control | int16 |
Priority | int32 |
Unknown | byte[8] |

### SNDX

Name | Type | Info
-----|------|-----
Minimum Attenuation Distance | uint8 | Multiplied by 5.
Maximum Attenuation Distancce | uint8 | Multiplied by 100.
Frequency Adjustment Percentage | int8 |
Unused | byte |
Flags | uint32 | See below for values.
Static Attenuation cdB | int16 |
Stop Time | uint8 |
Start Time | uint8 |

### SNDD / SNDX Flag Values

Value | Meaning
------|--------
0x00000001 | Random Frequency Shift
0x00000002 | Play At Random
0x00000004 | Environment Ignored
0x00000008 | Random Location
0x00000010 | Loop
0x00000020 | Menu Sound
0x00000040 | 2D
0x00000080 | 360 LFE
0x00000100 | Dialogue Sound
0x00000200 | Envelope Fast
0x00000400 | Envelope Slow
0x00000800 | 2D Radius
0x00001000 | Mute When Submerged
