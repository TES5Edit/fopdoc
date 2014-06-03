WEAP
====

Weapon

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | collection |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | EITM | Object Effect | formid | FormID of an [ENCH](ENCH.md) or [SPEL](SPEL.md) record.
 | EAMT | Enchantment Charge Amount | int16 |
 | NAM0 | Ammo | formid | FormID of an [AMMO](AMMO.md) or [FLST](FLST.md) record.
 | | [Destruction Data](Fields/Destruction.md) | collection |
 | REPL | Repair List | formid | FormID of a [FLST](FLST.md) record.
+ | [ETYP](Fields/ETYP.md) | Equipment Type | int32 |
 | BIPL | Biped Model List | formid | FormID of a [FLST](FLST.md) record.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
 | | [Shell Casing Model Data](Fields/Model.md) | collection | #2
 | | [Scope Model Data](Fields/Model.md) | collection | #3
 | EFSD | Scope Effect | formid | FormID of an [EFSH](EFSH.md) record.
 | | [Scope Effect Model Data](Fields/Model.md) | collection | #4
 | NNAM | Embedded Weapon Node | cstring |
 | INAM | Impact Dataset | formid | FormID of a [IPDS](IPDS.md) record.
 | WNAM | First Person Model | formid | FormID of a [STAT](STAT.md) record.
 | SNAM | Sound - Gun - Shoot 3D | formid | FormID of a [SOUN](SOUN.md) record.
 | XNAM | Sound - Gun - Shoot 2D | formid | FormID of a [SOUN](SOUN.md) record.
 | NAM7 | Sound - Gun - Shoot 3D Looping | formid | FormID of a [SOUN](SOUN.md) record.
 | TNAM | Sound - Melee - Swing / Gun - No Ammo | formid | FormID of a [SOUN](SOUN.md) record.
 | NAM6 | Sound - Block | formid | FormID of a [SOUN](SOUN.md) record.
 | UNAM | Sound - Idle | formid | FormID of a [SOUN](SOUN.md) record.
 | NAM9 | Sound - Equip | formid | FormID of a [SOUN](SOUN.md) record.
 | NAM8 | Sound - Unequip | formid | FormID of a [SOUN](SOUN.md) record.
+ | DATA | | struct |
+ | DNAM | | struct |
+ | CRDT | Critical Data | struct |
+ | [VNAM](Values/Sound Levels.md) | Sound Level | uint32 |

### DATA

Name | Type | Info
-----|------|-----
Value | int32 |
Health | int32 |
Weight | float32 |
Base Damage | int16 |
Clip Size | uint8 |

### DNAM

Name | Type | Info
-----|------|-----
[Animation Type](Values/Weapon Animation Types.md) | uint32 | Enum
Animation Multiplier | float32 |
Reach | float32 |
Flags 1 | uint8 | See values below.
Grip Animation | uint8 | Enum - see values below.
Ammo Use | uint8 |
Reload Animation | uint8 | Enum - see values below.
Min Spread | float32 |
Spread | float32 |
Unknown | byte[4] |
Sight FOV | float32 |
Unused | byte[4] |
Projectile | formid | FormID of a [PROJ](PROJ.md) record, or null.
Base VATS To-Hit Chance | uint8 |
Attack Animation | uint8 | Enum - see values below.
Projectile Cound | uint8 |
Embedded Weapon - Actor Value | uint8 | Enum - see values below.
Min Range | float32 |
Max Range | float32 |
On Hit | uint32 | Enum - see values below.
Flags 2 | uint32 | See values below.
Animation Attack Multiplier | float32 |
Fire Rate | float32 |
Override - Action Points | float32 |
Rumble - Left Motor Strength | float32 |
Rumble - Right Motor Strength | float32 |
Rumble - Duration | float32 |
Override - Damage To Weapon Mult | float32 |
Attack Shots/Sec | float32 |
Reload Time | float32 |
Jam Time | float32 |
Aim Arc | float32 |
[Skill](Values/Actor Values.md) | int32 | Enum
Rumble - Pattern | uint32 | Enum - see below for values.
Rumble - Wavelength | float32 |
Limb Damage Multiplier | float32 |
[Resistance Type](Values/Actor Values.md) | int32 | Enum
Sight Usage | float32 |
Semi-Automatic Fire Delay Min | float32 |
Semi-Automatic Fire Delay Max | float32 |

#### Flags 1 Values

Value | Meaning
------|--------
0x01 | Ignores Normal Weapon Resistance
0x02 | Is Automatic
0x04 | Has Scope
0x08 | Can't Drop
0x10 | Hide Backpack
0x20 | Embedded Weapon
0x40 | Don't Use 1st Person IS Animations
0x80 | Non-Playable

#### Grip Animation Values

Value | Meaning
------|--------
171 | HandGrip1
172 | HandGrip2
173 | HandGrip3
255 | Default

#### Reload Animation Values

Value | Meaning
------|--------
0 | ReloadA
1 | ReloadB
2 | ReloadC
3 | ReloadD
4 | ReloadE
5 | ReloadF
6 | ReloadG
7 | ReloadH
8 | ReloadI
9 | ReloadJ
10 | ReloadK

#### Attack Animation Values

Value | Meaning
------|--------
26 | AttackLeft
32 | AttackRight
38 | Attack3
44 | Attack4
50 | Attack5
56 | Attack6
62 | Attack7
68 | Attack8
74 | AttackLoop
80 | AttackSpin
86 | AttackSpin2
97 | PlaceMine
103 | PlaceMine2
109 | AttackThrow
115 | AttackThrow2
121 | AttackThrow3
127 | AttackThrow4
133 | AttackThrow5
255 | Default

#### Embedded Weapon Actor Values

Value | Meaning
------|--------
0 | Perception
1 | Endurance
2 | Left Attack
3 | Right Attack
4 | Left Mobility
5 | Right Mobility
6 | Brain

#### On Hit Values

Value | Meaning
------|--------
0 | Normal Formula Behaviour
1 | Dismember Only
2 | Explode Only
3 | No Dismember / Explode

#### Flags 2 Values

Value | Meaning
------|--------
0x00000001 | Player Only
0x00000002 | NPCs Use Ammo
0x00000004 | No Jam After Reload
0x00000008 | Override - Action Points
0x00000010 | Minor Crime
0x00000020 | Range - Fixed
0x00000040 | Not Used In Normal Combat
0x00000080 | Override - Damage to Weapon Mult
0x00000100 | Don't Use 3rd Person IS Animations
0x00000200 | Short Burst
0x00000400 | Rumble Alternate
0x00000800 | Long Burst

#### Rumble Pattern Values

Value | Meaning
------|--------
0 | Constant
1 | Square
2 | Triangle
3 | Sawtooth

### CRDT

Name | Type | Info
-----|------|-----
Critical Damage | uint16 |
Unused | byte[2] |
Critical % Multiplier | float32 |
Flags | uint8 | See below for values.
Unused | byte[3] |
Effect | formid | FormID of a [SPEL](SPEL.md) record, or null.

#### Flag Values

Value | Meaning
------|--------
0x01 | On Death
