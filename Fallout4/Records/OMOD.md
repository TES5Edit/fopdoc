---
layout: fallout4rec
title: fopdoc
---
OMOD
====

Object Mod

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
 | FULL | Fullname | localized string | Display name
 | [Model](Subrecords/Model.html) | Model | struct | Model to use when mod is attached 
 | DATA | DATA | struct | Unknown
 | WEAP | WEAP | struct | Values in the WEAP record to override?
 | [MNAM](KYWD.html) | MNAM | Keyword | Unknown
 | [LNAM](MISC.html) | LNAM | Misc Item | Item to use as inventory/world object?