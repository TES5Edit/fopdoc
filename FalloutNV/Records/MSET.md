MSET
====

Media Set

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
 | NAM1 | Type | uint32 | Enum - see values below.
 | NAM2 | Loop (Battle) / Battle (Dungeon) / Day Outer (Location) | cstring |
 | NAM3 | Explore (Dungeon) / Day Middle (Location) | cstring |
 | NAM4 | Suspense (Dungeon) / Day Inner (Location) | cstring |
 | NAM5 | Night Outer (Location) | cstring |
 | NAM6 | Night Middle (Location) | cstring |
 | NAM7 | Night Inner (Location) | cstring |
 | NAM8 | Loop dB (Battle) / Battle dB (Dungeon) / Day Outer dB (Location) | float32 |
 | NAM9 | Explore dB (Dungeon) / Day Middle dB (Location) | float32 |
 | NAM0 | Suspense dB (Dungeon) / Day Inner dB (Location) | float32 |
 | ANAM | Night Outer dB (Location) | float32 |
 | BNAM | Night Middle dB (Location) | float32 |
 | CNAM | Night Inner dB (Location) | float32 |
 | JNAM | Day Outer Boundary % (Location) | float32 |
 | JNAM | Day Middle Boundary % (Location) | float32 |
 | JNAM | Day Inner Boundary % (Location) | float32 |
 | JNAM | Night Outer Boundary % (Location) | float32 |
 | JNAM | Night Middle Boundary % (Location) | float32 |
 | JNAM | Night Inner Boundary % (Location) | float32 |
 | PNAM | Enable Flags | uint8 | See values below.
 | DNAM | Wait Time (Battle) / Min Time On (Dungeon, Location) / Daytime Min (Incidental) | float32 |
 | ENAM | Loop Fade Out (Battle) / Looping/Random Crossfade Overlap (Dungeon, Location) / Nighttime Min (Incidental) | float32 |
 | FNAM | Recovery Time (Battle) / Layer Crossfade Time (Dungeon, Location) / Daytime Max (Incidental) | float32 |
 | GNAM | Nighttime Max (Incidental) | float32 |
 | HNAM | Intro (Battle, Dungeon) / Daytime (Incidental) | formid | FormID of a [SOUN](SOUN.md) record.
 | INAM | Outro (Battle, Dungeon) / Nighttime (Incidental) | formid | FormID of a [SOUN](SOUN.md) record.
 | DATA | ?? | ?? |

### NAM1

Value | Meaning
------|--------
-1 | No Set
0 | Battle Set
1 | Location Set
2 | Dungeon Set
3 | Incidental Set

### PNAM

Value | Meaning
------|--------
0x01 | Day Outer
0x02 | Day Middle
0x04 | Day Inner
0x08 | Night Outer
0x10 | Night Middle
0x20 | Night Inner
