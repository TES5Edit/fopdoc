---
layout: falloutnvrec
title: fopdoc
---
QUST
====

Quest

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | FULL | Name | cstring |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
+ | DATA | General | struct |
-* | CTDA | Condition | struct | [FO3](../../Fallout3/Records/Subrecords/CTDA.md) and [FNV](../../FalloutNV/Records/Subrecords/CTDA.md) definitions differ.
-* | | Stage | collection | See below for details.
-* | | Objective | collection | See below for details.

### DATA

Name | Type | Info
-----|------|-----
Flags | uint8 | See below for values.
Priority | uint8 |
Unused | byte[2] |
Quest Delay | float32 |

#### Flag Values

Value | Meaning
------|--------
0x01 | Start Game Enabled
0x02 | ??
0x04 | Allow Repeated Conversation Topics
0x08 | Allow Repeated Stages
0x10 | ??

### Stage Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | INDX | Stage Index | int16 |
-* | | Log Entry | collection | See below for details.

#### Log Entry Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | Stage Flags | uint8 | See below for values.
-* | CTDA | Condition | struct | [FO3](../../Fallout3/Records/Subrecords/CTDA.md) and [FNV](../../FalloutNV/Records/Subrecords/CTDA.md) definitions differ.
 | CNAM | Log Entry | cstring |
+ | | Embedded Script | collection | [FO3](../../Fallout3/Records/Subrecords/Script.md) and [FNV](../../FalloutNV/Records/Subrecords/Script.md) definitions differ.
 | NAM0 | Next Quest | formid | FormID of a [QUST](QUST.md) record.

##### Stage Flag Values

Value | Meaning
------|--------
0x01 | Complete Quest
0x02 | Fail Quest

### Objective Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | QOBJ | Objective Index | int32 |
+ | NNAM | Description | cstring |
-* | | Target | collection | See below for details.

#### Target Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | QSTA | Target | struct |
-* | CTDA | Condition | struct | [FO3](../../Fallout3/Records/Subrecords/CTDA.md) and [FNV](../../FalloutNV/Records/Subrecords/CTDA.md) definitions differ.

##### QSTA

Name | Type | Info
-----|------|-----
Target | formid | FormID of a REFR ([FO3](../../Fallout3/Records/REFR.md), [FNV](../../FalloutNV/Records/REFR.md)), PGRE ([FO3](../../Fallout3/Records/PGRE.md), [FNV](../../FalloutNV/Records/PGRE.md)), PMIS ([FO3](../../Fallout3/Records/PMIS.md), [FNV](../../FalloutNV/Records/PMIS.md)), ACRE ([FO3](../../Fallout3/Records/ACRE.md), [FNV](../../FalloutNV/Records/ACRE.md)) or ACHR ([FO3](../../Fallout3/Records/ACHR.md), [FNV](../../FalloutNV/Records/ACHR.md)) record.
Flags | uint8 | See below for values.
Unused | byte[3] |

###### Flag Values

Value | Meaning
------|--------
0x01 | Compass Marker Ignores Locks
