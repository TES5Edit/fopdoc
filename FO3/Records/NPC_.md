NPC_
====

Non-Player Character

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
+ | [ACBS](Fields/ACBS.md) | Configuration | struct |
-* | [SNAM](Fields/SNAM (CREA, NPC_).md) | Faction | struct |
 | INAM | Death Item | formid | FormID of a [LVLI](LVLI.md) record.
+ | VTCK | Voice | formid | FormID of a [VTYP](VTYP.md) record.
 | TPLT | Template | formid | FormID of a [NPC_](NPC_.md) or [LVLN](LVLN.md) record.
+ | RNAM | Race | formid | FormID of a [RACE](RACE.md) record.
 | EITM | Unarmed Attack Effect | formid | FormID of an [ENCH](ENCH.md) or [SPEL](SPEL.md) record.
+ | [EAMT](Values/Attack Animations.md) | Unarmed Attack Animation | uint16 |
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
-* | | [Item](Fields/Item.md) | | This is a field collection.
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

Count | Name | Type | Info
------|------|------|-----
 | Base Health | int32 |
-* | Attribute | uint8 | There are 7 attribute fields, one for each attribute. The mapping of fields to attributes is given below.
 | Unused | uint8[] | Only appears in older record versions.

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

### DNAM

Count | Name | Type | Info
------|------|------|-----
-* | Skill Value | uint8 |
-* | Skill Offset | uint8 | 

There are 14 values and 14 offsets, with array indicies corresponding to different skills according to the values [here](Values/Skill Enum Values.md).
