LSCT
====

Load Screen Type

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | DATA | Data | struct |

### DATA

Name | Type | Info
-----|------|-----
Type | uint32 | Enum - see values below.
X | uint32 |
Y | uint32 |
Width | uint32 |
Height | uint32 |
Orientation | float32 |
Font 1 | uint32 | Enum - see values below.
Font 1 Color - Red | float32 |
Font 1 Color - Green | float32 |
Font 1 Color - Blue | float32 |
Font 1 Alignment | uint32 | Enum - see values below.
Unknown | byte[20] |
Font 2 | uint32 | Enum - see values below.
Font 2 Color - Red | float32 |
Font 2 Color - Green | float32 |
Font 2 Color - Blue | float32 |
Unknown | byte[4] |
Stats | uint32 | Enum - see values below.

#### Type Values

Value | Meaning
------|--------
0 | None
1 | XP Progress
2 | Objective
3 | Tip
4 | Stats

#### Font 1 / 2 Values

Value | Meaning
------|--------
0 | ??
1 | 2
2 | 3
3 | 4
4 | 5
5 | 6
6 | 7
7 | 8

#### Font 1 / 2 Alignment Values

Value | Meaning
------|--------
0 | ??
1 | Left
2 | Center
3 | ??
4 | Right