CLAS Record
===========

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
- | EDID | Editor ID | cstring | Editor ID
- | FULL | Name | cstring | Name
- | DESC | Description | cstring | Description
- | ICON | Large Icon filename | cstring |
- | MICO | Small Icon filename | cstring | May not appear in an file.  FO3Edit defines both ICON and MICO for convenience.
+ | DATA | ?? | struct | 
+ | ATTR | Attributes | struct |

### DATA

 Name | Type | Info
------|------|------
Tag Skills | int32 | This is repeated 4 times
General Flags | uint32 | See General Flags
Buys/Sells and Services | uint32 | See Service Flags
Teaches | int8 | 
Maximum training level | unit8 | 
Unused | uint16

### General Flags
	
Flag | Meaning
-----|--------
0x00000001 | Playable
0x00000002 | Guard

### Service Flags

Flag | Meaning
-----|--------
0x00000001 | Weapons
0x00000002 | Armor
0x00000004 | Alcohol
0x00000008 | Books
0x00000010 | Food
0x00000020 | Chems
0x00000040 | Stimpacks
0x00000080 | Lights?
0x00000100 | unused*
0x00000200 | unused*
0x00000400 | Miscellaneous
0x00000800 | unused*
0x00001000 | unused*
0x00002000 | Potions?
0x00004000 | Training
0x00008000 | unused*
0x00010000 | Recharge
0x00020000 | Repair

### ATTR

Attribute Name | Type | Info
------|------|-----
Strength | uint8 | 
Perception | uint8 | 
Endurance | uint8 | 
Charisma | uint8 | 
Intelligence | uint8 | 
Agility | uint8 | 
Luck | uint8 | 