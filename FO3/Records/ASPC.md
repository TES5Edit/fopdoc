ASPC
====

Acoustic Space

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | SNAM | Sound - Looping | formid | FormID of a [SOUN](SOUN.md) record.
 | RDAT | Use Sound from Region (Interiors Only) | formid | FormID of a [REGN](REGN.md) record.
+ | ANAM | Environment Type | uint32 | Enum - see below for values.

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
