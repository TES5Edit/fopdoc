Groups
======

Groups are collections of records, and are used to improve scanning of files to make it easier to skip over records that the reading program is not interested in. In addition to this, subgroups for [WRLD](Records/WRLD.md) and [CELL](Records/CELL.md) provide some useful structural information (e.g., the division of cell data into persistent and non-persistent references).

## Group Format

Name | Type | Description
-----|------|------------
type | char[4] | Always "GRUP".
groupSize | uint32 | Size of the group, *including* the 24 bytes before the data.
label | uint8[4] | Format depends on the group type.
groupType | int32 | The group type. See the section below for details.
stamp | uint16 | A date stamp. The first byte is the day of the month, and the second byte is the number of months since December 2002. For example, the 8th of March 2003 would be stored as `08 03`.
unknown | uint8[6] | ??
data | uint8[groupSize - 24] | The records and subgroups contained within the group.

### Group Types

Group Type | Label Type | Group Type Name | Label Info | Group Info
-----------|------------|-----------------|------------|-----------
0 | char[4] | Top Level | A record type. | Contains records of the given type.
1 | formid | World Children | A [WRLD](Records/WRLD.md) record FormID. | Contains [ROAD](Records/ROAD.md) and/or [CELL](Records/CELL.md) records that are children of the given [WRLD](Records/WRLD.md) record.
2 | int32 | Interior Cell Block | A cell block number. |
3 | int32 | Interior Cell Sub-Block | A cell sub-block number. |
4 | int16 | Exterior Cell Block | Cell block grid (Y, X) coordinates, stored as int8 values. |
5 | int16 | Exterior Cell Sub-Block | Cell sub-block grid (Y, X) coordinates, stored as int8 values. |
6 | formid | Cell Children | A [CELL](Records/CELL.md) record FormID. | Contains only [REFR](Records/REFR.md), [ACRE](Records/ACRE.md), [PGRE](Records/PGRE.md), [PMIS](Records/PMIS.md) or [ACHR](Records/ACHR.md) records that are children of the given [CELL](Records/CELL.md) record.
7 | formid | Topic Children | A [DIAL](Records/DIAL.md) record FormID. | Contains [INFO](Records/INFO.md) records that are children of the given [DIAL](Records/DIAL.md) record.
8 | formid | Cell Persistent Children | A [CELL](Records/CELL.md) record FormID. | The group must contain only [REFR](Records/REFR.md), [ACRE](Records/ACRE.md), [PGRE](Records/PGRE.md), [PMIS](Records/PMIS.md) or [ACHR](Records/ACHR.md) records that are children of the given [CELL](Records/CELL.md) record.
9 | formid | Cell Temporary Children | A [CELL](Records/CELL.md) record FormID. | The group must contain only [REFR](Records/REFR.md), [ACRE](Records/ACRE.md), [PGRE](Records/PGRE.md), [PMIS](Records/PMIS.md) or [ACHR](Records/ACHR.md) records that are children of the given [CELL](Records/CELL.md) record.
10 | formid | Cell Visible Distant Children | A [CELL](Records/CELL.md) record FormID. | The group must contain only [REFR](Records/REFR.md) records that are children of the given [CELL](Records/CELL.md) record.

## Top-Level Groups

The top level groups are stored in the following order in `Fallout3.esm`. It is unknown if this order is required, but it would be best to follow it just in case.

[GMST](Records/GMST.md), [TXST](Records/TXST.md), [MICN](Records/MICN.md), [GLOB](Records/GLOB.md), [CLAS](Records/CLAS.md), [FACT](Records/FACT.md), [HDPT](Records/HDPT.md), [HAIR](Records/HAIR.md), [EYES](Records/EYES.md), [RACE](Records/RACE.md), [SOUN](Records/SOUN.md), [ASPC](Records/ASPC.md), [MGEF](Records/MGEF.md), [SCPT](Records/SCPT.md), [LTEX](Records/LTEX.md), [ENCH](Records/ENCH.md), [SPEL](Records/SPEL.md), [ACTI](Records/ACTI.md), [TACT](Records/TACT.md), [TERM](Records/TERM.md), [ARMO](Records/ARMO.md), [BOOK](Records/BOOK.md), [CONT](Records/CONT.md), [DOOR](Records/DOOR.md), [INGR](Records/INGR.md), [LIGH](Records/LIGH.md), [MISC](Records/MISC.md), [STAT](Records/STAT.md), [SCOL](Records/SCOL.md), [MSTT](Records/MSTT.md), [PWAT](Records/PWAT.md), [GRAS](Records/GRAS.md), [TREE](Records/TREE.md), [FURN](Records/FURN.md), [WEAP](Records/WEAP.md), [AMMO](Records/AMMO.md), [NPC_](Records/NPC_.md), [CREA](Records/CREA.md), [LVLC](Records/LVLC.md), [LVLN](Records/LVLN.md), [KEYM](Records/KEYM.md), [ALCH](Records/ALCH.md), [IDLM](Records/IDLM.md), [NOTE](Records/NOTE.md), [PROJ](Records/PROJ.md), [LVLI](Records/LVLI.md), [WTHR](Records/WTHR.md), [CLMT](Records/CLMT.md), [COBJ](Records/COBJ.md), [REGN](Records/REGN.md), [NAVI](Records/NAVI.md), [CELL](Records/CELL.md), [WRLD](Records/WRLD.md), [DIAL](Records/DIAL.md), [QUST](Records/QUST.md), [IDLE](Records/IDLE.md), [PACK](Records/PACK.md), [CSTY](Records/CSTY.md), [LSCR](Records/LSCR.md), [ANIO](Records/ANIO.md), [WATR](Records/WATR.md), [EFSH](Records/EFSH.md), [EXPL](Records/EXPL.md), [DEBR](Records/DEBR.md), [IMGS](Records/IMGS.md), [IMAD](Records/IMAD.md), [FLST](Records/FLST.md), [PERK](Records/PERK.md), [BPTD](Records/BPTD.md), [ADDN](Records/ADDN.md), [AVIF](Records/AVIF.md), [RADS](Records/RADS.md), [CAMS](Records/CAMS.md), [CPTH](Records/CPTH.md), [VTYP](Records/VTYP.md), [IPCT](Records/IPCT.md), [IPDS](Records/IPDS.md), [ARMA](Records/ARMA.md), [ECZN](Records/ECZN.md), [MESG](Records/MESG.md), [RGDL](Records/RGDL.md), [DOBJ](Records/DOBJ.md), [LGTM](Records/LGTM.md), [MUSC](Records/MUSC.md)

## Misc
