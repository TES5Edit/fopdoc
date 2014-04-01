ACHR Record
===========

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
- | XMRC | Merchant Container | formid |
- | XCNT | Count | int32 |
- | XRDS | Radius | float32 |
- | XHLP | Health | float32 |
-* | [XDCR](Fields/XDCR.md) | Decal | struct | Linked decals
- | XLKR | Linked Reference | formid |
- | [XCLP](Fields/XCLP.md) | Linked Reference Color | struct |
- | XAPD | Flags | uint8 | Activate parents
-* | [XAPR](Fields/XAPR.md) | Activate Parent Ref | struct | Activate parents
- | [XESP](Fields/XESP.md) | Enable Parent | struct |
- | XEMI | Emittance | formid |
- | XMBR | MultiBound Reference | formid |
- | XIBS | Ignored By Sandbox | null | Flag
- | XSCL | Scale | float32 |
+ | [DATA](Fields/DATA (ACHR, ACRE).md) | Position / Rotation | struct |
