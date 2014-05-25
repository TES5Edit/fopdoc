FACT
====

Faction

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
-* | XNAM | Relation | struct |
 | DATA | Data | struct |
 | CNAM | Unused | float32 |
-* | | Rank | | This is a field collection, see below for details.


### XNAM

Count | Name | Type | Info
------|------|------|-----
 | Faction | formid | FormID of a [FACT](FACT.md) or [RACE](RACE.md) record.
 | Modifier | int32 |
 | Group Combat Reaction | uint32 | Enum - see values below.
 
#### Group Combat Reaction Enum Values

Value | Meaning
------|--------
0 | Neutral
1 | Enemy
2 | Ally
3 | Friend

### DATA

Count | Name | Type | Info
------|------|------|-----
 | Flags 1 | uint8 | See below for values.
 | Flags 2 | uint8 | See below for values.
 | Unushed | uint8[2] |
 
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
