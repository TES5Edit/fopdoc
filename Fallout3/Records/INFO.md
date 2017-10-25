---
layout: fallout3rec
title: fopdoc
---
INFO
====

Dialog Response

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | DATA | | struct |
+ | QSTI | Quest | formid | FormID of a [QUST](QUST.html) record.
 | TPIC | Topic | formid | FormID of a [DIAL](DIAL.html) record.
 | PNAM | Previous INFO | formid | FormID of an [INFO](INFO.html) record, or null.
-* | NAME | Topic | formid | FormID of a [DIAL](DIAL.html) record.
-* | | Response | collection | See below for details.
-* | [CTDA](Subrecords/CTDA.html) | Condition | struct |
-* | TCLT | Choice | formid | FormID of a [DIAL](DIAL.html) record.
-* | TCLF | Link From Topic | formid | FormID of a [DIAL](DIAL.html) record.
+ | | [Embedded Script (Begin)](Subrecords/Script.html) | collection |
+ | NEXT | Marker | null |
+ | | [Embedded Script (End)](Subrecords/Script.html) | collection |
 | SNDD | Unused | formid | FormID of a [SOUN](SOUN.html) record.
 | RNAM | Prompt | cstring |
 | ANAM | Speaker | formid | FormID of a [CREA](CREA.html) or [NPC_](NPC_.html) record.
 | KNAM | Actor Value / Perk | formid | FormID of a [AVIF](AVIF.html) or [PERK](PERK.html) record.
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

### Response Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | TRDT | Response Data | struct |
+ | NAM1 | Response Text | cstring |
+ | NAM2 | Script Notes | cstring |
 | NAM3 | Edits | cstring |
 | SNAM | Speaker Animation | formid | FormID of an [IDLE](IDLE.html) record.
 | LNAM | Listener Animation | formid | FormID of an [IDLE](IDLE.html) record.

#### TRDT

Name | Type | Info
-----|------|-----
Emotion Type | uint32 | Enum - see below for values.
Emotion Value | int32 |
Unused | byte[4] |
Response Number | uint8 |
Unused | byte[3] |
Sound | formid | FormID of a [SOUN](SOUN.html) record, or null.
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
