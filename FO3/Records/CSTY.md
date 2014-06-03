CSTY
====

Combat Style

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | CSTD | Advanced - Standard | struct |
+ | CSAD | Advanced - Advanced | struct |
+ | CSSD | Simple | struct |

### CSTD

Name | Type | Info
-----|------|-----
Maneuver Decision - Dodge % Chance | uint8 |
Maneuver Decision - Left/Right % Chance | uint8 |
Unused | byte[2] |
Maneuver Decision - Dodge L/R Timer Min | float32 |
Maneuver Decision - Dodge L/R Timer Max | float32 |
Maneuver Decision - Dodge Forward Timer Min | float32 |
Maneuver Decision - Dodge Forward Timer Max | float32 |
Maneuver Decision - Dodge Back Timer Min | float32 |
Maneuver Decision - Dodge Back Timer Max | float32 |
Maneuver Decision - Dodge Idle Timer Min | float32 |
Maneuver Decision - Dodge Idle Timer Max | float32 |
Melee Decision - Block % Chance | uint8 |
Melee Decision - Attack % Chance | uint8 |
Unused | byte[2] |
Melee Decision - Recoil/Stagger Bonus to Attack | float32 |
Melee Decision - Unconscious Bonus to Attack | float32 |
Melee Decision - Hand-To-Hand Bonus to Attack | float32 |
Melee Decision - Power Attacks - Power Attack % Chance | uint8 |
Unused | byte[3] |
Melee Decision - Power Attacks - Recoil/Stagger Bonus to Power | float32 |
Melee Decision - Power Attacks - Unconscious Bonus to Power Attack | float32 |
Melee Decision - Power Attacks - Normal | uint8 |
Melee Decision - Power Attacks - Forward | uint8 |
Melee Decision - Power Attacks - Back | uint8 |
Melee Decision - Power Attacks - Left | uint8 |
Melee Decision - Power Attacks - Right | uint8 |
Unused | byte[3] |
Melee Decision - Hold Timer Min | float32 |
Melee Decision - Hold Timer Max | float32 |
Flags | uint16 | See below for values.
Unused | byte[2] |
Maneuver Decision - Acrobatic Dodge & Chance | uint8 |
Melee Decision - Power Attacks - Rushing Attack % Chance | uint8 |
Unused | byte[2] |
Melee Decision - Power Attacks - Rushing Attack Distance Mult | float32 |
 
#### Flag Values

Value | Meaning
------|--------
0x0001 | Choose Attack Using % Chance
0x0002 | Melee Alert OK
0x0004 | Flee Based on Personal Survival
0x0008 | ??
0x0010 | Ignore Threats
0x0020 | Ignore Damaging Self
0x0040 | Ignore Damaging Group
0x0080 | Ignore Damaging Spectators
0x0100 | Cannot Use Stealthboy
 
 
### CSAD

Name | Type | Info
-----|------|-----
Dodge Fatigue Mod Mult | float32 |
Dodge Fatigue Mod Base | float32 |
Encumb. Speed Mod Base | float32 |
Encumb. Speed Mod Mult | float32 |
Dodge While Under Attack Mult | float32 |
Dodge Not Under Attack Mult | float32 |
Dodge Back While Under Attack Mult | float32 |
Dodge Back Not Under Attack Mult | float32 |
Dodge Forward While Attacking Mult | float32 |
Dodge Forward Not Attacking Mult | float32 |
Block Skill Modifier Mult | float32 |
Block Skill Modifier Base | float32 |
Block While Under Attack Mult | float32 |
Block Not Under Attack Mult | float32 |
Attack Skill Modifier Mult | float32 |
Attack Skill Modifier Base | float32 |
Attack While Under Attack Mult | float32 |
Attack Not Under Attack Mult | float32 |
Attack During Block Mult | float32 |
Power Att. Fatigue Mod Base | float32 |
Power Att. Fatigue Mod Mult | float32 |

### CSSD

Name | Type | Info
-----|------|-----
Cover Search Radius | float32 |
Take Cover Chance | float32 |
Wait Timer Min | float32 |
Wait Timer Max | float32 |
Wait to Fire Timer Min | float32 |
Wait to Fire Timer Max | float32 |
Fire Timer Min | float32 |
Fire Timer Max | float32 |
Ranged Weapon Range Mult Min | float32 |
Unused | byte[4] |
Weapon Restrictions | uint32 | Enum - see below for values.
Ranged Weapon Range Mult (max) | float32 |
Max Targeting FOV | float32 |
Combat Radius | float32 |
Semi-Auto Firing Delay Mult Min | float32 |
Semi-Auto Firing Delay Mult Max | float32 |

#### Weapon Restrictions Enum Values

Value | Meaning
------|--------
0 | None
1 | Melee Only
2 | Ranged Only
