ASPC
====

Acoustic Space

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | SNAM | Dawn / Default Loop | formid | FormID of a [SOUN](SOUN.md) record, or null.
+ | SNAM | Afternoon | formid | FormID of a [SOUN](SOUN.md) record, or null.
+ | SNAM | Dusk | formid | FormID of a [SOUN](SOUN.md) record, or null.
+ | SNAM | Night | formid | FormID of a [SOUN](SOUN.md) record, or null.
+ | SNAM | Walla | formid | FormID of a [SOUN](SOUN.md) record, or null.
+ | WNAM | Walla Trigger Count | uint32 |
 | RDAT | Use Sound from Region (Interiors Only) | formid | FormID of a [REGN](REGN.md) record.
+ | ANAM | Environment Type | uint32 | Enum - see below for values.
+ | INAM | Is Interior | uint32 | Enum - see values below.

### ANAM Enum Values

Value | Meaning
------|--------
0 | None
1 | Default
2 | Generic
3 | Padded Cell
4 | Room
5 | Bathroom
6 | Livingroom
7 | Stone Room
8 | Auditorium
9 | Concerthall
10 | Cave
11 | Arena
12 | Hangar
13 | Carpeted Hallway
14 | Hallway
15 | Stone Corridor
16 | Alley
17 | Forest
18 | City
19 | Mountains
20 | Quarry
21 | Plain
22 | Parkinglot
23 | Sewerpipe
24 | Underwater
25 | Small Room
26 | Medium Room
27 | Large Room
28 | Medium Hall
29 | Large Hall
30 | Plate

### INAM Values

Value | Meaning
------|--------
1 | No
2 | Yes
