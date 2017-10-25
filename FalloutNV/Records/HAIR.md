---
layout: falloutnvrec
title: fopdoc
---
HAIR
====

Hair

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | FULL | Name | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
+ | ICON | Texture | cstring |
+ | DATA | Flags | uint8 | See below for values.

### DATA Flag Values

Value | Meaning
------|--------
0x01 | Playable
0x02 | Not Male
0x04 | Not Female
0x08 | Fixed
