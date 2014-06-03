NPC_
====

Non-Player Character

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | collection |
+ | [ACBS](Fields/ACBS.md) | Configuration | struct |
-* | [SNAM](Fields/SNAM (CREA, NPC_).md) | Faction | struct |
 | INAM | Death Item | formid | FormID of a [LVLI](LVLI.md) record.
+ | VTCK | Voice | formid | FormID of a [VTYP](VTYP.md) record.
 | TPLT | Template | formid | FormID of a [NPC_](NPC_.md) or [LVLN](LVLN.md) record.
+ | RNAM | Race | formid | FormID of a [RACE](RACE.md) record.
 | EITM | Unarmed Attack Effect | formid | FormID of an [ENCH](ENCH.md) or [SPEL](SPEL.md) record.
+ | [EAMT](Values/Attack Animations.md) | Unarmed Attack Animation | uint16 |
 | | [Destruction Data](Fields/Destruction.md) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
-* | | [Item](Fields/Item.md) | collection |
 | [AIDT](Fields/AIDT.md) | AI Data | struct |
-* | PKID | Package | formid | FormID of a [PACK](PACK.md) record.
+ | CNAM | Class | formid | FormID of a [CLAS](CLAS.md) record.
+ | DATA | | struct |
 | DNAM | Skills | struct |
-* | PNAM | Head Part | formid | FormID of a [HDPT](HDPT.md) record.
 | HNAM | Hair | formid | FormID of a [HAIR](HAIR.md) record.
 | LNAM | Hair Length | float32 |
 | ENAM | Eyes | formid | FormID of an [EYES](EYES.md) record.
+ | HCLR | Hair Color | rgba |
 | ZNAM | Combat Style | formid | FormID of a [CSTY](CSTY.md) record.
+ | [NAM4](Values/Impact Material Types.md) | Impact Material Type | uint32 |
+ | FGGS | FaceGen Geometry-Symmetric | uint8[] |
+ | FGGA | FaceGen Geometry-Asymmetric | uint8[] |
+ | FGTS | FaceGen Texture-Symmetric | uint8[] |
+ | NAM5 | Unknown | uint16 |
+ | NAM6 | Height | float32 |
+ | NAM7 | Weight | float32 |

### DATA

Name | Type | Info
-----|------|-----
Base Health | int32 |
Strength | uint8 |
Perception | uint8 |
Endurance | uint8 |
Charisma | uint8 |
Intelligence | uint8 |
Agility | uint8 |
Luck | uint8 |
Unused | uint8[] | Only appears in older record versions.

### DNAM

Name | Type | Info
-----|------|-----
Skill Value - Barter | uint8 |
Skill Value - Big Guns | uint8 |
Skill Value - Energy Weapons | uint8 |
Skill Value - Explosives | uint8 |
Skill Value - Lockpick | uint8 |
Skill Value - Medicine | uint8 |
Skill Value - Melee Weapons | uint8 |
Skill Value - Repair | uint8 |
Skill Value - Science | uint8 |
Skill Value - Small Guns | uint8 |
Skill Value - Sneak | uint8 |
Skill Value - Speech | uint8 |
Skill Value - Throwing | uint8 | Unused
Skill Value - Unarmed | uint8 |
Skill Offset - Barter | uint8 |
Skill Offset - Big Guns | uint8 |
Skill Offset - Energy Weapons | uint8 |
Skill Offset - Explosives | uint8 |
Skill Offset - Lockpick | uint8 |
Skill Offset - Medicine | uint8 |
Skill Offset - Melee Weapons | uint8 |
Skill Offset - Repair | uint8 |
Skill Offset - Science | uint8 |
Skill Offset - Small Guns | uint8 |
Skill Offset - Sneak | uint8 |
Skill Offset - Speech | uint8 |
Skill Offset - Throwing | uint8 | Unused
Skill Offset - Unarmed | uint8 |
