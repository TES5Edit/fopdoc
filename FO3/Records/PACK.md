PACK
====

Package

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | PKDT | General | struct |
-* | | Location | | A field collection, see below for details.
+ | PSDT | Schedule | struct |
 | PTDT | Target 1 | struct |
-* | [CTDA](Fields/CTDA.md) | Condition | struct |
+ | IDLF | Idle Animation Flags | uint8 | See below for values.
+ | IDLC | Idle Animation Count | struct |
+ | IDLT | Idle Timer Setting | float32 |
+* | IDLA | Idle Animations | formid | FormID of an [IDLE](IDLE.md) record.
 | IDLB | Unused | uint8[4] |
 | CNAM | Combat Style | formid | FormID of a [CSTY](CSTY.md) record.
 | PKED | Eat Marker | null |
 | PKE2 | Escort Distance | uint32 |
 | PKFD | Follow - Start Location - Trigger Radius | float32 |
 | PKPT | Patrol Flags | uint16 |
 | PKW3 | Use Weapon Data | struct |
 | PTD2 | Target 2 | struct |
 | PUID | Use Item Marker | null |
 | PKAM | Ambush Marker | null |
 | PKDD | Dialog Data | struct |
 | PLD2 | Location 2 (repeated??) | struct |
+ | POBA | OnBegin Marker | null |
+ | INAM | OnBegin Idle | formid | FormID of an [IDLE](IDLE.md) record, or null.
+ | | [OnBegin Embedded Script](Fields/Script.md) | | A field collection.
+ | TNAM | OnBegin Topic | formid | FormID of a [DIAL](DIAL.md) record, or null.
+ | POBA | OnEnd Marker | null |
+ | INAM | OnEnd Idle | formid | FormID of an [IDLE](IDLE.md) record, or null.
+ | | [OnEnd Embedded Script](Fields/Script.md) | | A field collection.
+ | TNAM | OnEnd Topic | formid | FormID of a [DIAL](DIAL.md) record, or null.
+ | POBA | OnChange Marker | null |
+ | INAM | OnChange Idle | formid | FormID of an [IDLE](IDLE.md) record, or null.
+ | | [OnChange Embedded Script](Fields/Script.md) | | A field collection.
+ | TNAM | OnChange Topic | formid | FormID of a [DIAL](DIAL.md) record, or null.
 

### PKDT

Count | Name | Type | Info
------|------|------|-----
 | General Flags | uint32 | See below for values.
 | Type | uint8 | Enum - see below for values.
 | Unused | uint8 |
 | Fallout Behaviour Flags | uint16 | See below for values.
 | Type-Specific Flags | null *or* uint16 | See below for values. The value of the Type field determines how flag values are interpreted.
 | Unused | uint8[2] |

#### General Flag Values

Value | Meaning
------|--------
0x00000001 | Offers Services
0x00000002 | Must reach location
0x00000004 | Must complete
0x00000008 | Lock doors at package start
0x00000010 | Lock doors at package end
0x00000020 | Lock doors at location
0x00000040 | Unlock doors at package start
0x00000080 | Unlock doors at package end
0x00000100 | Unlock doors at location
0x00000200 | Continue if PC near
0x00000400 | Once per day
0x00000800 | ??
0x00001000 | Skip fallout behavior
0x00002000 | Always run
0x00004000 | ??
0x00008000 | ??
0x00010000 | ??
0x00020000 | Always sneak
0x00040000 | Allow swimming
0x00080000 | Allow falls
0x00100000 | Head-Tracking off
0x00200000 | Weapons unequipped
0x00400000 | Defensive combat
0x00800000 | Weapon Drawn
0x01000000 | No idle anims
0x02000000 | Pretend In Combat
0x04000000 | Continue During Combat
0x08000000 | No Combat Alert
0x10000000 | No Warn/Attack Behaviour
0x20000000 | ??
0x40000000 | ??
0x80000000 | ??

#### Type Values

Value | Meaning
------|--------
0 | Find
1 | Follow
2 | Escort
3 | Eat
4 | Sleep
5 | Wander
6 | Travel
7 | Accompany
8 | Use Item At
9 | Ambush
10 | Flee Not Combat
11 | ??
12 | Sandbox
13 | Patrol
14 | Guard
15 | Dialogue
16 | Use Weapon

