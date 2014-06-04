INFO
====

Dialog Response

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | DATA | | struct |
+ | QSTI | Quest | formid | FormID of a [QUST](QUST.md) record.
 | TPIC | Topic | formid | FormID of a [DIAL](DIAL.md) record.
 | PNAM | Previous INFO | formid | FormID of an [INFO](INFO.md) record, or null.
-* | NAME | Topic | formid | FormID of a [DIAL](DIAL.md) record.
-* | | Response | collection | See below for details.
-* | [CTDA](Subrecords/CTDA.md) | Condition | struct |
-* | TCLT | Choice | formid | FormID of a [DIAL](DIAL.md) record.
-* | TCLF | Link From Topic | formid | FormID of a [DIAL](DIAL.md) record.
-* | TCFU | ?? | formid | FormID of an [INFO](INFO.md) record.
+ | | [Embedded Script (Begin)](Subrecords/Script.md) | collection |
+ | NEXT | Marker | null |
+ | | [Embedded Script (End)](Subrecords/Script.md) | collection |
 | SNDD | Unused | formid | FormID of a [SOUN](SOUN.md) record.
 | RNAM | Prompt | cstring |
 | ANAM | Speaker | formid | FormID of a [CREA](CREA.md) or [NPC_](NPC_.md) record.
 | KNAM | Actor Value / Perk | formid | FormID of a [AVIF](AVIF.md) or [PERK](PERK.md) record.
 | DNAM | Speech Challenge | uint32 | Enum - see below for values

### DATA

Name | Type | Info
-----|------|-----
Type | uint8 | Enum - see below for values.
Next Speaker | uint8 | Enum - see below for values.
Flags | uint16 | See below for details.

#### Type Values

Value | Meaning
------|--------
0 | Topic
1 | Conversation
2 | Combat
3 | Persuasion
4 | Detection
5 | Service
6 | Miscellaneous
7 | Radio

#### Next Speaker Values

Value | Meaning
------|--------
0 | Target
1 | Self
2 | Either

#### Flag Values

Value | Meaning
------|--------
0x0001 | Goodbye
0x0002 | Random
0x0004 | Say Once
0x0008 | Run Immediately
0x0010 | Info Refusal
0x0020 | Random End
0x0040 | Run For Rumors
0x0080 | Speech Challenge
0x0100 | Say Once A Day
0x0200 | Always Darken
0x0400 | ??
0x0800 | ??
0x1000 | Low Intelligence
0x2000 | High Intelligence

### Response Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | TRDT | Response Data | struct |
+ | NAM1 | Response Text | cstring |
+ | NAM2 | Script Notes | cstring |
 | NAM3 | Edits | cstring |
 | SNAM | Speaker Animation | formid | FormID of an [IDLE](IDLE.md) record.
 | LNAM | Listener Animation | formid | FormID of an [IDLE](IDLE.md) record.

#### TRDT

Name | Type | Info
-----|------|-----
Emotion Type | uint32 | Enum - see below for values.
Emotion Value | int32 |
Unused | byte[4] |
Response Number | uint8 |
Unused | byte[3] |
Sound | formid | FormID of a [SOUN](SOUN.md) record, or null.
Flags | uint8 | See below for values.
Unused | byte[3] |

##### Emotion Type Values

Value | Meaning
------|--------
0 | Neutral
1 | Anger
2 | Disgust
3 | Fear
4 | Sad
5 | Happy
6 | Surprise
7 | Pained

##### Flag Values

Value | Meaning
------|--------
0x01 | Use Emotion Animation

### Speech Challenge Values

Value | Meaning
------|--------
0 | ---
1 | Very Easy
2 | Easy
3 | Average
4 | Hard
5 | Very Hard
