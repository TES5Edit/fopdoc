---
layout: fallout3rec
title: fopdoc
---
ARMA
====

Armor Addon

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.html) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | [BMDT](Subrecords/BMDT.html) | Biped Data | struct |
+ | | [Male Biped Model Data](Subrecords/Model.html) | collection | The `MODB` subrecord is not present in this instance.
+ | | [Male World Model Data](Subrecords/Model.html) | collection | #2
 | ICON | Male inventory icon filename | cstring |
 | MICO | Male message icon filename | cstring |
+ | | [Female Biped Model Data](Subrecords/Model.html) | collection | #3
+ | | [Female World Model Data](Subrecords/Model.html) | collection | #4
 | ICO2 | Female inventory icon filename | cstring |
 | MIC2 | Female message icon filename | cstring |
+ | [ETYP](Subrecords/ETYP.html) | Equipment Type | int32 |
+ | [DATA](Subrecords/DATA (ARMO, ARMA).html) | Data | struct |
+ | [DNAM](Subrecords/DNAM (ARMO, ARMA).html) | | struct |

