---
layout: falloutnvrec
title: fopdoc
---
EXPL
====

Explosion

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.html) | collection |
 | EITM | Object Effect | formid | FormID of an [ENCH](ENCH.html) or [SPEL](SPEL.html) record.
 | MNAM | Image Space Modifier | formid | FormID of an [IMAD](IMAD.html) record.
+ | DATA | Data | struct |
 | INAM | Placed Impact Object | formid | FormID of a [TREE](TREE.html), [SOUN](SOUN.html), [ACTI](ACTI.html), [DOOR](DOOR.html), [STAT](STAT.html), [FURN](FURN.html), [CONT](CONT.html), [ARMO](ARMO.html), [AMMO](AMMO.html), [LVLN](LVLN.html), [LVLC](LVLC.html), [MISC](MISC.html), [WEAP](WEAP.html), [BOOK](BOOK.html), [KEYM](KEYM.html), [ALCH](ALCH.html), [LIGH](LIGH.html), [GRAS](GRAS.html), [ASPC](ASPC.html), [IDLM](IDLM.html), [ARMA](ARMA.html), [MSTT](MSTT.html), [NOTE](NOTE.html), [PWAT](PWAT.html), [SCOL](SCOL.html), [TACT](TACT.html), [TERM](TERM.html), [TXST](TXST.html), [CHIP](CHIP.html), [CMNY](CMNY.html), [CCRD](CCRD.html) or [IMOD](IMOD.html) record.

### DATA

Name | Type | Info
-----|------|-----
Force | float32 |
Damage | float32 |
Radius | float32 |
Light | formid | FormID of a [LIGH](LIGH.html) record, or null.
Sound 1 | formid | FormID of a [SOUN](SOUN.html) record, or null.
Flags | uint32 | See below for values.
IS Radius | float32 |
Impact Dataset | formid | FormID of a [IPDS](IPDS.html) record, or null.
Sound 2 | formid | FormID of a [SOUN](SOUN.html) record, or null.
Radiation Level | float32 |
Radiation Dissipation Time | float32 |
Radiation Radius | float32 |
+ | [Sound Level](Values/Sound Levels.html) | uint32 | Enum - see link for values.

