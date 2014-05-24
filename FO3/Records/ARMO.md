ARMO
====

Armor

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | EITM | Object Effect | formid | FormID of a [ENCH](ENCH.md) or [SPEL](SPEL.md) record.
+ | [BMDT](Fields/BMDT.md) | Biped Data | struct |
+ | | [Male Biped Model Data](Fields/Model.md) | | This is a field collection. The `MODB` field is not present in this instance.
+ | | [Male World Model Data](Fields/Model.md) | | This is a field collection (#2).
 | ICON | Male inventory icon filename | cstring | 
 | MICO | Male message icon filename | cstring |
+ | | [Female Biped Model Data](Fields/Model.md) | | This is a field collection (#3).
+ | | [Female World Model Data](Fields/Model.md) | | This is a field collection (#4).
 | ICO2 | Female inventory icon filename | cstring |
 | MIC2 | Female message icon filename | cstring |
 | BMCT | Ragdoll Constraint Template | cstring |
 | REPL | Repair List | formid | FormID of a [FLST](FLST.md) record.
 | BIPL | Biped Model List | formid | FormID of a [FLST](FLST.md) record.
+ | [ETYP](Fields/ETYP.md) | Equipment Type | int32 |
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | [DATA](Fields/DATA (ARMO, ARMA).md) | Data | struct |
+ | [DNAM](Fields/DNAM (ARMO, ARMA).md) | | struct |
