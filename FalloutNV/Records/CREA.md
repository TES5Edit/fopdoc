---
layout: falloutnvrec
title: fopdoc
---
CREA
====

Creature

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
-* | SPLO | Actor Effect | formid | FormID of a [SPEL](SPEL.html) record.
 | EITM | Unarmed Attack Effect | formid | FormID of a [ENCH](ENCH.html) or [SPEL](SPEL.html) record.
+ | [EAMT](Values/Attack Animations.html) | Unarmed Attack Animation | uint16 |
- | NIFZ | Model List | cstring[] | An array of models.
 | NIFT | Texture File Hashes | uint8[] |
+ | [ACBS](Subrecords/ACBS.html) | Configuration | struct |
-* | [SNAM](Subrecords/SNAM (CREA, NPC_).html) | Faction | struct |
 | INAM | Death Item | formid | FormID of a [LVLI](LVLI.html) record.
 | VTCK | Voice | formid | FormID of a [VTYP](VTYP.html) record.
 | TPLT | Template | formid | FormID of a [CREA](CREA.html) or [LVLC](LVLC.html) record.
 | | [Destruction Data](Subrecords/Destruction.html) | collection |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
-* | | [Item](Subrecords/Item.html) | collection |
 | [AIDT](Subrecords/AIDT.html) | AI Data | struct |
-* | PKID | Package | formid | FormID of a [PACK](PACK.html) record.
- | KFFZ | Animations | cstring[] | An array of animations.
+ | DATA | Data | struct |
+ | RNAM | Attack Reach | uint8 |
 | ZNAM | Combat Style | formid | FormID of a [CSTY](CSTY.html) record.
+ | PNAM | Body Part Data | formid | FormID of a [BPTD](BPTD.html) record.
+ | TNAM | Turning Speed | float32 |
+ | BNAM | Base Scale | float32 |
+ | WNAM | Foot Weight | float32 |
+ | [NAM4](Values/Impact Material Types.html) | Impact Material Type | uint32 |
+ | [NAM5](Values/Sound Levels.html) | Sound Level | uint32 | Enum - see link for values.
 | CSCR | Inherits Sounds from | formid | FormID of a [CREA](CREA.html) record.
-* | | Sound Type | collection | See below for details.
 | CNAM | Impact Dataset | formid | FormID of a [IPDS](IPDS.html) record.
 | LNAM | Melee Weapon List | formid | FormID of a [FLST](FLST.html) record.

### DATA

Name | Type | Info
-----|------|-----
Type | uint8 | Enum - see below for values.
Combat Skill | uint8 |
Magic Skill | uint8 |
Stealth Skill | uint8 |
Health | int16 |
Unused | byte[2] |
Damage | int16 |
Strength | uint8 |
Perception | uint8 |
Endurance | uint8 |
Charisma | uint8 |
Intelligence | uint8 |
Agility | uint8 |
Luck | uint8 |

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

### Sound Type Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | CSDT | Type | uint32 | Enum - see below for values.
+* | CSDI | Sound | formid | FormID of a [SOUN](SOUN.html) record, or null.
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
10 | Movement Loop
11 | Conscious Loop
12 | Auxiliary 1
13 | Auxiliary 2
14 | Auxiliary 3
15 | Auxiliary 4
16 | Auxiliary 5
17 | Auxiliary 6
18 | Auxiliary 7
19 | Auxiliary 8
20 | Jump
21 | Play Random / Loop
