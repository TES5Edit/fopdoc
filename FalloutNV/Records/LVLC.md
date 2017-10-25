---
layout: falloutnvrec
title: fopdoc
---
LVLC
====

Leveled Creature

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | LVLD | Chance None | uint8 |
+ | LVLF | Flags | uint8 | See below for values.
+* | | Leveled List Entry | collection | See below for details.
 | | [Model Data](Subrecords/Model.md) | collection |

### LVLF Flag Values

Value | Meaning
------|--------
0x01 | Calculate From All Levels (player's level)
0x02 | Calculate For Each Item In Count

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
Reference | formid | FormID of a CREA ([FO3](../../Fallout3/Records/CREA.md), [FNV](../../FalloutNV/Records/CREA.md)) or [LVLC](LVLC.md) record.
Count | int16 |
Unused | byte[2] |

