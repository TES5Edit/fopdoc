---
layout: falloutnvgrp
title: fopdoc
---
Groups
======

Groups are collections of records, and are used to improve scanning of files to make it easier to skip over records that the reading program is not interested in. In addition to this, subgroups for [WRLD](Records/WRLD.html) and [CELL](Records/CELL.html) provide some useful structural information (e.g., the division of cell data into persistent and non-persistent references).

## Group Format

Name | Type | Description
-----|------|------------
type | char[4] | Always "GRUP".
groupSize | uint32 | Size of the group, *including* the 24 bytes before the data.
label | byte[4] | Format depends on the group type.
groupType | int32 | The group type. See the section below for details.
stamp | uint16 | A date stamp. The first byte is the day of the month, and the second byte is the number of months since some unknown point in time (perhaps April 2009, when Obsidian is said to have began development of Fallout: New Vegas).
Unknown | byte[6] |
data | byte[groupSize - 24] | The records and subgroups contained within the group.

### Group Types

Group Type | Label Type | Group Type Name | Label Info | Group Info
-----------|------------|-----------------|------------|-----------
0 | char[4] | Top Level | A record type. | Contains records of the given type.
1 | formid | World Children | A [WRLD](Records/WRLD.html) record FormID. | Contains [ROAD](Records/ROAD.html) and/or [CELL](Records/CELL.html) records that are children of the given [WRLD](Records/WRLD.html) record.
2 | int32 | Interior Cell Block | A cell block number. |
3 | int32 | Interior Cell Sub-Block | A cell sub-block number. |
4 | int16 | Exterior Cell Block | Cell block grid (Y, X) coordinates, stored as int8 values. |
5 | int16 | Exterior Cell Sub-Block | Cell sub-block grid (Y, X) coordinates, stored as int8 values. |
6 | formid | Cell Children | A [CELL](Records/CELL.html) record FormID. | Contains only [REFR](Records/REFR.html), [ACRE](Records/ACRE.html), [PGRE](Records/PGRE.html), [PMIS](Records/PMIS.html) or [ACHR](Records/ACHR.html) records that are children of the given [CELL](Records/CELL.html) record.
7 | formid | Topic Children | A [DIAL](Records/DIAL.html) record FormID. | Contains [INFO](Records/INFO.html) records that are children of the given [DIAL](Records/DIAL.html) record.
8 | formid | Cell Persistent Children | A [CELL](Records/CELL.html) record FormID. | The group must contain only [REFR](Records/REFR.html), [ACRE](Records/ACRE.html), [PGRE](Records/PGRE.html), [PMIS](Records/PMIS.html) or [ACHR](Records/ACHR.html) records that are children of the given [CELL](Records/CELL.html) record.
9 | formid | Cell Temporary Children | A [CELL](Records/CELL.html) record FormID. | The group must contain only [REFR](Records/REFR.html), [ACRE](Records/ACRE.html), [PGRE](Records/PGRE.html), [PMIS](Records/PMIS.html) or [ACHR](Records/ACHR.html) records that are children of the given [CELL](Records/CELL.html) record.
10 | formid | Cell Visible Distant Children | A [CELL](Records/CELL.html) record FormID. | The group must contain only [REFR](Records/REFR.html) records that are children of the given [CELL](Records/CELL.html) record.

## Top-Level Groups

The top level groups are stored in the following order in `FalloutNV.esm`. It is unknown if this order is required, but it would be best to follow it just in case.

[GMST](Records/GMST.html), [TXST](Records/TXST.html), [MICN](Records/MICN.html), [GLOB](Records/GLOB.html), [CLAS](Records/CLAS.html), [FACT](Records/FACT.html), [HDPT](Records/HDPT.html), [HAIR](Records/HAIR.html), [EYES](Records/EYES.html), [RACE](Records/RACE.html), [SOUN](Records/SOUN.html), [ASPC](Records/ASPC.html), [MGEF](Records/MGEF.html), [SCPT](Records/SCPT.html), [LTEX](Records/LTEX.html), [ENCH](Records/ENCH.html), [SPEL](Records/SPEL.html), [ACTI](Records/ACTI.html), [TACT](Records/TACT.html), [TERM](Records/TERM.html), [ARMO](Records/ARMO.html), [BOOK](Records/BOOK.html), [CONT](Records/CONT.html), [DOOR](Records/DOOR.html), [INGR](Records/INGR.html), [LIGH](Records/LIGH.html), [MISC](Records/MISC.html), [STAT](Records/STAT.html), [SCOL](Records/SCOL.html), [MSTT](Records/MSTT.html), [PWAT](Records/PWAT.html), [GRAS](Records/GRAS.html), [TREE](Records/TREE.html), [FURN](Records/FURN.html), [WEAP](Records/WEAP.html), [AMMO](Records/AMMO.html), [NPC_](Records/NPC_.html), [CREA](Records/CREA.html), [LVLC](Records/LVLC.html), [LVLN](Records/LVLN.html), [KEYM](Records/KEYM.html), [ALCH](Records/ALCH.html), [IDLM](Records/IDLM.html), [NOTE](Records/NOTE.html), [COBJ](Records/COBJ.html), [PROJ](Records/PROJ.html), [LVLI](Records/LVLI.html), [WTHR](Records/WTHR.html), [CLMT](Records/CLMT.html), [REGN](Records/REGN.html), [NAVI](Records/NAVI.html), [DIAL](Records/DIAL.html), [QUST](Records/QUST.html), [IDLE](Records/IDLE.html), [PACK](Records/PACK.html), [CSTY](Records/CSTY.html), [LSCR](Records/LSCR.html), [ANIO](Records/ANIO.html), [WATR](Records/WATR.html), [EFSH](Records/EFSH.html), [EXPL](Records/EXPL.html), [DEBR](Records/DEBR.html), [IMGS](Records/IMGS.html), [IMAD](Records/IMAD.html), [FLST](Records/FLST.html), [PERK](Records/PERK.html), [BPTD](Records/BPTD.html), [ADDN](Records/ADDN.html), [AVIF](Records/AVIF.html), [RADS](Records/RADS.html), [CAMS](Records/CAMS.html), [CPTH](Records/CPTH.html), [VTYP](Records/VTYP.html), [IPCT](Records/IPCT.html), [IPDS](Records/IPDS.html), [ARMA](Records/ARMA.html), [ECZN](Records/ECZN.html), [MESG](Records/MESG.html), [RGDL](Records/RGDL.html), [DOBJ](Records/DOBJ.html), [LGTM](Records/LGTM.html), [MUSC](Records/MUSC.html), [IMOD](Records/IMOD.html), [REPU](Records/REPU.html), [RCPE](Records/RCPE.html), [RCCT](Records/RCCT.html), [CHIP](Records/CHIP.html), [CSNO](Records/CSNO.html), [LSCT](Records/LSCT.html), [MSET](Records/MSET.html), [ALOC](Records/ALOC.html), [CHAL](Records/CHAL.html), [AMEF](Records/AMEF.html), [CCRD](Records/CCRD.html), [CMNY](Records/CMNY.html), [CDCK](Records/CDCK.html), [DEHY](Records/DEHY.html), [HUNG](Records/HUNG.html), [SLPD](Records/SLPD.html), [CELL](Records/CELL.html), [WRLD](Records/WRLD.html)
