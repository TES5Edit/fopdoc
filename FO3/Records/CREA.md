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
+ | EAMT | Unarmed Attack Animation | uint16 | 
-* | NIFZ | Model | cstring |
 | NIFT | Texture File Hashes | uint8[] |
+ | [ACBS](Fields/ACBS.md) | Configuration | struct |
-* | SNAM | Faction | struct |
 | INAM | Death Item | formid | FormID of a [LVLI](LVLI.md) record.
 | VTCK | Voice | formid | FormID of a [VTYP](VTYP.md) record.
 | TPLT | Template | formid | FormID of a [CREA](CREA.md) or [LVLC](LVLC.md) record.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
-* | | [Item](Fields/Item.md) | | This is a field collection.
 | AIDT | AI Data | struct |
-* | PKID | Package | formid | FormID of a [PACK](PACK.md) record.
-* | KFFZ | Animation | cstring |
+ | DATA | Data | struct |
+ | RNAM | Attack Reach | uint8 |
 | ZNAM | Combat Style | formid | FormID of a [CSTY](CSTY.md) record.
+ | PNAM | Body Part Data | formid | FormID of a [BPTD](BPTD.md) record.
+ | TNAM | Turning Speed | float32 | 
+ | BNAM | Base Scale | float32 |
+ | WNAM | Foot Weight | float32 |
+ | NAM4 | Impact Material Type | uint32 | Enum - see below for values.
+ | [NAM5](Values/Sound Levels.md) | Sound Level | uint32 | Enum - see link for values.
 | CSCR | Inherits Sounds from | formid | FormID of a [CREA](CREA.md) record.
-* | | Sound Type | | This is a field collection. See below for details.
 | CNAM | Impact Dataset | formid | FormID of a [IPDS](IPDS.md) record.
 | LNAM | Melee Weapon List | formid | FormID of a [FLST](FLST.md) record.

### SNAM

Count | Name | Type | Info
------|------|------|-----
 | Faction | formid | FormID of a [FACT](FACT.md) record.
 | Rank | uint8 | 
 | Unused | uint8[3] |
 
### AIDT

Count | Name | Type | Info
------|------|------|-----
 | Aggression | uint8 | Enum - see below for values.
 | Confidence | uint8 | Enum - see below for values.
 | Energy Level | uint8 |
 | Responsibility | uint8 |
 | Mood | uint8 | Enum - see below for values.
 | Unused | uint8[3] |
 | [Buys/Sells and Services](Values/Services.md) | uint32 | Flags - see link for values.
 | [Teaches](Values/Skills.md) | int8 | Enum - see link for values.
 | Maximum Training Level | uint8 | 
 | Assistance | int8 | Enum - see below for values.
 | Aggro Radius Behaviour | uint8 | Flags - see below for values.
 | Aggro Radius | int32 |
 
 
#### Aggression Enum Values

Value | Meaning
------|--------
0 | Unaggressive
1 | Aggressive
2 | Very Aggressive
3 | Frenzied
 
#### Confidence Enum Values

Value | Meaning
------|--------
0 | Cowardly
1 | Cautious
2 | Average
3 | Brave
4 | Foolhardy

#### Mood Enum Values

Value | Meaning
------|--------
0 | Neutral 
1 | Afraid
2 | Annoyed
3 | Cocky
4 | Drugged
5 | Pleasant
6 | Angry
7 | Sad

#### Assistance Enum Values

Value | Meaning
------|--------
0 | Helps Nobody
1 | Helps Allies
2 | Helps Friends and Allies

#### Aggro Radius Behavior Flag Values

Value | Meaning
------|--------
0x01 | Aggro Radius Behavior

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


### NAM4 Enum Values

Value | Meaning
------|--------
0 | Stone
1 | Dirt
2 | Grass
3 | Glass
4 | Metal
5 | Wood
6 | Organic
7 | Cloth
8 | Water
9 | Hollow Metal
10 | Organic Bug
11 | Organic Glow

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
 