#### Fallout Behaviour Flags

Value | Meaning
------|--------
0x0001 | Hellos To Player
0x0002 | Random Conversations
0x0004 | Observe Combat Behavior
0x0008 | ??
0x0010 | Reaction To Player Actions
0x0020 | Friendly Fire Comments
0x0040 | Aggro Radius Behavior
0x0080 | Allow Idle Chatter
0x0100 | Avoid Radiation

#### Type-Specific Flags

The `Follow`, `Sleep`, `Travel`, `Accompany`, `Flee Not Combat`, `??`, `Patrol`, `Dialogue` and `Use Weapon` types have no flags.

Value | Meaning (Find / Escort / Eat) | Meaning (Wander / Sandbox) | Meaning (Use Item At) | Meaning (Ambush) | Meaning (Guard)
------|-------------------------------|------------------|-----------------------|------------------|---------------
0x0001 | ?? | No Eating | | Hide While Ambushing | 
0x0002 | ?? | No Sleeping | Sit Down | |
0x0004 | ?? | No Conversation | | | Remain Near Reference to Guard
0x0008 | ?? | No Idle Markers | | |
0x0010 | ?? | No Furniture | | |
0x0020 | ?? | No Wandering | | |
0x0040 | ?? | | | |
0x0080 | ?? | | | |
0x0100 | Allow Buying | | Allow Buying | 
0x0200 | Allow Killing | | Allow Killing | 
0x0400 | Allow Stealing | | Allow Stealing | 

### Location Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | PLDT | Location 1 | struct |
 | PLD2 | Location 2 | struct |
 
#### PLDT / PLD2

Count | Name | Type | Info
------|------|------|-----
 | Type | uint32 | Enum - see below for values.
 | Location | formid *or* uint32 *or* uint8[] | See below for data type info.
 | Radius | int32 |
 
##### Type Values & Location Data Types

