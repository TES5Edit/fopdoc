PACK
====

Package

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | PKDT | General | struct |
 
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
0x0002 | ?? | No Sleeping | Sit Down | 
0x0004 | ?? | No Conversation | | Remain Near Reference to Guard
0x0008 | ?? | No Idle Markers | | 
0x0010 | ?? | No Furniture | | 
0x0020 | ?? | No Wandering | | 
0x0040 | ?? | | | 
0x0080 | ?? | | | 
0x0100 | Allow Buying | | Allow Buying | 
0x0200 | Allow Killing | | Allow Killing | 
0x0400 | Allow Stealing | | Allow Stealing | 
