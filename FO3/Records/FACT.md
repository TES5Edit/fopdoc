FACT
====

Faction

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
-* | [XNAM](Fields/XNAM (FACT, RACE).md) | Relation | struct |
 | DATA | Data | struct |
 | CNAM | Unused | float32 |
-* | | Rank | collection | See below for details.

### DATA

Name | Type | Info
-----|------|-----
Flags 1 | uint8 | See below for values.
Flags 2 | uint8 | See below for values.
Unused | uint8[2] |

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


### Rank Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | RNAM | Rank Number | int32 |
 | MNAM | Male | cstring |
 | FNAM | Female | cstring |
 | INAM | Insignia (unused) | cstring |
