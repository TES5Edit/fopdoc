XESP Field
==========

As used in the [ACHR](../ACHR.md) and [ACRE](../ACRE.md) record types.

## Format

Name | Type | Info
-----|------|-----
Reference | formid | FormID of a [PLYR](../PLYR.md), [REFR](../REFR.md), [ACRE](../ACRE.md), [ACHR](../ACHR.md), [PGRE](../PGRE.md) or [PMIS](../PMIS.md) record.
Flags | uint8 | See below for details.
Unknown | byte[3] |

### Flag Values

Value | Meaning
------|--------
0x01 | Set Enable State to Opposite of Parent
0x02 | Pop In
