---
layout: fallout3rec
title: fopdoc
---
ARMO
====

Armor

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | EITM | Object Effect | formid | FormID of a [ENCH](ENCH.html) or [SPEL](SPEL.html) record.
+ | [BMDT](Subrecords/BMDT.html) | Biped Data | struct |
+ | | [Male Biped Model Data](Subrecords/Model.html) | collection | The `MODB` subrecord is not present in this instance.
+ | | [Male World Model Data](Subrecords/Model.html) | collection | #2
 | ICON | Male inventory icon filename | cstring |
 | MICO | Male message icon filename | cstring |
+ | | [Female Biped Model Data](Subrecords/Model.html) | collection | #3
+ | | [Female World Model Data](Subrecords/Model.html) | collection | #4
 | ICO2 | Female inventory icon filename | cstring |
 | MIC2 | Female message icon filename | cstring |
 | BMCT | Ragdoll Constraint Template | cstring |
 | REPL | Repair List | formid | FormID of a [FLST](FLST.html) record.
 | BIPL | Biped Model List | formid | FormID of a [FLST](FLST.html) record.
+ | [ETYP](Subrecords/ETYP.html) | Equipment Type | int32 |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.html) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.html) record.
+ | [DATA](Subrecords/DATA (ARMO, ARMA).html) | Data | struct |
+ | [DNAM](Subrecords/DNAM (ARMO, ARMA).html) | | struct |
