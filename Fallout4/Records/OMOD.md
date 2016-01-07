OMOD
====

Object Mod

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
 | FULL | Fullname | localized string | Display name
 | [Model](Subrecords/Model.md) | Model | struct | Model to use when mod is attached 
 | DATA | DATA | struct | Unknown
 | WEAP | WEAP | struct | Values in the WEAP record to override?
 | [MNAM](KYWD.md) | MNAM | Keyword | Unknown
 | [LNAM](MISC.md) | LNAM | Misc Item | Item to use as inventory/world object?