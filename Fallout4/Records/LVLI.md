---
layout: fallout4rec
title: fopdoc
---
LVLI
====

Leveled Item

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | LVLD | Chance None | uint8 |
 | LVLM | | | Unknown at this time
+ | LVLF | Flags | uint8 | See below for values.
+ | LVLG | Global | formid | FormID of a [GLOB](GLOB.md) record.
+ | LLCT | Count | uint8 | Leveled List Count not to exceed 255
+* | | Leveled List Entry | collection | See below for details.
 | LLKC | | | Unknown at this time
 | LVSG | | | Unknown at this time
 | ONAM | | | Unknown at this time

** Existing Data Below Subject to change Copied from previous Fallout **

### LVLF Flag Values

Value | Meaning
------|--------
0x01 | Calculate From All Levels (player's level)
0x02 | Calculate For Each Item In Count
0x04 | Use All

### Leveled List Entry Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | LVLO | Base Data | struct |
 | [COED](Subrecords/COED.md) | Extra Data | struct |

#### LVLO

Name | Type | Info
-----|------|-----
Level | int16 |
Unused | byte[2] |
Reference | formid | FormID of a [ARMO](ARMO.md), [AMMO](AMMO.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [LVLI](LVLI.md), [KEYM](KEYM.md), [ALCH](ALCH.md), [NOTE](NOTE.md), [IMOD](IMOD.md), [CMNY](CMNY.md), [CCRD](CCRD.md) or [CHIP](CHIP.md) record.
Count | int16 |
Unused | byte[2] |