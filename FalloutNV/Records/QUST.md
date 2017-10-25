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
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.html) record.
 | FULL | Name | cstring |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
+ | DATA | General | struct |
-* | CTDA | Condition | struct | [FO3](../../Fallout3/Records/Subrecords/CTDA.html) and [FNV](../../FalloutNV/Records/Subrecords/CTDA.html) definitions differ.
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
-* | CTDA | Condition | struct | [FO3](../../Fallout3/Records/Subrecords/CTDA.html) and [FNV](../../FalloutNV/Records/Subrecords/CTDA.html) definitions differ.
 | CNAM | Log Entry | cstring |
+ | | Embedded Script | collection | [FO3](../../Fallout3/Records/Subrecords/Script.html) and [FNV](../../FalloutNV/Records/Subrecords/Script.html) definitions differ.
 | NAM0 | Next Quest | formid | FormID of a [QUST](QUST.html) record.

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
-* | CTDA | Condition | struct | [FO3](../../Fallout3/Records/Subrecords/CTDA.html) and [FNV](../../FalloutNV/Records/Subrecords/CTDA.html) definitions differ.

##### QSTA

Name | Type | Info
-----|------|-----
Target | formid | FormID of a REFR ([FO3](../../Fallout3/Records/REFR.html), [FNV](../../FalloutNV/Records/REFR.html)), PGRE ([FO3](../../Fallout3/Records/PGRE.html), [FNV](../../FalloutNV/Records/PGRE.html)), PMIS ([FO3](../../Fallout3/Records/PMIS.html), [FNV](../../FalloutNV/Records/PMIS.html)), ACRE ([FO3](../../Fallout3/Records/ACRE.html), [FNV](../../FalloutNV/Records/ACRE.html)) or ACHR ([FO3](../../Fallout3/Records/ACHR.html), [FNV](../../FalloutNV/Records/ACHR.html)) record.
Flags | uint8 | See below for values.
Unused | byte[3] |

###### Flag Values

Value | Meaning
------|--------
0x01 | Compass Marker Ignores Locks
