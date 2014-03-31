Groups
======

Groups are collections of records, and are used to improve scanning of files to make it easier to skip over records that the reading program is not interested in. In addition to this, subgroups for WRLD and CELL provide some useful structural information (e.g., the division of cell data into persistent and non-persistent references).

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
1 | formid | World Children | A WRLD record FormID. | Contains ROAD and/or CELL records that are children of the given WRLD record.
2 | int32 | Interior Cell Block | A cell block number. | 
3 | int32 | Interior Cell Sub-Block | A cell sub-block number. |
4 | int16 | Exterior Cell Block | Cell block grid (Y, X) coordinates, stored as int8 values. |
5 | int16 | Exterior Cell Sub-Block | Cell sub-block grid (Y, X) coordinates, stored as int8 values. |
6 | formid | Cell Children | A CELL record FormID. | Contains only REFR, ACRE, PGRE, PMIS or ACHR records that are children of the given CELL record.
7 | formid | Topic Children | A DIAL record FormID. | Contains INFO records that are children of the given DIAL record.
8 | formid | Cell Persistent Children | A CELL record FormID. | The group must contain only REFR, ACRE, PGRE, PMIS or ACHR records that are children of the given CELL record.
9 | formid | Cell Temporary Children | A CELL record FormID. | The group must contain only REFR, ACRE, PGRE, PMIS or ACHR records that are children of the given CELL record.
10 | formid | Cell Visible Distant Children | A CELL record FormID. | The group must contain only REFR records that are children of the given CELL record.

## Top-Level Groups

The top level groups are stored in the following order in `Fallout3.esm`. It is unknown if this order is required, but it would be best to follow it just in case.

GMST, TXST, MICN, GLOB, CLAS, FACT, HDPT, HAIR, EYES, RACE, SOUN, ASPC, MGEF, SCPT, LTEX, ENCH, SPEL, ACTI, TACT, TERM, ARMO, BOOK, CONT, DOOR, INGR, LIGH, MISC, STAT, SCOL, MSTT, PWAT, GRAS, TREE, FURN, WEAP, AMMO, NPC_, CREA, LVLC, LVLN, KEYM, ALCH, IDLM, NOTE, PROJ, LVLI, WTHR, CLMT, COBJ, REGN, NAVI, CELL, WRLD, DIAL, QUST, IDLE, PACK, CSTY, LSCR, ANIO, WATR, EFSH, EXPL, DEBR, IMGS, IMAD, FLST, PERK, BPTD, ADDN, AVIF, RADS, CAMS, CPTH, VTYP, IPCT, IPDS, ARMA, ECZN, MESG, RGDL, DOBJ, LGTM, MUSC

## Misc
