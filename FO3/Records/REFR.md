REFR
====

Placed Object

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | RCLR | Linked Reference Color | struct |
 | RCLR | ?? | ?? |
+ | NAME | Base | formid | FormID of a [TREE](TREE.md), [SOUN](SOUN.md), [ACTI](ACTI.md), [DOOR](DOOR.md), [STAT](STAT.md), [FURN](FURN.md), [CONT](CONT.md), [ARMO](ARMO.md), [AMMO](AMMO.md), [LVLN](LVLN.md), [LVLC](LVLC.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [KEYM](KEYM.md), [ALCH](ALCH.md), [LIGH](LIGH.md), [GRAS](GRAS.md), [ASPC](ASPC.md), [IDLM](IDLM.md), [ARMA](ARMA.md), [MSTT](MSTT.md), [NOTE](NOTE.md), [PWAT](PWAT.md), [SCOL](SCOL.md), [TACT](TACT.md), [TERM](TERM.md) or [TXST](TXST.md) record.
 | XEZN | Encounter Zone | formid | FormID of a [ECZN](ECZN.md) record.
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
 | XTRG | Target | formid | FormID of a [REFR](REFR.md), [ACRE](ACRE.md), [ACHR](ACHR.md), [PGRE](PGRE.md) or [PMIS](PMIS.md) record.
 | XLCM | Level Modifier | int32 |
+ | XPRD | Idle Time | float32 | Patrol data
+ | XPPA | Patrol Script Marker | null | Patrol data
+ | INAM | Idle | formid | Patrol data. FormID of an [IDLE](IDLE.md) record, or null.
+ | | [Embedded Script](Fields/Script.md) | collection | Patrol data.
+ | TNAM | Topic | formid | Patrol data. FormID of a [DIAL](DIAL.md) record, or null.
 | XRDO | Radio Data | struct |
 | XOWN | Owner | formid | Ownership data. FormID of a [FACT](FACT.md), [ACHR](ACHR.md) or [NPC_](NPC_.md) record.
 | XRNK | Faction Rank | int32 | Ownership data
 | XLOC | Lock Data | struct |
 | XCNT | Count | int32 |
 | XRDS | Radius | float32 |
 | XHLP | Health | float32 |
 | XRAD | Radiation | float32 |
 | XCHG | Charge | float32 |
+ | XAMT | Ammo Type | formid | FormID of an [AMMO](AMMO.md) record, or null.
+ | XAMC | Ammo Count | int32 |
-* | [XPWR](Fields/XPWR.md) | Water Reflection / Refraction | struct |
-* | XLTW | Lit Water | formid | FormID of a [REFR](REFR.md) record.
-* | [XDCR](Fields/XDCR.md) | Decal | struct | Linked decals
 | XLKR | Linked Reference | formid | FormID of a [REFR](REFR.md), [ACRE](ACRE.md), [ACHR](ACHR.md), [PGRE](PGRE.md) or [PMIS](PMIS.md) record.
 | [XCLP](Fields/XCLP.md) | Linked Reference Color | struct |
 | [XAPD](Fields/XAPD.md) | Flags | uint8 | Activate parents.
-*| [XAPR](Fields/XAPR.md) | Activate Parent Ref | struct | Activate parents
 | [XESP](Fields/XESP.md) | Enable Parent | struct |
 | XEMI | Emittance | formid | FormID of a [LIGH](LIGH.md) or [REGN](REGN.md) record.
 | XMBR | MultiBound Reference | formid | FormID of a [REFR](REFR.md) record.
 | XACT | Action Flag | uint32 | See below for values.
 | ONAM | Open By Default | null |
 | XIBS | Ignored By Sandbox | null |
 | XNDP | Navigation Door Link | struct |
-* | XPOD | Portal Room | formid | FormID of a [REFR](REFR.md) record, or null.
 | XPLT | Portal Data | struct |
 | XSED | SpeedTree Seed | uint8 |
 | XRMR | Room Data Header | struct |
 | XLRM | Linked Room | formid | FormID of a [REFR](REFR.md) record.
 | XOCP | Occlusion Plane Data | struct |
-* | XORD | Linked Occlusion Plane | formid | FormID of a [REFR](REFR.md) record, or null. Each XORD subrecord corresponds to a different plane - the mapping is given below.
-* | XLOD | Distant LOD Data | byte[4] |
 | XSCL | Scale | float32 |
 | [DATA](Fields/DATA (ACHR, ACRE).md) | Position / Rotation | struct |



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
Door | formid | FormID of a [REFR](REFR.md) record.
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
Position Reference | FormID of a [REFR](REFR.md), [ACRE](ACRE.md), [ACHR](ACHR.md), [PGRE](PGRE.md) or [PMIS](PMIS.md) record, or null.

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
Key | formid | FormID of a [KEYM](KEYM.md) record, or null.
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
Navigation Mesh | formid | FormID of a [NAVM](NAVM.md) record.
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

### XORD Mapping

Index | Occlusion Plane
------|----------------
0 | Right
1 | Left
2 | Bottom
3 | Top
