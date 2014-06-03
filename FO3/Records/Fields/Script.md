# Script Field Collection

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SCHR](SCHR.md) | Basic Script Data | struct |
+ | SCDA | Compiled Script Source | uint8[] |
+ | SCTX | Script Source | char[] |
-* | | [Local Variables](#local-variables) | | A field collection, see below for details.
-* | SCRO | Reference | formid *or* uint32 | A local variable reference, or FormID of a [ACTI](../ACTI.md), [DOOR](../DOOR.md), [STAT](../STAT.md), [FURN](../FURN.md), [CREA](../CREA.md), [SPEL](../SPEL.md), [NPC_](../NPC_.md), [CONT](../CONT.md), [ARMO](../ARMO.md), [AMMO](../AMMO.md), [MISC](../MISC.md), [WEAP](../WEAP.md), [IMAD](../IMAD.md), [BOOK](../BOOK.md), [KEYM](../KEYM.md), [ALCH](../ALCH.md), [LIGH](../LIGH.md), [QUST](../QUST.md), [PLYR](../PLYR.md), [PACK](../PACK.md), [LVLI](../LVLI.md), [ECZN](../ECZN.md), [EXPL](../EXPL.md), [FLST](../FLST.md), [IDLM](../IDLM.md), [PMIS](../PMIS.md), [FACT](../FACT.md), [ACHR](../ACHR.md), [REFR](../REFR.md), [ACRE](../ACRE.md), [GLOB](../GLOB.md), [DIAL](../DIAL.md), [CELL](../CELL.md), [SOUN](../SOUN.md), [MGEF](../MGEF.md), [WTHR](../WTHR.md), [CLAS](../CLAS.md), [EFSH](../EFSH.md), [RACE](../RACE.md), [LVLC](../LVLC.md), [CSTY](../CSTY.md), [WRLD](../WRLD.md), [SCPT](../SCPT.md), [IMGS](../IMGS.md), [MESG](../MESG.md), [MSTT](../MSTT.md), [MUSC](../MUSC.md), [NOTE](../NOTE.md), [PERK](../PERK.md), [PGRE](../PGRE.md), [PROJ](../PROJ.md), [LVLN](../LVLN.md), [WATR](../WATR.md), [ENCH](../ENCH.md), [TREE](../TREE.md), [REPU](../REPU.md), [REGN](../REGN.md), [CSNO](../CSNO.md), [CHAL](../CHAL.md), [IMOD](../IMOD.md), [RCCT](../RCCT.md), [CMNY](../CMNY.md), [CDCK](../CDCK.md), [CHIP](../CHIP.md), [CCRD](../CCRD.md), [TERM](../TERM.md), [HAIR](../HAIR.md), [EYES](../EYES.md), [ADDN](../ADDN.md) or [NULL](../NULL.md) record.

### Local Variables


Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SLSD](#slsd) | Local Variable Data | struct |
+ | SCVR | Local Variable Name | cstring |

#### SLSD

Name | Type | Info
-----|------|-----
Index | uint32 |
Unused | uint8[12] |
Flags | uint8 | See below for values.
Unused | uint8[7] |
 
##### Flag Values

Value | Meaning
------|--------
0x01 | IsLongOrShort
