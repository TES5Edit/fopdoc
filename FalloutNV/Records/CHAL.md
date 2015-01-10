CHAL
====

Challenge

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
 | ICON | Path to icon texture, when viewed in PipBoy | cstring | Optional
 | MICO | Path to icon texture, when viewed in upper-left message | cstring | Optional
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | DESC | Description | cstring |
 | DATA | Data | struct |
 | SNAM | Value3 | FormID | Depends on DATA.Type
 | XNAM | Value4 | FormID | Depends on Data.Type

### DATA

Name | Type | Info
-----|------|-----
Type | uint32 | Enum - see values below.
Threshold | uint32 |
Flags | uint32 | See values below.
Interval | uint32 |
Value1 | byte[2] | Depends on Type
Value2 | byte[2] | Depends on Type
Value3 | byte[4] | Depends on Type

#### Type Values

Value | Meaning |
------|---------|
0 | Kill From A Form List
1 | Kill A Specific FormID
2 | Kill Any In A Category
3 | Hit An Enemy
4 | Discover A Map Marker
5 | Use An Item
6 | Acquire An Item
7 | Use A Skill
8 | Do Damage
9 | Use An Item From A List
10 | Acquire An Item From A List
11 | Miscellaneous Stat
12 | Craft Using An Item
13 | Scripted Challenge

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Start Disabled
0x00000002 | Recurring
0x00000004 | Show Zero Progress
