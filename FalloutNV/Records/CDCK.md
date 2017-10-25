---
layout: falloutnvrec
title: fopdoc
---
CDCK
====

Caravan Deck

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
-* | CARD | Card | formid | FormID of a [CCRD](CCRD.html) record.
 | DATA | Data | uint32 | Broken