ACBS Field
==========

As used by the [CREA](../CREA.md) and [NPC_](../NPC_.md) record types.

## Format

Name | Type | Info
-----|------|-----
Flags | uint32 | See below for values.
Fatigue | uint16 | 
Barter Gold | uint16
Level / Level Mult | int16 | If the 0x00000080 flag is set, the value is divided by 1000 to give a multiplier.
Calc Min | uint16 | 
Calc Max | uint16 |
Speed Multiplier | uint16 |
Karma (Alignment) | float32 |
Disposition Base | int16 |
Template Flags | uint16 | See below for values.
 
### Flag Values

Flag values for [CREA](../CREA.md) and [NPC_](../NPC_.md) records differ.

Value | Meaning (CREA) | Meaning (NPC_)
------|----------------|---------------
0x00000001 | Biped | Female
0x00000002 | Essential | Essential
0x00000004 | Weapon & Shield | Is CharGen Face Preset
0x00000008 | Respawn | Respawn
0x00000010 | Swims | Auto-calc stats
0x00000020 | Flies | ??
0x00000040 | Walks | ??
0x00000080 | PC Level Mult | PC Level Mult
0x00000100 | ?? | Use Template
0x00000200 | No Low Level Processing | No Low Level Processing
0x00000400 | ?? | ??
0x00000800 | No Blood Spray | No Blood Spray
0x00001000 | No Blood Decal | No Blood Decal
0x00002000 | ?? | ??
0x00004000 | ?? | ??
0x00008000 | No Head | ??
0x00010000 | No Right Arm | ??
0x00020000 | No Left Arm | ??
0x00040000 | No Combat in Water | ??
0x00080000 | No Shadow | ??
0x00100000 | No VATS Melee | No VATS Melee
0x00200000 | Allow PC Dialogue | ??
0x00400000 | Can't Open Doors | Can be all races
0x00800000 | Immobile | ??
0x01000000 | Tilt Front/Back | ??
0x02000000 | Tilt Left/Right | ??
0x03000000 | No Knockdowns | No Knockdowns
0x08000000 | Not Pushable | Not Pushable
0x10000000 | Allow Pickpocket | ??
0x20000000 | Is Ghost | ??
0x40000000 | No Rotating To Head-track | No Rotating To Head-track
0x80000000 | Invulnerable | ??

### Template Flag Values

Value | Meaning
------|--------
0x0001 | Use Traits
0x0002 | Use Stats
0x0004 | Use Factions
0x0008 | Use Actor Effect List
0x0010 | Use AI Data
0x0020 | Use AI Packages
0x0040 | Use Model/Animation
0x0080 | Use Base Data
0x0100 | Use Inventory
0x0200 | Use Script
