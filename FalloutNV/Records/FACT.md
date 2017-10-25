---
layout: falloutnvrec
title: fopdoc
---
FACT
====

Faction

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
-* | [XNAM](Subrecords/XNAM (FACT, RACE).html) | Relation | struct |
 | DATA | Data | struct |
 | CNAM | Unused | float32 |
-* | | Rank | collection | See below for details.
 | WMI1 | Reputation | formid | FormID of a [REPU](REPU.html) record.

### DATA

Name | Type | Info
-----|------|-----
Flags 1 | uint8 | See below for values.
Flags 2 | uint8 | See below for values.
Unused | byte[2] |

#### Flags 1 Values

Value | Meaning
------|--------
0x01 | Hidden From PC
0x02 | Evil
0x04 | Special Combat

#### Flags 2 Values

Value | Meaning
------|--------
0x01 | Track Crime
0x02 | Allow Sell


### Rank Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | RNAM | Rank Number | int32 |
 | MNAM | Male | cstring |
 | FNAM | Female | cstring |
 | INAM | Insignia (unused) | cstring |
