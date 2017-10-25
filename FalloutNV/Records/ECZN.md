---
layout: falloutnvrec
title: fopdoc
---
ECZN
====

Encounter Zone

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | DATA | | struct |

### DATA

Name | Type | Info
-----|------|-----
Owner | formid | FormID of an [NPC_](NPC_.html) or [FACT](FACT.html) record, or null.
Rank | int8 |
Minnimum Level | int8 |
Flags | uint8 | See below for values.
Unused | byte | 
 
#### Flag Values

Value | Meaning
------|--------
0x01 | Never Resets
0x02 | Match PC Below Minimum Level

