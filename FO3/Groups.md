Groups
======

Groups are collections of records, and are used to improve scanning of files to make it easier to skip over records that the reading program is not interested in. In addition to this, subgroups for WRLD and CELL provide some useful structural information (e.g., the division of cell data into persistent and non-persistent references).

## Group Format

Name | Type | Description
-----|------|------------
type | char[4] | Always "GRUP".
groupSize | uint32 | Size of the group, *including* the 24 bytes before the data.
label | uint8 | 
groupType | int32 | 
stamp | uint16 | 
unknown | uint16 |
version | uint16 |
unknown | uint16 |
data | uint8[groupSize - 24] |

## Top Level Groups

The top level groups are stored in the following order in `Fallout3.esm`. It is unknown if this order is required, but it would be best to follow it just in case.

GMST, TXST, MICN, GLOB, CLAS, FACT, HDPT, HAIR, EYES, RACE, SOUN, ASPC, MGEF, SCPT, LTEX, ENCH, SPEL, ACTI, TACT, TERM, ARMO, BOOK, CONT, DOOR, INGR, LIGH, MISC, STAT, SCOL, MSTT, PWAT, GRAS, TREE, FURN, WEAP, AMMO, NPC_, CREA, LVLC, LVLN, KEYM, ALCH, IDLM, NOTE, PROJ, LVLI, WTHR, CLMT, COBJ, REGN, NAVI, CELL, WRLD, DIAL, QUST, IDLE, PACK, CSTY, LSCR, ANIO, WATR, EFSH, EXPL, DEBR, IMGS, IMAD, FLST, PERK, BPTD, ADDN, AVIF, RADS, CAMS, CPTH, VTYP, IPCT, IPDS, ARMA, ECZN, MESG, RGDL, DOBJ, LGTM, MUSC

## Misc
