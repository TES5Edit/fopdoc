---
layout: fallout4rec
title: fopdoc
---
XESP Subrecord
==========

As used in the [ACHR](../ACHR.html) and [ACRE](../ACRE.html) record types.

## Format

Name | Type | Info
-----|------|-----
Reference | formid | FormID of a [PLYR](../PLYR.html), [REFR](../REFR.html), [ACRE](../ACRE.html), [ACHR](../ACHR.html), [PGRE](../PGRE.html) or [PMIS](../PMIS.html) record.
Flags | uint8 | See below for details.
Unknown | byte[3] |

### Flag Values

Value | Meaning
------|--------
0x01 | Set Enable State to Opposite of Parent
0x02 | Pop In
