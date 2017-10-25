---
layout: fallout4rec
title: fopdoc
---
FACT
====

Faction

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | editorID | zstring | Faction name
 | FULL | name | lstring | Full name
 | XNAM | Interfaction Relations | struct |
+ | DATA | flags | uint32 | See below for details
 | JAIL | Prison Marker | formid | REFR formid - The exterior jail marker for the faction's prison.
 | WAIT | Follower Wait Marker | formid | REFR formid - Marker the player's followers are assigned to wait at.
 | STOL | Evidence Chest | formid | REFR formid - Stolen goods are stored in this chest.
 | PLCN | Player Belongings Chest | formid  | REFR formid - Player's inventory is stored in this chest.
 | CRGR | Crime Group | formid | Crime Factions List (FLST)
 | JOUT | Jail Outfit | formid | OTFT formid - Jail outfit the player is given.
 | CRVA | Crime Gold | struct[12/16/20] | Size varies in record versions 30 and below, additional fields are those at the end of the structure
 | | Ranks | Collection | See Rank Subrecord Collection Below
 | VEND | Vendor List | formid | Merchandise list (FLST)
 | VENC | Vendor Chest | formid | Reference to vendor chest (REFR)
 | VENV | | struct[12] | All 0s unless vendor; always present in record versions 29 and above, never present in record versions 28 and below
 | PLVD | | struct[12] | Where to sell goods
 | CTDA | | struct | Conditions
 
 ** Existing Data Below Subject to change Copied from previous UESP **

### XNAM

Name | Type | Info
-----|------|-----
Faction | formid |
Mod | int32 | Appears to be unused - no longer editable in CK and only non-zero for CWDisaffectedSoldierFaction (0004BB3F)
Combat | int32 |

#### Combat

Value | Meaning
------|--------
1 | Neutral
2 | Enemy
3 | Ally
4 | Friend

### DATA

Name | Type | Info
-----|------|-----
Flags | uint32 | See below for values.

#### Flags

Value | Meaning
------|--------
0x01 | Hidden from PC
0x02 | Special Combat
0x40 | Track Crime
0x80 | Ignore Murder
0x100 | Ignore Assault
0x200 | Ignore Stealing
0x400 | Ignore Trespass
0x800 | Do not report crimes against members
0x1000 | Crime Gold, Use Defaults
0x2000 | Ignore Pickpocket
0x4000 | Vendor
0x8000 | Can Be Owner
0x10000 | Ignore Werewolf


### CRVA Values

Size | Value | Meaning
------|------|------
uint8 | 1 | Arrest
uint8 | 1 | Attack on Sight
uint16 | | Murder
uint16 | | Assault
uint16 | | Trespass
uint16 | | Pickpocket
uint16 | | Unused (usually 0, but not always, changing data has no effect in CK)
float | | Steal Mult.
uint16 | | Escape
uint16 | | Werewolf

### VENV Values

Size | Meaning
------|------
uint16 | Start hour
uint16 | End hour
uint32 | Radius
uint8 | 1 = Buys stolen items (wording in CK is misleading)
uint8 | 1 = NOT sell/buy (causes vendor to buy/sell everything ''except'' what's in the Vendor List)
uint16 | Unused

### PLVD Values

Size | Meaning
------|------
uint32 | Specification type
formID | meaning depends on previous int
uint32 | Unused

#### Specifications

Value | Meaning
------|--------
0 | Near Reference, REFR formID follows
1 | In Cell, CELL formID follows
2 | Near Package Start Location ''not used in original files''
3 | Near Editor Location''
6 | Linked Reference, KWYD formID follows ''not used in original files''
12 | Near Self

### Rank Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | RNAM | Rank Number | int32 |
 | MNAM | Male | cstring |
 | FNAM | Female | cstring |
