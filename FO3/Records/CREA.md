CREA
====

Creature

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
-* | SPLO | Actor Effect | formid | FormID of a [SPEL](SPEL.md) record.
 | EITM | Unarmed Attack Effect | formid | FormID of a [ENCH](ENCH.md) or [SPEL](SPEL.md) record.
+ | [EAMT](Values/Attack Animations.md) | Unarmed Attack Animation | uint16 |
-* | NIFZ | Model | cstring |
 | NIFT | Texture File Hashes | uint8[] |
+ | [ACBS](Fields/ACBS.md) | Configuration | struct |
-* | [SNAM](Fields/SNAM (CREA, NPC_).md) | Faction | struct |
 | INAM | Death Item | formid | FormID of a [LVLI](LVLI.md) record.
 | VTCK | Voice | formid | FormID of a [VTYP](VTYP.md) record.
 | TPLT | Template | formid | FormID of a [CREA](CREA.md) or [LVLC](LVLC.md) record.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
-* | | [Item](Fields/Item.md) | | This is a field collection.
 | [AIDT](Fields/AIDT.md) | AI Data | struct |
-* | PKID | Package | formid | FormID of a [PACK](PACK.md) record.
-* | KFFZ | Animation | cstring |
+ | DATA | Data | struct |
+ | RNAM | Attack Reach | uint8 |
 | ZNAM | Combat Style | formid | FormID of a [CSTY](CSTY.md) record.
+ | PNAM | Body Part Data | formid | FormID of a [BPTD](BPTD.md) record.
+ | TNAM | Turning Speed | float32 | 
+ | BNAM | Base Scale | float32 |
+ | WNAM | Foot Weight | float32 |
+ | [NAM4](Values/Impact Material Types.md) | Impact Material Type | uint32 | 
+ | [NAM5](Values/Sound Levels.md) | Sound Level | uint32 | Enum - see link for values.
 | CSCR | Inherits Sounds from | formid | FormID of a [CREA](CREA.md) record.
-* | | Sound Type | | This is a field collection. See below for details.
 | CNAM | Impact Dataset | formid | FormID of a [IPDS](IPDS.md) record.
 | LNAM | Melee Weapon List | formid | FormID of a [FLST](FLST.md) record.

### DATA

Count | Name | Type | Info
------|------|------|-----
 | Type | uint8 | Enum - see below for values.
 | Combat Skill | uint8 |
 | Magic Skill | uint8 |
 | Stealth Skill | uint8 |
 | Health | int16 |
 | Unused | uint8[2] | 
 | Damage | int16 |
 | Attribute | uint8 | There are 7 attribute fields, one for each attribute. The mapping of fields to attributes is given below.There are 7 attribute fields, one for each attribute. The mapping of fields to attributes is given below.

#### Type Enum Values

Values | Meaning
-------|--------
0 | Animal
1 | Mutated Animal
2 | Mutated Insect
3 | Abomination
4 | Super Mutant
5 | Feral Ghoul
6 | Robot
7 | Giant

#### ATTR Map

ATTR Field | Attribute
-----------|----------
1st | Strength
2nd | Perception
3rd | Endurance
4th | Charisma
5th | Intelligence
6th | Agility
7th | Luck

### Sound Type Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | CSDT | Type | uint32 | Enum - see below for values.
+* | CSDI | Sound | formid | FormID of a [SOUN](SOUN.md) record.
+* | CSDC | Sound Chance | uint8 |

CSDI and CSDC are in a repeated block.

#### CSDT Enum Values

Value | Meaning
------|--------
0 | Left Foot
1 | Right Foot
2 | Left Back Foot
3 | Right Back Foot
4 | Idle
5 | Aware
6 | Attack
7 | Hit
8 | Death
9 | Weapon
10 | Movement
11 | Conscious
 
