---
layout: falloutnvrec
title: fopdoc
---
IDLE
====

Idle Animation

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
+ | | [Model Data](Subrecords/Model.html) | collection |
-* | [CTDA](Subrecords/CTDA.html) | Condition | struct |
 | ANAM | Related Idle Animations | struct |
+ | DATA | | struct |

### ANAM

Name | Type | Info
-----|------|-----
Parent Idle Animation | formid | FormID of a [IDLE](IDLE.html) record, or null.
Previous Sibling Idle Animation | formid | FormID of a [IDLE](IDLE.html) record, or null.

### DATA

Name | Type | Info
-----|------|-----
Animation Group Section | uint8 | See below for values.
Looping Min | uint8 |
Looping Max | uint8 |
Unused | byte |
Replay Delay | int16 |
Flags | uint8 | See below for values.
Unused | byte |

#### Animation Group Section Values

Value | Animation Group
------|----------------
0 | Idle
1 | Movement
2 | Left Arm
3 | Left Hand
4 | Weapon
5 | Weapon Up
6 | Weapon Down
7 | Special Idle
20 | Whole Body
21 | Upper Body

#### Flag Values

Value | Meaning
------|--------
0x01 | No Attacking
