MGEF
====

Magic Effect

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
+ | DESC | Description | cstring |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
 | | [Model Data](Fields/Model.md) | collection |
+ | DATA | Data | struct |

### DATA

Name | Type | Info
------|------|------|-----
Flags | uint32 | See below for values.
Base Cost | float32 | Unused.
Associated Item | formid |
Magic School | int32 | Unused. A value of `-1` means `None`.
[Resistance Type](Values/Actor Values.md) | int32 |
Unknown | uint16 |
Unused | byte[2] |
Light | formid | FormID of a [LIGH](LIGH.md) record, or null.
Projectile Speed | float32 |
Effect Shader | formid | FormID of an [EFSH](EFSH.md) record, or null.
Object Display Shader | formid | FormID of an [EFSH](EFSH.md) record, or null.
Effect Sound | formid | FormID of an [SOUN](SOUN.md) record, or null.
Bold Sound | formid | FormID of an [SOUN](SOUN.md) record, or null.
Hit Sound | formid | FormID of an [SOUN](SOUN.md) record, or null.
Area Sound | formid | FormID of an [SOUN](SOUN.md) record, or null.
Constant Effect Enchantment Factor | float32 | Unused.
Constant Effect Barter Factor | float32 | Unused.
Archtype | uint32 | Enum - see below for values.
[Actor Value](Values/Actor Values.md) | int32 |

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Hostile
0x00000002 | Recover
0x00000004 | Detrimental
0x00000008 | ??
0x00000010 | Self
0x00000020 | Touch
0x00000040 | Target
0x00000080 | No Duration
0x00000100 | No Magnitude
0x00000200 | No Area
0x00000400 | FX Persist
0x00000800 | ??
0x00001000 | Gory Visuals
0x00002000 | Display Name Only
0x00004000 | ??
0x00008000 | Radio Broadcast
0x00010000 | ??
0x00020000 | ??
0x00040000 | ??
0x00080000 | Use skill
0x00100000 | Use attribute
0x00200000 | ??
0x00400000 | ??
0x00800000 | ??
0x01000000 | Painless
0x02000000 | Spray projectile type (or Fog if Bolt is specified as well)
0x04000000 | Bolt projectile type (or Fog if Spray is specified as well)
0x08000000 | No Hit Effect
0x10000000 | No Death Dispel
0x20000000 | ??

#### Archtype Values

Value | Meaning
------|--------
0 | Value Modifier
1 | Script
2 | Dispel
3 | Cure Disease
4 | ??
5 | ??
6 | ??
7 | ??
8 | ??
9 | ??
10 | ??
11 | Invisibility
12 | Chameleon
13 | Light
14 | ??
15 | ??
16 | Lock
17 | Open
18 | Bound Item
19 | Summon Creature
20 | ??
21 | ??
22 | ??
23 | ??
24 | Paralysis
25 | ??
26 | ??
27 | ??
28 | ??
29 | ??
30 | Cure Paralysis
31 | Cure Addiction
32 | Cure Poison
33 | Concussion
34 | Value And Parts
