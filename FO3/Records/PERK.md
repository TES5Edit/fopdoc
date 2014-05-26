PERK
====

Perk

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
+ | DESC | Description | cstring |
 | ICON | Large icon filename | cstring | 
 | MICO | Small icon filename | cstring | 
-* | [CTDA](Fields/CTDA.md) | Condition | struct |
+ | DATA | Data | struct |
-* | | Effect | | This is a field collection - see below for details.

### DATA

Count | Name | Type | Info
------|------|------|-----
 | Trait | uint8 | Enum - see below for values.
 | Min Level | uint8 |
 | Ranks | uint8 |
 | Playable | uint8 | Enum -see below for values.
 | Hidden | uint8 | Enum -see below for values.
 
#### Trait / Playable / Hidden Enum Values

Value | Meaning
------|--------
0 | No
1 | Yes

### Effect Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | PRKE | Header | struct |
+ | DATA | Effect Data | struct *or * formid |
-* | | Perk Conditions | | A field collection - see below for details.
 | EPFT | Entry Point Function Type | uint8 |
 | EPFD | Entry Point Function Data | uint8[] *or* float32 *or* formid *or* null |
 | EPF2 | Button Label | cstring |
 | EPF3 | Script Flags | uint16 | See below for values.
 | | [Embedded Script](Fields/Script.md) | | Patrol data. A field collection.
+ | PRKF | End Marker | null | Flag

 
#### PRKE

Count | Name | Type | Info
------|------|------|-----
 | Type | uint8 | Enum -see below for values.
 | Rank | uint8 |
 | Priority | uint8 |
 
##### Type Enum Values

Value | Meaning
------|--------
0 | Quest + Stage
1 | Ability
2 | Entry Point



