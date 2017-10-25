---
layout: fallout3rec
title: fopdoc
---
LVLN
====

Leveled NPC

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
+ | LVLD | Chance None | uint8 |
+ | LVLF | Flags | uint8 | See below for values.
+* | | Leveled List Entry | collection | See below for details.
 | | [Model Data](Subrecords/Model.html) | collection |

### LVLF Flag Values

Value | Meaning
------|--------
0x01 | Calculate From All Levels (player's level)
0x02 | Calculate For Each Item In Count

### Leveled List Entry Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | LVLO | Base Data | struct |
 | [COED](Subrecords/COED.html) | Extra Data | struct |

#### LVLO

Name | Type | Info
-----|------|-----
Level | int16 |
Unused | byte[2] |
Reference | formid | FormID of a NPC_ ([FO3](../../Fallout3/Records/NPC_.html), [FNV](../../FalloutNV/Records/NPC_.html)) or [LVLN](LVLN.html) record.
Count | int16 |
Unused | byte[2] |
