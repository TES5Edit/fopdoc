ARMA
====

Armor Addon

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | BMDT | Biped Data | struct | See below for details.
+ | | [Male Biped Model Data](Fields/Model.md) | collection | The `MODB` field is not present in this instance.
+ | | [Male World Model Data](Fields/Model.md) | collection | #2
 | ICON | Male inventory icon filename | cstring |
 | MICO | Male message icon filename | cstring |
+ | | [Female Biped Model Data](Fields/Model.md) | collection | #3
+ | | [Female World Model Data](Fields/Model.md) | collection | #4
 | ICO2 | Female inventory icon filename | cstring |
 | MIC2 | Female message icon filename | cstring |
+ | [ETYP](Fields/ETYP.md) | Equipment Type | int32 |
+ | [DATA](Fields/DATA (ARMO, ARMA).md) | Data | struct |
+ | [DNAM](Fields/DNAM (ARMO, ARMA).md) | | struct |

