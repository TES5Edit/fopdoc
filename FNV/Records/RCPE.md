RCPE
====

Recipe

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
-* | [CTDA](Fields/CTDA.md) | Condition | struct |
 | DATA | Data | struct |
-* | | Ingredient | collection | See below for details.
-* | | Output | collection | See below for details.

### DATA

Name | Type | Info
-----|------|-----
[Skill](Values/Actor Values.md) | int32 |
Level | uint32 |
Category | formid | FormID of a [RCCT](RCCT.md) record.
Sub-Category | formid | FormID of a [RCCT](RCCT.md) record.

### Ingredient / Output Field Collection

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | RCIL | Item | formid | FormID of a [ARMO](ARMO.md), [AMMO](AMMO.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [KEYM](KEYM.md), [ALCH](ALCH.md), [NOTE](NOTE.md), [IMOD](IMOD.md), [CMNY](CMNY.md), [CCRD](CCRD.md), [CHIP](CHIP.md) or [LIGH](LIGH.md) record.
+ | RCQY | Quantity | uint32 |
