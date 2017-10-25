---
layout: fallout3rec
title: fopdoc
---
REFR
====

Placed Object

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | RCLR | Linked Reference Color | struct |
 | RCLR | ?? | ?? |
+ | NAME | Base | formid | FormID of a [TREE](TREE.html), [SOUN](SOUN.html), [ACTI](ACTI.html), [DOOR](DOOR.html), [STAT](STAT.html), [FURN](FURN.html), [CONT](CONT.html), [ARMO](ARMO.html), [AMMO](AMMO.html), [LVLN](LVLN.html), [LVLC](LVLC.html), [MISC](MISC.html), [WEAP](WEAP.html), [BOOK](BOOK.html), [KEYM](KEYM.html), [ALCH](ALCH.html), [LIGH](LIGH.html), [GRAS](GRAS.html), [ASPC](ASPC.html), [IDLM](IDLM.html), [ARMA](ARMA.html), [MSTT](MSTT.html), [NOTE](NOTE.html), [PWAT](PWAT.html), [SCOL](SCOL.html), [TACT](TACT.html), [TERM](TERM.html) or [TXST](TXST.html) record.
 | XEZN | Encounter Zone | formid | FormID of a [ECZN](ECZN.html) record.
 | XRGD | Ragdoll Data | ?? |
 | XRGB | Ragdoll Biped Data | ?? |
 | XPRM | Primitive | struct |
 | XTRI | Collision Layer | uint32 | Enum - see below for values.
 | XMBP | MultiBound Primitive Marker | null |
 | XMBO | Bound Half Extents | struct |
 | XTEL | Teleport Destination | struct |
 | XMRK | Map Marker Marker | null |
 | FNAM | Map Marker Flags | uint8 | See below for values.
+ | FULL | Map Marker Name | cstring |
+ | TNAM | Map Marker Data | struct |
 | XTRG | Target | formid | FormID of a [REFR](REFR.html), [ACRE](ACRE.html), [ACHR](ACHR.html), [PGRE](PGRE.html) or [PMIS](PMIS.html) record.
 | XLCM | Level Modifier | int32 |
+ | XPRD | Idle Time | float32 | Patrol data
+ | XPPA | Patrol Script Marker | null | Patrol data
+ | INAM | Idle | formid | Patrol data. FormID of an [IDLE](IDLE.html) record, or null.
+ | | [Embedded Script](Subrecords/Script.html) | collection | Patrol data.
+ | TNAM | Topic | formid | Patrol data. FormID of a [DIAL](DIAL.html) record, or null.
 | XRDO | Radio Data | struct |
 | XOWN | Owner | formid | Ownership data. FormID of a [FACT](FACT.html), [ACHR](ACHR.html) or [NPC_](NPC_.html) record.
 | XRNK | Faction Rank | int32 | Ownership data
 | XLOC | Lock Data | struct |
 | XCNT | Count | int32 |
 | XRDS | Radius | float32 |
 | XHLP | Health | float32 |
 | XRAD | Radiation | float32 |
 | XCHG | Charge | float32 |
+ | XAMT | Ammo Type | formid | FormID of an [AMMO](AMMO.html) record, or null.
+ | XAMC | Ammo Count | int32 |
-* | [XPWR](Subrecords/XPWR.html) | Water Reflection / Refraction | struct |
-* | XLTW | Lit Water | formid | FormID of a [REFR](REFR.html) record.
-* | [XDCR](Subrecords/XDCR.html) | Decal | struct | Linked decals
 | XLKR | Linked Reference | formid | FormID of a [REFR](REFR.html), [ACRE](ACRE.html), [ACHR](ACHR.html), [PGRE](PGRE.html) or [PMIS](PMIS.html) record.
 | [XCLP](Subrecords/XCLP.html) | Linked Reference Color | struct |
 | [XAPD](Subrecords/XAPD.html) | Flags | uint8 | Activate parents.
-*| [XAPR](Subrecords/XAPR.html) | Activate Parent Ref | struct | Activate parents
 | [XESP](Subrecords/XESP.html) | Enable Parent | struct |
 | XEMI | Emittance | formid | FormID of a [LIGH](LIGH.html) or [REGN](REGN.html) record.
 | XMBR | MultiBound Reference | formid | FormID of a [REFR](REFR.html) record.
 | XACT | Action Flag | uint32 | See below for values.
 | ONAM | Open By Default | null |
 | XIBS | Ignored By Sandbox | null |
 | XNDP | Navigation Door Link | struct |
 | XPOD | Portal Rooms | formid[] | Array of [REFR](REFR.html) record FormIDs, or null.
 | XPLT | Portal Data | struct |
 | XSED | SpeedTree Seed | uint8 |
 | XRMR | Room Data Header | struct |
 | XLRM | Linked Room | formid | FormID of a [REFR](REFR.html) record.
 | XOCP | Occlusion Plane Data | struct |
 | XORD | Linked Occlusion Planes | struct |
 | XLOD | Distant LOD Data | byte[12] | Unknown
 | XSCL | Scale | float32 |
 | [DATA](Subrecords/DATA (ACHR, ACRE).html) | Position / Rotation | struct |



