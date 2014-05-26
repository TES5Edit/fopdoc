PROJ
====

Projectile

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | | This is a field collection.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
+ | [DATA](#data) | Data | struct 
+ | NAM1 | Muzzle Flash Model Filename | cstring |
+ | NAM2 | Muzzle Flash Model Texture File Hashes | uint8[] |
+ | [VNAM](Values/Sound Levels.md) | Sound Level | uint32 | Enum - see link for values.
 
### DATA

Count | Name | Type | Info
------|------|------|-----
 | Flags | uint16 | See below for values.
 | Type | uint16 | Enum - see below for values.
 | Gravity | float32 |
 | Speed | float32 |
 | Range | float32 |
 | Light | formid | FormID of a [LIGH](LIGH.md) record, or null.
 | Muzzle Flash - Light | formid | FormID of a [LIGH](LIGH.md) record, or null.
 | Tracer Chance | float32 |
 | Explosion - Alt. Trigger - Proximity | float32 |
 | Explosion - Alt. Trigger - Timer | float32 |
 | Explosion | formid | FormID of an [EXPL](EXPL.md) record, or null.
 | Sound | formid | FormID of a [SOUN](SOUN.md) record, or null.
 | Muzzle Flash - Duration | float32 |
 | Fade Duration | float32 |
 | Impact Force | float32 |
 | Sound - Countdown | formid | FormID of a [SOUN](SOUN.md) record, or null.
 | Sound - Disable | formid | FormID of a [SOUN](SOUN.md) record, or null.
 | Default Weapon Source | formid | FormID of a [WEAP](WEAP.md) record, or null.
 
#### Flag Values

Value | Meaning
------|--------
0x001 | Hitscan
0x002 | Explosion
0x004 | Alt. Trigger
0x008 | Muzzle Flash
0x010 | ??
0x020 | Can Be Disabled
0x040 | Can Be Picked Up
0x080 | Supersonic
0x100 | Pins Limbs
0x200 | Pass Through Small Transparent

#### Type Enum Values

Value | Meaning
------|--------
0 | ??
1 | Missile
2 | Lobber
3 | ??
4 | Beam
5 | ??
6 | ??
7 | ??
8 | Flame
 
 