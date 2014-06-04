ARMA
====

Armor Addon

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | BMDT | Biped Data | struct | See below for details.
+ | | [Male Biped Model Data](Subrecords/Model.md) | collection | The `MODB` subrecord is not present in this instance.
+ | | [Male World Model Data](Subrecords/Model.md) | collection | #2
 | ICON | Male inventory icon filename | cstring |
 | MICO | Male message icon filename | cstring |
+ | | [Female Biped Model Data](Subrecords/Model.md) | collection | #3
+ | | [Female World Model Data](Subrecords/Model.md) | collection | #4
 | ICO2 | Female inventory icon filename | cstring |
 | MIC2 | Female message icon filename | cstring |
+ | [ETYP](Subrecords/ETYP.md) | Equipment Type | int32 |
+ | [DATA](Subrecords/DATA (ARMO, ARMA).md) | Data | struct |
+ | [DNAM](Subrecords/DNAM (ARMO, ARMA).md) | | struct |

