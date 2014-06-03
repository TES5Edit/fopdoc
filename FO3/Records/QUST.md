QUST
====

Quest

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | FULL | Name | cstring |
 | ICON | Large Icon Filename | cstring | 
 | MICO | Small Icon FIlename | cstring |
+ | DATA | General | struct |
-* | [CTDA](Fields/CTDA.md) | Condition | struct |
-* | | Stage | A field collection, see below for details.
-* | | Objective | A field collection, see below for details.
 
### DATA

Name | Type | Info
-----|------|-----
Flags | uint8 | See below for values.
Priority | uint8 |
Unused | uint8[2] |
Quest Delay | float32 |
 
#### Flag Values

Value | Meaning
------|--------
0x01 | Start Game Enabled
0x02 | ??
0x04 | Allow Repeated Conversation Topics
0x08 | Allow Repeated Stages
0x10 | ??

### Stage Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | INDX | Stage Index | int16 |
-* | | Log Entry | | A field collection, see below for details.

#### Log Entry Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | Stage Flags | uint8 | See below for values.
-* | [CTDA](Fields/CTDA.md) | Condition | struct |
 | CNAM | Log Entry | cstring |
+ | | [Embedded Script](Fields/Script.md) | | A field collection.
 | NAM0 | Next Quest | formid | FormID of a [QUST](QUST.md) record.

##### Stage Flag Values

Value | Meaning
------|--------
0x01 | Complete Quest
0x02 | Fail Quest

### Objective Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | QOBJ | Objective Index | int32 |
+ | NNAM | Description | cstring |
-* | | Target | | A field collection, see below for details.

#### Target Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | QSTA | Target | struct |
-* | [CTDA](Fields/CTDA.md) | Condition | struct |

##### QSTA

Name | Type | Info
-----|------|-----
Target | formid | FormID of a [REFR](REFR.md), [PGRE](PGRE.md), [PMIS](PMIS.md), [ACRE](ACRE.md) or [ACHR](ACHR.md) record.
Flags | uint8 | See below for values.
Unused | uint8[3] |

###### Flag Values

Value | Meaning
------|--------
0x01 | Compass Marker Ignores Locks
