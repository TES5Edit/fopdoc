---
layout: falloutnvrec
title: fopdoc
---
ALOC
====

Media Location Controller

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
 | NAM1 | ?? | ?? | Possibly a combination of flags and enums.
 | NAM2 | ?? | ?? |
 | NAM3 | ?? | ?? |
 | NAM4 | Location Delay | float32 |
 | NAM5 | Day Start | uint32 |
 | NAM6 | Night Start | uint32 |
 | NAM7 | Retrigger Delay | float32 |
-* | HNAM | Neutral Media Set | formid | FormID of a [MSET](MSET.html) record.
-* | ZNAM | Ally Media Set | formid | FormID of a [MSET](MSET.html) record.
-* | XNAM | Friend Media Set | formid | FormID of a [MSET](MSET.html) record.
-* | YNAM | Enemy Media Set | formid | FormID of a [MSET](MSET.html) record.
-* | LNAM | Location Media Set | formid | FormID of a [MSET](MSET.html) record.
-* | GNAM | Battle Media Set | formid | FormID of a [MSET](MSET.html) record.
 | RNAM | Conditional Faction | formid | FormID of a [FACT](FACT.html) record.
 | FNAM | ?? | ?? |