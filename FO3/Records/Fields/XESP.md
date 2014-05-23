XESP Field
==========

As used in the [ACHR](../ACHR.md) and [ACRE](../ACRE.md) record types.

## Format

Count | Name | Type | Info
------|------|------|-----
- | Reference | formid | FormID of a [PLYR](../PLYR.md), [REFR](../REFR.md), [ACRE](../ACRE.md), [ACHR](../ACHR.md), [PGRE](../PGRE.md) or [PMIS](../PMIS.md) record.
- | Flags | uint8 | See below for details.
- | unknown | uint8[3] | ??

### Flag Values

Value | Meaning
------|--------
0x00000001 | Set Enable State to Opposite of Parent
0x00000002 | Pop In
