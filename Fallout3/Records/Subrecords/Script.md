---
layout: fallout3rec
title: fopdoc
---
# Script Subrecord Collection

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | [SCHR](SCHR.html) | Basic Script Data | struct |
+ | SCDA | Compiled Script Source | uint8[] |
+ | SCTX | Script Source | char[] |
-* | | [Local Variables](#local-variables) | collection | See below for details.
-* | SCRO | Reference | formid *or* uint32 | A local variable reference, or FormID of a [ACTI](../ACTI.html), [DOOR](../DOOR.html), [STAT](../STAT.html), [FURN](../FURN.html), [CREA](../CREA.html), [SPEL](../SPEL.html), [NPC_](../NPC_.html), [CONT](../CONT.html), [ARMO](../ARMO.html), [AMMO](../AMMO.html), [MISC](../MISC.html), [WEAP](../WEAP.html), [IMAD](../IMAD.html), [BOOK](../BOOK.html), [KEYM](../KEYM.html), [ALCH](../ALCH.html), [LIGH](../LIGH.html), [QUST](../QUST.html), [PLYR](../PLYR.html), [PACK](../PACK.html), [LVLI](../LVLI.html), [ECZN](../ECZN.html), [EXPL](../EXPL.html), [FLST](../FLST.html), [IDLM](../IDLM.html), [PMIS](../PMIS.html), [FACT](../FACT.html), [ACHR](../ACHR.html), [REFR](../REFR.html), [ACRE](../ACRE.html), [GLOB](../GLOB.html), [DIAL](../DIAL.html), [CELL](../CELL.html), [SOUN](../SOUN.html), [MGEF](../MGEF.html), [WTHR](../WTHR.html), [CLAS](../CLAS.html), [EFSH](../EFSH.html), [RACE](../RACE.html), [LVLC](../LVLC.html), [CSTY](../CSTY.html), [WRLD](../WRLD.html), [SCPT](../SCPT.html), [IMGS](../IMGS.html), [MESG](../MESG.html), [MSTT](../MSTT.html), [MUSC](../MUSC.html), [NOTE](../NOTE.html), [PERK](../PERK.html), [PGRE](../PGRE.html), [PROJ](../PROJ.html), [LVLN](../LVLN.html), [WATR](../WATR.html), [ENCH](../ENCH.html), [TREE](../TREE.html), [TERM](../TERM.html), [HAIR](../HAIR.html), [EYES](../EYES.html), [ADDN](../ADDN.html) or [NULL](../NULL.html) record.

### Local Variables


Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | [SLSD](#slsd) | Local Variable Data | struct |
+ | SCVR | Local Variable Name | cstring |

#### SLSD

Name | Type | Info
-----|------|-----
Index | uint32 |
Unused | byte[12] |
Flags | uint8 | See below for values.
Unused | byte[7] |

##### Flag Values

Value | Meaning
------|--------
0x01 | IsLongOrShort
