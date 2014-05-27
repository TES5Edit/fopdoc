LVLC
====

Leveled Creature

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | LVLD | Chance None | uint8 |
+ | LVLF | Flags | uint8 | See below for values.
+* | | Leveled List Entry | | A field collection, see below for details.
 | | [Model Data](Fields/Model.md) | | This is a field collection.

### LVLF Flag Values

Value | Meaning
------|--------
0x01 | Calculate From All Levels (player's level)
0x02 | Calculate For Each Item In Count

### Leveled List Entry Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | LVLO | Base Data | struct |
 | [COED](Fields/COED.md) | Extra Data | struct |
 
#### LVLO

Count | Name | Type | Info
------|------|------|-----
 | Level | int16 |
 | Unused | uint8[2] |
 | Reference | formid | FormID of a [CREA](CREA.md) or [LVLC](LVLC.md) record.
 | Count | int16 |
 | Unused | uint8[2] |

