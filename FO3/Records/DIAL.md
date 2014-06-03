DIAL
====

Dialog Topic

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
-* | QSTI | Quest | formid | FormID of a [QUST](QUST.md) record.
-* | QSTR | Quest | formid | FormID of a [QUST](QUST.md) record.
+ | FULL | Name | cstring |
+ | PNAM | Priority | float32 |
+ | DATA | Data | struct |

### DATA

Name | Type | Info
-----|------|-----
Type | uint8 | Enum - see below for values.
Flags | uint8 | See below for values.
 
#### Type Enum Values

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

#### Flag Values

Value | Meaning
------|--------
0x01 | Rumors
0x02 | Top-Level

