---
layout: falloutnvrec
title: fopdoc
---
RCPE
====

Recipe

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
-* | [CTDA](Subrecords/CTDA.html) | Condition | struct |
 | DATA | Data | struct |
-* | | Ingredient | collection | See below for details.
-* | | Output | collection | See below for details.

### DATA

Name | Type | Info
-----|------|-----
[Skill](Values/Actor Values.html) | int32 |
Level | uint32 |
Category | formid | FormID of a [RCCT](RCCT.html) record.
Sub-Category | formid | FormID of a [RCCT](RCCT.html) record.

### Ingredient / Output Field Collection

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | RCIL | Item | formid | FormID of a [ARMO](ARMO.html), [AMMO](AMMO.html), [MISC](MISC.html), [WEAP](WEAP.html), [BOOK](BOOK.html), [KEYM](KEYM.html), [ALCH](ALCH.html), [NOTE](NOTE.html), [IMOD](IMOD.html), [CMNY](CMNY.html), [CCRD](CCRD.html), [CHIP](CHIP.html) or [LIGH](LIGH.html) record.
+ | RCQY | Quantity | uint32 |
