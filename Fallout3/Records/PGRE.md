---
layout: fallout3rec
title: fopdoc
---
PGRE
====

Placed Grenade

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
+ | NAME | Base | formid | FormID of a [PROJ](PROJ.html) record.
 | XEZN | Encounter Zone | formid | FormID of an [ECZN](ECZN.html) record.
 | XRGD | Ragdoll Data | uint8[] |
 | XRGB | Ragdoll Biped Data | uint8[] |
+ | XPRD | Idle Time | float32 | Patrol data
+ | XPPA | Patrol Script Marker | null | Patrol data
+ | INAM | Idle | formid | Patrol data. FormID of an [IDLE](IDLE.html) record, or null.
+ | | [Embedded Script](Subrecords/Script.html) | collection | Patrol data.
+ | TNAM | Topic | formid | Patrol data. FormID of a [DIAL](DIAL.html) record, or null.
 | XOWN | Owner | formid | Ownership data. FormID of a [FACT](FACT.html), [ACHR](ACHR.html) or [NPC_](NPC_.html) record.
 | XRNK | Faction rank | int32 | Ownership data
 | XCNT | Count | int32 |
 | XRDS | Radius | float32 |
 | XHLP | Health | float32 |
-* | [XPWR](Subrecords/XPWR.html) | Water Reflection / Refraction | struct |
-* | [XDCR](Subrecords/XDCR.html) | Decal | struct | Linked decals
 | XLKR | Linked Reference | formid | FormID of a [REFR](REFR.html), [ACRE](ACRE.html), [ACHR](ACHR.html), [PGRE](PGRE.html) or [PMIS](PMIS.html) record.
 | [XCLP](Subrecords/XCLP.html) | Linked Reference Color | struct |
 | [XAPD](Subrecords/XAPD.html) | Flags | uint8 | Activate parents.
-*| [XAPR](Subrecords/XAPR.html) | Activate Parent Ref | struct | Activate parents
 | [XESP](Subrecords/XESP.html) | Enable Parent | struct |
 | XEMI | Emittance | formid | FormID of a [LIGH](LIGH.html) or [REGN](REGN.html) record.
 | XMBR | MultiBound Reference | formid | FormID of a [REFR](REFR.html) record.
 | XIBS | Ignored By Sandbox | null | Flag
 | XSCL | Scale | float32 |
+ | [DATA](Subrecords/DATA (ACHR, ACRE).html) | Position / Rotation | struct |