Type Value | Meaning | Location Data Type Info
-----------|---------|------------------------
0 | Near Reference | FormID of a [REFR](REFR.md), [PGRE](PGRE.md), [PMIS](PMIS.md), [ACHR](ACHR.md), [ACRE](ACRE.md) or [PLYR](PLYR.md) record.
1 | In Cell | FormID of a [CELL](CELL.md) record.
2 | Near Current Location | ??
3 | Near Editor Location | ??
4 | Object ID | FormID of a [ACTI](ACTI.md), [DOOR](DOOR.md), [STAT](STAT.md), [FURN](FURN.md), [CREA](CREA.md), [SPEL](SPEL.md), [NPC_](NPC_.md), [CONT](CONT.md), [ARMO](ARMO.md), [AMMO](AMMO.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [KEYM](KEYM.md), [ALCH](ALCH.md) or [LIGH](LIGH.md) record.
5 | Object Type | Enum - see below for values.
6 | Near Linked Reference | ??
7 | At Package Location | ??

### PSDT

Count | Name | Type | Info
------|------|------|-----
 | Month | int8 |
 | Day of Week | int8 | Enum - see below for values.
 | Date | uint8 |
 | Time | int8 |
 | Duration | int32 |

#### Day of Week Values

Value | Meaning
------|--------
-1 | Any
0 | Sunday
1 | Monday
2 | Tuesday
3 | Wednesday
4 | Thursday
5 | Friday
6 | Saturday
7 | Weekdays
8 | Weekends
9 | Monday, Wednesday, Friday
10 | Tuesday, Thursday

### PTDT / PTD2

Count | Name | Type | Info
------|------|------|-----
 | Type | int32 | Enum - see below for values.
 | Target | formid *or* uint32 *or* uint8[] |
 | Count / Distance | int32 |
 | Unknown | float32 |

#### Type Values & Target Data Types

Type Value | Meaning | Target Data Type Info
-----------|---------|----------------------
0 | Specific Reference | FormID of a [REFR](REFR.md), [PGRE](PGRE.md), [PMIS](PMIS.md), [ACHR](ACHR.md), [ACRE](ACRE.md) or [PLYR](PLYR.md) record.
1 | Object ID | FormID of a [ACTI](ACTI.md), [DOOR](DOOR.md), [STAT](STAT.md), [FURN](FURN.md), [CREA](CREA.md), [SPEL](SPEL.md), [NPC_](NPC_.md), [LVLN](LVLN.md), [LVLC](LVLC.md), [CONT](CONT.md), [ARMO](ARMO.md), [AMMO](AMMO.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [KEYM](KEYM.md), [ALCH](ALCH.md), [LIGH](LIGH.md), [FACT](FACT.md) or [FLST](FLST.md) record.
2 | Object Type | Enum - see below for values.
3 | Linked Reference | ??

### Object Type Values

Value | Meaning
------|--------
0 | None
1 | Activators
2 | Armor
3 | Books
4 | Clothing
5 | Containers
6 | Doors
7 | Ingredients
8 | Lights
9 | Misc
10 | Flora
11 | Furniture
12 | Weapons: Any
13 | Ammo
14 | NPCs
15 | Creatures
16 | Keys
17 | Alchemy
18 | Food
19 | All: Combat Wearable
20 | All: Wearable
21 | Weapons: Ranged
22 | Weapons: Melee
23 | Weapons: NONE
24 | Actor Effects: Any
25 | Actor Effects: Range Target
26 | Actor Effects: Range Touch
27 | Actor Effects: Range Self
28 | ??
29 | Actors: Any

### Idle Animation Flag Values

Value | Meaning
------|--------
0x01 | Run In Sequence
0x02 | ??
0x04 | Do Once

### IDLC

Count | Name | Type | Info
------|------|------|-----
 | Animation Count | uint8 |
 | Unused | uint8[3] |

### PKPT

Count | Name | Type | Info
------|------|------|-----
 | Repeatable | uint8 | A value of `0` means `Not Repeatable`, and a value of `1` means `Repeatable`.
 | Unused | uint8 |
 
### PKW3

Count | Name | Type | Info
------|------|------|-----
 | Flags | uint32 | See below for values.
 | Fire Rate | uint8 | Enum - see below for values.
 | Fire Count | uint8 | Enum - see below for values.
 | Number of Bursts | uint16 |
 | Shots Per Volley (Min) | uint16 |
 | Shots Per Volley (Max) | uint16 |
 | Pause Between Volleys (Min) | float32 |
 | Pause Between Volleys (Max) | float32 |
 | Unused | uint8[4] |
 
#### Flag Values

Value | Meaning
------|--------
0x00000001 | Always Hit
0x00000002 | ??
0x00000004 | ??
0x00000008 | ??
0x00000010 | ??
0x00000020 | ??
0x00000040 | ??
0x00000080 | ??
0x00000100 | Do No Damage
0x00000200 | ??
0x00000400 | ??
0x00000800 | ??
0x00001000 | ??
0x00002000 | ??
0x00004000 | ??
0x00008000 | ??
0x00010000 | Crouch To Reload
0x00020000 | ??
0x00040000 | ??
0x00080000 | ??
0x00100000 | ??
0x00200000 | ??
0x00400000 | ??
0x00800000 | ??
0x01000000 | Hold Fire When Blocked

#### Fire Rate Values

Value | Meaning
------|--------
0 | Auto Fire
1 | Volley Fire

#### Fire Count Values

Value | Meaning
------|--------
0 | Number of Bursts
1 | Repeat Fire

### PKDD

Count | Name | Type | Info
------|------|------|-----
 | FOV | float32 |
 | Topic | formid | FormID of a [DIAL](DIAL.md) record, or null.
 | Flags | uint32 | See below for values.
 | Unused | uint8[4] |
 | Dialog Type | uint32 | Enum - see below for values.
 
#### Flag Values

Value | Meaning
------|--------
0x00000001 | No Headtracking
0x00000002 | ??
0x00000004 | ??
0x00000008 | ??
0x00000010 | ??
0x00000020 | ??
0x00000040 | ??
0x00000080 | ??
0x00000100 | Don't Control Target Movement

#### Dialog Type Values

Value | Meaning
------|--------
0 | Say Tosation
1 | Say To


