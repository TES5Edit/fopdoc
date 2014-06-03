LVLI
====

Leveled Item

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | LVLD | Chance None | uint8 |
+ | LVLF | Flags | uint8 | See below for values.
+ | LVLG | Global | formid | FormID of a [GLOB](GLOB.md) record.
+* | | Leveled List Entry | collection | See below for details.
 | | [Model Data](Fields/Model.md) | collection |

### LVLF Flag Values

Value | Meaning
------|--------
0x01 | Calculate From All Levels (player's level)
0x02 | Calculate For Each Item In Count
0x04 | Use All

### Leveled List Entry Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | LVLO | Base Data | struct |
 | [COED](Fields/COED.md) | Extra Data | struct |
 
#### LVLO

Name | Type | Info
-----|------|-----
Level | int16 |
Unused | uint8[2] |
Reference | formid | FormID of a [ARMO](ARMO.md), [AMMO](AMMO.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [LVLI](LVLI.md), [KEYM](KEYM.md), [ALCH](ALCH.md) or [NOTE](NOTE.md) record.
Count | int16 |
Unused | uint8[2] |
