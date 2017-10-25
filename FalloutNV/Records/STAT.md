---
layout: falloutnvrec
title: fopdoc
---
STAT
====

Static

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | | [Model](Subrecords/Model.md) | collection |
 | BRUS | Passthrough Sound | int8 | Enum - see values below.
 | RNAM | Sound - Looping / Random | formid | FormID of a [SOUN](SOUN.md) record.

### BRUS Values

Value | Meaning
------|--------
-1 | None
0 | BushA
1 | BushB
2 | BushC
3 | BushD
4 | BushE
5 | BushF
6 | BushG
7 | BushH
8 | BushI
9 | BushJ