### RCLR

Name | Type | Info
-----|------|-----
Link Start Color | rgba |
Link End Color | rgba |

### XPRM

Name | Type | Info
-----|------|-----
X Bound | float32 |
Y Bound | float32 |
Z Bound | float32 |
Red | float32 |
Green | float32 |
Blue | float32 |
Unknown | byte[4] |
Type | uint32 | Enum - see below for values.

#### Type Values

Value | Meaning
------|--------
0 | None
1 | Box
2 | Sphere
3 | Portal Box

### Collision Layer Values

Value | Meaning
------|--------
0 | Unidentified
1 | Static
2 | AnimStatic
3 | Transparent
4 | Clutter
5 | Weapon
6 | Projectile
7 | Spell
8 | Biped
9 | Trees
10 | Props
11 | Water
12 | Trigger
13 | Terrain
14 | Trap
15 | Non Collidable
16 | Cloud Trap
17 | Ground
18 | Portal
19 | Debris Small
20 | Debris Large
21 | Acustic Space
22 | Actor Zone
23 | Projectile Zone
24 | Gas Trap
25 | Shell Casing
26 | Transparent Small
27 | Invisible Wall
28 | Transparent Small Anim
29 | Dead Bip
30 | Char Controller
31 | Avoid Box
32 | Collision Box
33 | Camera Sphere
34 | Door Detection
35 | Camera Pick
36 | Item Pick
37 | Line Of Sight
38 | Path Pick
39 | Custom Pick 1
40 | Custom Pick 2
41 | Spell Explosion
42 | Dropping Pick

### XMBO

Name | Type | Info
-----|------|-----
X | float32 |
Y | float32 |
Z | float32 |

### XTEL

Name | Type | Info
-----|------|-----
Door | formid | FormID of a [REFR](REFR.html) record.
X Position | float32 |
Y Position | float32 |
Z Position | float32 |
X Rotation | float32 |
Y Rotation | float32 |
Z Rotation | float32 |
Flags | uint32 | See below for values.

#### Flag Values

Value | Meaning
------|--------
0x00000001 | No Alarm

### FNAM Flag Values

Value | Meaning
------|--------
0x01 | Visible
0x02 | Can Travel To
0x04 | "Show All" Hidden

### TNAM

Name | Type | Info
-----|------|-----
Type | uint8 | Enum - see below for values.
Unused | byte |

#### Type Values

Value | Meaning
------|--------
0 | None
1 | City
2 | Settlement
3 | Encampment
4 | Natural Landmark
5 | Cave
6 | Factory
7 | Monument
8 | Military
9 | Office
10 | Town Ruins
11 | Urban Ruins
12 | Sewer Ruins
13 | Metro
14 | Vault

### XRDO

Name | Type | Info
-----|------|-----
Range Radius | float32 |
Broadcast Range Type | uint32 | Enum - see below for values.
Static Percentage | float32 |
Position Reference | FormID of a [REFR](REFR.html), [ACRE](ACRE.html), [ACHR](ACHR.html), [PGRE](PGRE.html) or [PMIS](PMIS.html) record, or null.

#### Broadcast Range Type Values

Value | Meaning
------|--------
0 | Radius
1 | Everywhere
2 | Worldspace and Linked Interiors
3 | Linked Interiors
4 | Current Cell Only

### XLOC

Name | Type | Info
-----|------|-----
Level | uint8 |
Unused | byte[3] |
Key | formid | FormID of a [KEYM](KEYM.html) record, or null.
Flags | uint8 | See below for values.
Unknown | byte[11] |

### XACT Values

Value | Meaning
------|--------
0x00000001 | Use Default
0x00000002 | Activate
0x00000004 | Open
0x00000008 | Open By Default

### XNDP

Name | Type | Info
-----|------|-----
Navigation Mesh | formid | FormID of a [NAVM](NAVM.html) record.
Unknown | byte[4] |

### XPTL / XOCP

Name | Type | Info
-----|------|-----
Width | float32 |
Height | float32 |
X Position | float32 |
Y Position | float32 |
Z Position | float32 |
Quaternion 1 Rotation | float32 |
Quaternion 2 Rotation | float32 |
Quaternion 3 Rotation | float32 |
Quaternion 4 Rotation | float32 |

### XRMR

Name | Type | Info
-----|------|-----
Linked Rooms Count | uint16 |
Unknown | byte[2] |

### XORD

Name | Type | Info
-----|------|-----
Right | formid | FormID of a [REFR](REFR.html) record, or null.
Left | formid | FormID of a [REFR](REFR.html) record, or null.
Bottom | formid | FormID of a [REFR](REFR.html) record, or null.
Top | formid | FormID of a [REFR](REFR.html) record, or null.
