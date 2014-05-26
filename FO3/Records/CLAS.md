CLAS
====

Class

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | FULL | Name | cstring |
+ | DESC | Description | cstring |
 | ICON | Large icon filename | cstring |
 | MICO | Small icon filename | cstring |
+ | DATA | Data | struct |
+* | ATTR | Attribute | uint8 | There are 7 attribute fields, one for each attribute. The mapping of fields to attributes is given below.

### DATA

Count | Name | Type | Info
------|------|------|-----
-* | [Tag Skill](Values/Actor Values.md) | int32 | Enum - see link for values. There are 4 Tag Skill fields in this block.
 | Flags | uint32 | See below for values.
 | [Buys/Sells and Services](Values/Services.md) | uint32 | Flags. See the link for values.
 | [Teaches](Values/Skills.md) | int8 | See the link for enum values.
 | Maximum Training Level | uint8 |
 | Unused | uint8[2] |

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Playable
0x00000002 | Guard

### ATTR Map

ATTR Field | Attribute
-----------|----------
1st | Strength
2nd | Perception
3rd | Endurance
4th | Charisma
5th | Intelligence
6th | Agility
7th | Luck
