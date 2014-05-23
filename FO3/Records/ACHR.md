ACHR Record
===========

Placed NPC

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | NAME | Base | formid | FormID of an [NPC_](NPC_.md) record.
- | XEZN | Encounter Zone | formid | FormID of an [ECZN](ECZN.md) record.
- | XRGD | Ragdoll Data | ?? | ??
- | XRGB | Ragdoll Biped Data | ?? | ??
+ | XPRD | Idle Time | float32 | Patrol data
+ | XPPA | Patrol Script Marker | null | Patrol data
+ | INAM | Idle | formid | Patrol data. FormID of an [IDLE](IDLE.md) record, or null.
+ | [SCHR](#SCHR) | Basic Script Data | struct | Patrol data, embedded script.
+ | SCDA | Compiled Embedded Script Source | uint8[] | Patrol data, embedded script.
+ | SCTX | Embedded Script Source | char[] | Patrol data, embedded script.
-* | | [Local Variables](#local-variables-field-collection) | | This is a field collection.
-* | SCRO | Reference | formid *or* uint32 | Patrol data, embedded script. A FormID or local variable reference.
+ | TNAM | Topic | formid | Patrol data. FormID of a [DIAL](DIAL.md) record, or null.
- | XLCM | Level Modifier | int32 |
- | XMRC | Merchant Container | formid | FormID of a [REFR](REFR.md) record.
- | XCNT | Count | int32 |
- | XRDS | Radius | float32 |
- | XHLP | Health | float32 |
-* | [XDCR](Fields/XDCR.md) | Decal | struct | Linked decals
- | XLKR | Linked Reference | formid | FormID of a [REFR](REFR.md), [ACRE](ACRE.md), [ACHR](ACHR.md), [PGRE](PGRE.md) or [PMIS](PMIS.md) record.
- | [XCLP](Fields/XCLP.md) | Linked Reference Color | struct |
- | [XAPD](Fields/XAPD.md) | Flags | uint8 | Activate parents.
-* | [XAPR](Fields/XAPR.md) | Activate Parent Ref | struct | Activate parents
- | [XESP](Fields/XESP.md) | Enable Parent | struct |
- | XEMI | Emittance | formid | FormID of a [LIGH](LIGH.md) or [REGN](REGN.md) record.
- | XMBR | MultiBound Reference | formid | FormID of a [REFR](REFR.md) record.
- | XIBS | Ignored By Sandbox | null | Flag
- | XSCL | Scale | float32 |
+ | [DATA](Fields/DATA (ACHR, ACRE).md) | Position / Rotation | struct |

### SCHR

Count | Name | Type | Info
------|------|------|-----
 | Unused | uint8[4] | 
 | Ref Count | uint32 |
 | Compiled Size | uint32 |
 | Variable Count | uint32 |
 | Type | uint16 | See below for values.
 | Flags | | See below for values.
 
#### Type Enum Values

Value | Meaning
------|--------
0 | Object
1 | Quest
0x100 | Effect

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Enabled

### Local Variables Field Collection


Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SLSD](#SLSD) | Local Variable Data | struct | Patrol data, embedded script.
+ | SCVR | Local Variable Name | cstring | Patrol data, embedded script.

#### SLSD

Count | Name | Type | Info
------|------|------|-----
 | Index | uint32 |
 | Unused | uint8[12] |
 | Flags | uint8 | 
 | Unused | uint8[7] |
 
##### Flag Values

Value | Meaning
------|--------
0x00000001 | IsLongOrShort
