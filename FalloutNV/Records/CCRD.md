CCRD
====

Caravan Card

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
 | ICON | Large Icon Filename | cstring |
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
 | TX00 | High Res Image - Face | cstring |
 | TX01 | High Res Image - Back | cstring |
 | INTV | Card Suit | uint32 | Enum - see values below.
 | INTV | Card Value | uint32 | Enum - see values below.
 | DATA | Value | uint32 |

### INTV Card Suit Values

Value | Meaning
------|--------
0 | ??
1 | Hearts
2 | Spades
3 | Diamonds
4 | Clubs
5 | Joker

### INTV Card Value Values

Value | Meaning
------|--------
0 | ??
1 | Ace
2 | 2
3 | 3
4 | 4
5 | 5
6 | 6
7 | 7
8 | 8
9 | 9
10 | 10
11 | ??
12 | Jack
13 | Queen
14 | King
15 | Joker
