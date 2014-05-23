ARMO
====

Armor

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | EITM | Object Effect | formid | FormID of a [ENCH](ENCH.md) or [SPEL](SPEL.md) record.
+ | BMDT | Biped Data | struct | See below for details.
+ | | [Male Biped Model Data](Fields/Model.md) | | This is a field collection. The `MODB` field is not present in this instance.
+ | | [Male World Model Data](Fields/Model.md) | | This is a field collection (#2).
 | ICON | Male inventory icon filename | cstring | 
 | MICO | Male message icon filename | cstring |
+ | | [Female Biped Model Data](Fields/Model.md) | | This is a field collection (#3).
+ | | [Female World Model Data](Fields/Model.md) | | This is a field collection (#4).
 | ICO2 | Female inventory icon filename | cstring |
 | MIC2 | Female message icon filename | cstring |
 | BMCT | Ragdoll Constraint Template | cstring |
 | REPL | Repair List | formid | FormID of a [FLST](FLST.md) record.
 | BIPL | Biped Model List | formid | FormID of a [FLST](FLST.md) record.
+ | [ETYP](Fields/ETYP.md) | Equipment Type | int32 |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | DATA | Data | struct | See below for details.
+ | DNAM | | struct | See below for details.
 

### BMDT

Count | Name | Type | Info
------|------|------|-----
 | Biped Flags | uint32 |
 | General Flags | uint8 |
 | Unused | uint8
 
#### Biped Flag Values

Value | Meaning
-----|--------
0x00000001 | Head
0x00000002 | Hair
0x00000004 | Upper Body
0x00000008 | Left Hand
0x00000010 | Right Hand
0x00000020 | Weapon
0x00000040 | PipBoy
0x00000080 | Backpack
0x00000100 | Necklace
0x00000200 | Headband
0x00000400 | Hat
0x00000800 | Eye Glasses
0x00001000 | Nose Ring
0x00002000 | Earrings
0x00004000 | Mask
0x00008000 | Choker
0x00010000 | Mouth Object
0x00020000 | Body AddOn 1
0x00040000 | Body AddOn 2
0x00080000 | Body AddOn 3

#### General Flag Values

Value | Meaning
-----|--------
0x0001 | ??
0x0002 | ??
0x0004 | ??
0x0008 | ??
0x0010 | ??
0x0020 | Power Armor
0x0040 | Non-Playable
0x0080 | Heavy
 
### DATA

Count | Name | Type | Info
------|------|------|-----
 | Value | int32 | 
 | Max Condition | int32 |
 | Weight | float32 |

### DNAM

Count | Name | Type | Info
------|------|------|-----
 | AR | int16 |
 | Flags | uint16 | See below for details.
 
#### Flag Values

Value | Meaning
-----|--------
0x0001 | Modulates Voice
