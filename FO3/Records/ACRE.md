ACRE Record
===========

Placed Creature

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | NAME | Base | formid | 
- | XEZN | Encounter Zone | formid |
- | XRGD | Ragdoll Data | ?? | ??
- | XRGB | Ragdoll Biped Data | ?? | ??
+ | XPRD | Idle Time | float32 | Patrol data
+ | XPPA | Patrol Script Marker | null | Patrol data
+ | INAM | Idle | formid | Patrol data
+ | TNAM | Topic | formid | Patrol data
- | XLCM | Level Modifier | int32 | 
- | XOWN | Owner | formid | Ownership data
- | XRNK | Faction rank | int32 | Ownership data
- | XMRC | Merchant Container | formid |
- | XCNT | Count | int32 |
- | XRDS | Radius | float32 |
- | XHLP | Health | float32 |
-* | XDCR | Decal | struct | Linked decals
- | XLKR | Linked Reference | formid | 
- | XCLP | Linked Reference Color | struct |
- | XAPD | Flags | uint8 | Activate parents
-* | XAPR | Activate Parent Ref | struct | Activate parents
- | XESP | Enable Parent | struct |
- | XEMI | Emittance | formid |
- | XMBR | MultiBound Reference | formid |
- | XIBS | Ignored By Sandbox | null | Flag
- | XSCL | Scale | float32 |
+ | DATA | Position / Rotation | struct |

### XDCR

Count | Name | Type | Info
------|------|------|-----
- | Reference | formid | 
- | unknown | ?? | ??

### XCLP

Count | Name | Type | Info
------|------|------|-----
- | Link Start Color | rgba | 
- | Link End Color | rgba |

### XAPR

Count | Name | Type | Info
------|------|------|-----
- | Reference | formid | 
- | Delay | float32 |

### XESP

Count | Name | Type | Info
------|------|------|-----
- | Reference | formid | 
- | Flags | uint8 |
- | unknown | uint8[3] | ??

### DATA

Count | Name | Type | Info
------|------|------|-----
- | X | float32 | X position
- | Y | float32 | Y position
- | Z | float32 | Z position
+ | X | float32 | X rotation
+ | Y | float32 | Y rotation
+ | Z | float32 | Z rotation
