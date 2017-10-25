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
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
 | EITM | Object Effect | formid | FormID of an [ENCH](ENCH.md) or [SPEL](SPEL.md) record.
 | MNAM | Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
+ | DATA | Data | struct |
 | INAM | Placed Impact Object | formid | FormID of a [TREE](TREE.md), [SOUN](SOUN.md), [ACTI](ACTI.md), [DOOR](DOOR.md), [STAT](STAT.md), [FURN](FURN.md), [CONT](CONT.md), [ARMO](ARMO.md), [AMMO](AMMO.md), [LVLN](LVLN.md), [LVLC](LVLC.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [KEYM](KEYM.md), [ALCH](ALCH.md), [LIGH](LIGH.md), [GRAS](GRAS.md), [ASPC](ASPC.md), [IDLM](IDLM.md), [ARMA](ARMA.md), [MSTT](MSTT.md), [NOTE](NOTE.md), [PWAT](PWAT.md), [SCOL](SCOL.md), [TACT](TACT.md), [TERM](TERM.md), [TXST](TXST.md), [CHIP](CHIP.md), [CMNY](CMNY.md), [CCRD](CCRD.md) or [IMOD](IMOD.md) record.

### DATA

Name | Type | Info
-----|------|-----
Force | float32 |
Damage | float32 |
Radius | float32 |
Light | formid | FormID of a [LIGH](LIGH.md) record, or null.
Sound 1 | formid | FormID of a [SOUN](SOUN.md) record, or null.
Flags | uint32 | See below for values.
IS Radius | float32 |
Impact Dataset | formid | FormID of a [IPDS](IPDS.md) record, or null.
Sound 2 | formid | FormID of a [SOUN](SOUN.md) record, or null.
Radiation Level | float32 |
Radiation Dissipation Time | float32 |
Radiation Radius | float32 |
+ | [Sound Level](Values/Sound Levels.md) | uint32 | Enum - see link for values.

