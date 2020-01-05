---
layout: falloutnvrec
title: fopdoc
---
XNAM Subrecord
==========

As used in the [FACT](../FACT.md) and [RACE](../RACE.md) record types.

## Format

Name | Type | Info
-----|------|-----
Faction | formid | FormID of a [FACT](../FACT.md) or [RACE](../RACE.md) record.
Modifier | int32 |
Group Combat Reaction | uint32 | Enum - see values below.
 
#### Group Combat Reaction Enum Values

Value | Meaning
------|--------
0 | Neutral
1 | Enemy
2 | Ally
3 | Friend
