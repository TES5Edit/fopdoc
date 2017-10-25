---
layout: falloutnvrec
title: fopdoc
---
ACHR Record
===========

Placed NPC

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | NAME | Base | formid | FormID of an [NPC_](NPC_.html) record.
- | XEZN | Encounter Zone | formid | FormID of an [ECZN](ECZN.html) record.
- | XRGD | Ragdoll Data | ?? | ??
- | XRGB | Ragdoll Biped Data | ?? | ??
+ | XPRD | Idle Time | float32 | Patrol data
+ | XPPA | Patrol Script Marker | null | Patrol data
+ | INAM | Idle | formid | Patrol data. FormID of an [IDLE](IDLE.html) record, or null.
+ | | [Embedded Script](Subrecords/Script.html) | collection | Patrol data.
+ | TNAM | Topic | formid | Patrol data. FormID of a [DIAL](DIAL.html) record, or null.
- | XLCM | Level Modifier | int32 |
- | XMRC | Merchant Container | formid | FormID of a [REFR](REFR.html) record.
- | XCNT | Count | int32 |
- | XRDS | Radius | float32 |
- | XHLP | Health | float32 |
-* | [XDCR](Subrecords/XDCR.html) | Decal | struct | Linked decals
- | XLKR | Linked Reference | formid | FormID of a [REFR](REFR.html), [ACRE](ACRE.html), [ACHR](ACHR.html), [PGRE](PGRE.html) or [PMIS](PMIS.html) record.
- | [XCLP](Subrecords/XCLP.html) | Linked Reference Color | struct |
- | [XAPD](Subrecords/XAPD.html) | Flags | uint8 | Activate parents.
-* | [XAPR](Subrecords/XAPR.html) | Activate Parent Ref | struct | Activate parents
- | XATO | Activation Prompt | cstring |
- | [XESP](Subrecords/XESP.html) | Enable Parent | struct |
- | XEMI | Emittance | formid | FormID of a [LIGH](LIGH.html) or [REGN](REGN.html) record.
- | XMBR | MultiBound Reference | formid | FormID of a [REFR](REFR.html) record.
- | XIBS | Ignored By Sandbox | null | Flag
- | XSCL | Scale | float32 |
+ | [DATA](Subrecords/DATA (ACHR, ACRE).html) | Position / Rotation | struct |
