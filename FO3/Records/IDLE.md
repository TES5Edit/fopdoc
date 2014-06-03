IDLE
====

Idle Animation

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
+ | | [Model Data](Fields/Model.md) | collection |
-* | [CTDA](Fields/CTDA.md) | Condition | struct |
+* | ANAM | Related Idle Animation | formid | FormID of an [IDLE](IDLE.md) record, or null. The first ANAM field is for the parent, the second for the previous sibling.
+ | DATA | | struct |

### DATA

Name | Type | Info
-----|------|-----
Animation Group Section | uint8 | See below for values.
Looping Min | uint8 |
Looping Max | uint8 |
Unused | uint8 |
Replay Delay | int16 |
Flags | uint8 | See below for values.
Unused | uint8 |
 
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
