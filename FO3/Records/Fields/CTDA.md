CTDA Field
==========

## Format

Count | Name | Type | Info
------|------|------|-----
 | Type | uint8 | See values below.
 | Unused | uint8[3] |
 | Comparison Value | formid *or* float32 | If not a valid [GLOB](../GLOB.md) record FormID, is interpreted as a float32.
 | Function | uint32 | A function index. See below for a list of function indicies.
 | Parameter #1 | uint8[4] | First parameter to pass to the function. 
 | Parameter #2 | uint8[4] | Second parameter to pass to the function.
 | Run On | uint32 | Values and what they correspond to are given below.
 | Reference | formid | A FormID of a [PLYR](../PLYR.md), [ACHR](../ACHR.md), [ACRE](../ACRE.md), [REFR](../REFR.md), [PMIS](../PMIS.md) or [PGRE](../PGRE.md) reference on which to apply the function, or null.
 
### Type Values

Value | Meaning
------|--------
0x0001 | Combine conditions using OR (default is to use AND)
0x0002 | Run On Target
0x0004 | Use Global
0x0000 | Equal To
0x2000 | Not Equal To
0x4000 | Greater Than
0x6000 | Greater Than or Equal To
0x8000 | Less Than
0xA000 | Less Than or Equal To
 
### Function Indicies

Index | Function
------|---------
  1 | GetDistance
  5 | GetLocked
  6 | GetPos
  8 | GetAngle
 10 | GetStartingPos
 11 | GetStartingAngle
 12 | GetSecondsPassed
 14 | GetActorValue
 18 | GetCurrentTime
 24 | GetScale
 25 | IsMoving
 26 | IsTurning
 27 | GetLineOfSight
 32 | GetInSameCell
 35 | GetDisabled
 36 | MenuMode
 39 | GetDisease
 40 | GetVampire
 41 | GetClothingValue
 42 | SameFaction
 43 | SameRace
 44 | SameSex
 45 | GetDetected
 46 | GetDead
 47 | GetItemCount
 48 | GetGold
 49 | GetSleeping
 50 | GetTalkedToPC
 53 | GetScriptVariable
 56 | GetQuestRunning
 58 | GetStage
 59 | GetStageDone
 60 | GetFactionRankDifference
 61 | GetAlarmed
 62 | IsRaining
 63 | GetAttacked
 64 | GetIsCreature
 65 | GetLockLevel
 66 | GetShouldAttack
 67 | GetInCell
 68 | GetIsClass
 69 | GetIsRace
 70 | GetIsSex
 71 | GetInFaction
 72 | GetIsID
 73 | GetFactionRank
 74 | GetGlobalValue
 75 | IsSnowing
 76 | GetDisposition
 77 | GetRandomPercent
 79 | GetQuestVariable
 80 | GetLevel
 81 | GetArmorRating
 84 | GetDeadCount
 91 | GetIsAlerted
 99 | GetHeadingAngle
101 | IsWeaponOut
102 | IsTorchOut
103 | IsShieldOut
106 | IsFacingUp
107 | GetKnockedState
108 | GetWeaponAnimType
109 | IsWeaponSkillType
110 | GetCurrentAIPackage
111 | IsWaiting
112 | IsIdlePlaying
116 | GetMinorCrimeCount
117 | GetMajorCrimeCount
118 | GetActorAggroRadiusViolated
122 | GetCrime
123 | IsGreetingPlayer
125 | IsGuard
127 | HasBeenEaten
128 | GetFatiguePercentage
129 | GetPCIsClass
130 | GetPCIsRace
131 | GetPCIsSex
132 | GetPCInFaction
133 | SameFactionAsPC
134 | SameRaceAsPC
135 | SameSexAsPC
136 | GetIsReference
141 | IsTalking
142 | GetWalkSpeed
143 | GetCurrentAIProcedure
144 | GetTrespassWarningLevel
145 | IsTrespassing
146 | IsInMyOwnedCell
147 | GetWindSpeed
148 | GetCurrentWeatherPercent
149 | GetIsCurrentWeather
150 | IsContinuingPackagePCNear
153 | CanHaveFlames
154 | HasFlames
157 | GetOpenState
159 | GetSitting
160 | GetFurnitureMarkerID
161 | GetIsCurrentPackage
162 | IsCurrentFurnitureRef
163 | IsCurrentFurnitureObj
170 | GetDayOfWeek
172 | GetTalkedToPCParam
175 | IsPCSleeping
176 | IsPCAMurderer
180 | GetDetectionLevel
182 | GetEquipped
185 | IsSwimming
190 | GetAmountSoldStolen
192 | GetIgnoreCrime
193 | GetPCExpelled
195 | GetPCFactionMurder
197 | GetPCEnemyofFaction
199 | GetPCFactionAttack
203 | GetDestroyed
214 | HasMagicEffect
215 | GetDefaultOpen
219 | GetAnimAction
223 | IsSpellTarget
224 | GetVATSMode
225 | GetPersuasionNumber
226 | GetSandman
227 | GetCannibal
228 | GetIsClassDefault
229 | GetClassDefaultMatch
230 | GetInCellParam
235 | GetVatsTargetHeight
237 | GetIsGhost
242 | GetUnconscious
244 | GetRestrained
246 | GetIsUsedItem
247 | GetIsUsedItemType
254 | GetIsPlayableRace
255 | GetOffersServicesNow
258 | GetUsedItemLevel
259 | GetUsedItemActivate
264 | GetBarterGold
265 | IsTimePassing
266 | IsPleasant
267 | IsCloudy
274 | GetArmorRatingUpperBody
277 | GetBaseActorValue
278 | IsOwner
280 | IsCellOwner
282 | IsHorseStolen
285 | IsLeftUp
286 | IsSneaking
287 | IsRunning
288 | GetFriendHit
289 | IsInCombat
300 | IsInInterior
304 | IsWaterObject
306 | IsActorUsingATorch
309 | IsXBox
310 | GetInWorldspace
312 | GetPCMiscStat
313 | IsActorEvil
314 | IsActorAVictim
315 | GetTotalPersuasionNumber
318 | GetIdleDoneOnce
320 | GetNoRumors
323 | WhichServiceMenu
327 | IsRidingHorse
332 | IsInDangerousWater
338 | GetIgnoreFriendlyHits
339 | IsPlayersLastRiddenHorse
353 | IsActor
354 | IsEssential
358 | IsPlayerMovingIntoNewSpace
361 | GetTimeDead
362 | GetPlayerHasLastRiddenHorse
365 | IsChild
367 | GetLastPlayerAction
368 | IsPlayerActionActive
370 | IsTalkingActivatorActor
372 | IsInList
382 | GetHasNote
391 | GetHitLocation
392 | IsPC1stPerson
397 | GetCauseofDeath
398 | IsLimbGone
399 | IsWeaponInList
403 | HasFriendDisposition
408 | GetVATSValue
409 | IsKiller
410 | IsKillerObject
411 | GetFactionCombatReaction
415 | Exists
416 | GetGroupMemberCount
417 | GetGroupTargetCount
427 | GetIsVoiceType
428 | GetPlantedExplosive
430 | IsActorTalkingThroughActivator
431 | GetHealthPercentage
433 | GetIsObjectType
435 | GetDialogueEmotion
436 | GetDialogueEmotionValue
438 | GetIsCreatureType
446 | GetInZone
449 | HasPerk
450 | GetFactionRelation
451 | IsLastIdlePlayed
454 | GetPlayerTeammate
455 | GetPlayerTeammateCount
459 | GetActorCrimePlayerEnemy
460 | GetActorFactionPlayerEnemy
464 | IsPlayerGrabbedRef
471 | GetDestructionStage
474 | GetIsAlignment
478 | GetThreatRatio
480 | GetIsUsedItemEquipType
489 | GetConcussed
492 | GetMapMarkerVisible
495 | GetPermanentActorValue
496 | GetKillingBlowLimb
500 | GetWeaponHealthPerc
503 | GetRadiationLevel
510 | GetLastHitCritical
515 | IsCombatTarget
518 | GetVATSRightAreaFree
519 | GetVATSLeftAreaFree
520 | GetVATSBackAreaFree
521 | GetVATSFrontAreaFree
522 | GetIsLockBroken
523 | IsPS3
524 | IsWin32
525 | GetVATSRightTargetVisible
526 | GetVATSLeftTargetVisible
527 | GetVATSBackTargetVisible
528 | GetVATSFrontTargetVisible
531 | IsInCriticalStage
533 | GetXPForNextLevel
546 | GetQuestCompleted
550 | IsGoreDisabled
555 | GetSpellUsageNum
557 | GetActorsInHigh
558 | HasLoaded3D

### Parameters

The parameters can be any of the following.

Valid For Parameter | Name | Type | Info
--------------------|------|------|-----
Both | Unknown | uint8[4] |
Both | None | uint8[4] |
Both | Integer | int32 |
2 | Variable Name | int32 | 
Both | Sex | uint32 | Enum - see values below.
Both | [Actor Value](../Values/Actor Values.md) | int32 |
Both | Crime Type | uint32 | Enum - see values below.
Both | Axis | uint32 | Enum - see values below.
2 | Quest Stage | int32 | 
Both | Misc Stat | uint32 | Enum - see values below.
Both | Alignment | uint32 | Enum - see values below.
Both | Equipment Type | uint32 | Enum - see [ETYP](ETYP.md) for values.
Both | Form Type | uint32 | Enum - see values below.
Both | Critical Stage | uint32 | Enum - see values below.
Both | Object Reference | formid | FormID of a [PLYR](../PLYR.md), [REFR](../REFR.md), [ACHR](../ACHR.md), [ACRE](../ACRE.md), [PGRE](../PGRE.md), [PMIS](../PMIS.md) or [TRGT](../TRGT.md) record.
Both | Inventory Object | formid | FormID of a [ARMO](../ARMO.md), [BOOK](../BOOK.md), [MISC](../MISC.md), [WEAP](../WEAP.md), [AMMO](../AMMO.md), [KEYM](../KEYM.md), [ALCH](../ALCH.md), [NOTE](../NOTE.md), [FLST](../FLST.md), [CHIP](../CHIP.md), [CMNY](../CMNY.md) or [IMOD](../IMOD.md) record.
Both | Actor | formid | FormID of a [PLYR](../PLYR.md), [ACHR](../ACHR.md), [ACRE](../ACRE.md) or [TRGT](../TRGT.md) record.
Both | Voice Type | formid | FormID of a [VTYP](../VTYP.md) record.
Both | Idle | formid | FormID of a [IDLE](../IDLE.md) record.
Both | Form List | formid | FormID of a [FLST](../FLST.md) record.
Both | Note | formid | FormID of a [NOTE](../NOTE.md) record.
Both | Quest | formid | FormID of a [QUST](../QUST.md) record.
Both | Faction | formid | FormID of a [FACT](../FACT.md) record.
Both | Weapon | formid | FormID of a [WEAP](../WEAP.md) record.
Both | Cell | formid | FormID of a [CELL](../CELL.md) record.
Both | Class | formid | FormID of a [CLAS](../CLAS.md) record.
Both | Race | formid | FormID of a [RACE](../RACE.md) record.
Both | Actor Base | formid | FormID of a [NPC_](../NPC_.md), [CREA](../CREA.md), [ACTI](../ACTI.md) or [TACT](../TACT.md) record.
Both | Global | formid | FormID of a [GLOB](../GLOB.md) record.
Both | Weather | formid | FormID of a [WTHR](../WTHR.md) record.
Both | Package | formid | FormID of a [PACK](../PACK.md) record.
Both | Encounter Zone | formid | FormID of a [ECZN](../ECZN.md) record.
Both | Perk | formid | FormID of a [PERK](../PERK.md) record.
Both | Owner | formid | FormID of a [FACT](../FACT.md) or [NPC_](../NPC_.md) record.
Both | Furniture | formid | FormID of a [FURN](../FURN.md) or [FLST](../FLST.md) record.
Both | Effect Item | formid | FormID of a [SPEL](../SPEL.md), [ENCH](../ENCH.md), [ALCH](../ALCH.md) or [INGR](../INGR.md) record.
Both | Base Effect | formid | FormID of a [MGEF](../MGEF.md) record.
Both | Worldspace | formid | FormID of a [WRLD](../WRLD.md) record.
1 | VATS Value Function | uint32 | Enum - see values below.
2 | VATS Value Param | uint32 | 
Both | Creature Type | uint32 | Enum - see values below.
Both | Menu Mode | uint32 | Enum - see values below.
Both | Player Action | uint32 | Enum - see values below.
Both | Body Location | int32 | Enum - see values below.
Both | Referenceable Object | formid | FormID of a [CREA](../CREA.md), [NPC_](../NPC_.md), [PROJ](../PROJ.md), [TREE](../TREE.md), [SOUN](../SOUN.md), [ACTI](../ACTI.md), [DOOR](../DOOR.md), [STAT](../STAT.md), [FURN](../FURN.md), [CONT](../CONT.md), [ARMO](../ARMO.md), [AMMO](../AMMO.md), [MISC](../MISC.md), [WEAP](../WEAP.md), [BOOK](../BOOK.md), [KEYM](../KEYM.md), [ALCH](../ALCH.md), [LIGH](../LIGH.md), [GRAS](../GRAS.md), [ASPC](../ASPC.md), [IDLM](../IDLM.md), [ARMA](../ARMA.md), [MSTT](../MSTT.md), [NOTE](../NOTE.md), [PWAT](../PWAT.md), [SCOL](../SCOL.md), [TACT](../TACT.md), [TERM](../TERM.md), [FLST](../FLST.md), [CHIP](../CHIP.md), [CMNY](../CMNY.md), [CCRD](../CCRD.md) or [IMOD](../IMOD.md) record.
2 | Quest Objective | int32 | 
Both | Reputation | formid | FormID of a [REPU](../REPU.md) record.
Both | Region | formid | FormID of a [REGN](../REGN.md) record.
Both | Challenge | formid | FormID of a [CHAL](../CHAL.md) record.
Both | Casino | formid | FormID of a [CSNO](../CSNO.md) record.

#### Parameter Values

##### Sex Values

Value | Meaning
------|--------
0 | Male
1 | Female

##### Crime Type Values

Value | Meaning
------|--------
-1 | None
0 | Steal
1 | Pickpocket
2 | Trespass
3 | Attack
4 | Murder

##### Axis Values

Value | Meaning
------|--------
88 | X
89 | Y
90 | Z

##### Misc Stat Values

Value | Meaning
------|--------
0 | Quests Completed
1 | Locations Discovered
2 | People Killed
3 | Creatures Killed
4 | Locks Picked
5 | Computers Hacked
6 | Stimpaks Taken
7 | Rad-X Taken
8 | RadAway Taken
9 | Chems Taken
10 | Times Addicted
11 | Mines Disarmed
12 | Speech Successes
13 | Pockets Picked
14 | Pants Exploded
15 | Books Read
16 | Bobbleheads Found
17 | Weapons Created
18 | People Mezzed
19 | Captives Rescued
20 | Sandman Kills
21 | Paralyzing Punches
22 | Robots Disabled
23 | Contracts Completed
24 | Corpses Eaten
25 | Mysterious Stranger Visits

##### Alignment Values

Value | Meaning
------|--------
0 | Good
1 | Neutral
2 | Evil
3 | Very Good
4 | Very Evil

##### Form Type Values

Value | Meaning
------|--------
0x04 | Texture Set
0x05 | Menu Icon
0x06 | Global
0x07 | Class
0x08 | Faction
0x09 | Head Part
0x0A | Hair
0x0B | Eyes
0x0C | Race
0x0D | Sound
0x0E | Acoustic Space
0x0F | Skill
0x10 | Base Effect
0x11 | Script
0x12 | Landscape Texture
0x13 | Object Effect
0x14 | Actor Effect
0x15 | Activator
0x16 | Talking Activator
0x17 | Terminal
0x18 | Armor
0x19 | Book
0x1A | Clothing
0x1B | Container
0x1C | Door
0x1D | Ingredient
0x1E | Light
0x1F | Misc
0x20 | Static
0x21 | Static Collection
0x22 | Movable Static
0x23 | Placeable Water
0x24 | Grass
0x25 | Tree
0x26 | Flora
0x27 | Furniture
0x28 | Weapon
0x29 | Ammo
0x2A | NPC
0x2B | Creature
0x2C | Leveled Creature
0x2D | Leveled NPC
0x2E | Key
0x2F | Ingestible
0x30 | Idle Marker
0x31 | Note
0x32 | Constructible Object
0x33 | Projectile
0x34 | Leveled Item
0x35 | Weather
0x36 | Climate
0x37 | Region
0x39 | Cell
0x3A | Placed Object
0x3B | Placed Character
0x3C | Placed Creature
0x3E | Placed Grenade
0x41 | Worldspace
0x42 | Landscape
0x43 | Navigation Mesh
0x45 | Dialog Topic
0x46 | Dialog Response
0x47 | Quest
0x48 | Idle Animation
0x49 | Package
0x4A | Combat Style
0x4B | Load Screen
0x4C | Leveled Spell
0x4D | Animated Object
0x4E | Water
0x4F | Effect Shader
0x51 | Explosion
0x52 | Debris
0x53 | Image Space
0x54 | Image Space Modifier
0x55 | FormID List
0x56 | Perk
0x57 | Body Part Data
0x58 | Addon Node
0x59 | Actor Value Info
0x5A | Radiation Stage
0x5B | Camera Shot
0x5C | Camera Path
0x5D | Voice Type
0x5E | Impact Data
0x5F | Impact DataSet
0x60 | Armor Addon
0x61 | Encounter Zone
0x62 | Message
0x63 | Ragdoll
0x64 | Default Object Manager
0x65 | Lighting Template
0x66 | Music Type

##### Critical Stage Values

Value | Meaning
------|--------
0 | None
1 | Goo Start
2 | Goo End
3 | Disintegrate Start
4 | Disintegrate End

##### VATS Value Function & Param Values

Function Value | Function Meaning | Param Type | Param Info
---------------|------------------|------------|-----------
0 | Weapon Is | formid | FormID of a [WEAP](../WEAP.md) record.
1 | Weapon In List | formid | FormID of a [FLST](../FLST.md) record referencing [WEAP](../WEAP.md) records.
2 | Target Is | formid | FormID of a [CREA](../CREA.md) or [NPC_](../NPC_.md) record.
3 | Target In List | formid | FormID of a [FLST](../FLST.md) record referencing [CREA](../CREA.md) or [NPC_](../NPC_.md) records.
4 | Target Distance | uint8[4] | Unused
5 | Target Part | int32 | See [here](../Values/Actor Values.md) for values.
6 | VATS Action | uint32 | See values below.
7 | Is Success | uint8[4] | Unused
8 | Is Critical | uint8[4] | Unused
9 | Critical Effect Is | formid | FormID of a [SPEL](../SPEL.md) record.
10 | Critical Effect In List | formid | FormID of a [FLST](../FLST.md) record referencing [SPEL](../SPEL.md) records.
11 | Is Fatal | uint8[4] | Unused
12 | Explode Part | uint8[4] | Unused
13 | Dismember Part | uint8[4] | Unused
14 | Cripple Part | uint8[4] | Unused
15 | Weapon Type Is | uint32 | See [here](../Values/Weapon Animation Types.md) for values.
16 | Is Stranger | uint8[4] | Unused
17 | Is Paralyzing Palm | uint8[4] | Unused

###### VATS Action Param Values

Value | Meaning
------|--------
0 | Unarmed Attack
1 | One Hand Melee Attack
2 | Two Hand Melee Attack
3 | Fire Pistol
4 | Fire Rifle
5 | Fire Handle Weapon
6 | Fire Launcher
7 | Throw Grenade
8 | Place Mine
9 | Reload
10 | Crouch
11 | Stand
12 | Switch Weapon
13 | Toggle Weapon Drawn
14 | Heal
15 | Player Death
16 | Special Weapon Attack
17 | Special Unarmed Attack
18 | Kill Camera Shot
19 | Throw Weapon

##### Creature Type Values

Value | Meaning
------|--------
0 | Animal
1 | Mutated Animal
2 | Mutated Insect
3 | Abomination
4 | Super Mutant
5 | Feral Ghoul
6 | Robot
7 | Giant

##### Menu Mode Values

Value | Meaning
------|--------
1 | Type: Character Interface
2 | Type: Other
3 | Type: Console
1001 | Specific: Message
1002 | Specific: Inventory
1003 | Specific: Stats
1004 | Specific: HUDMainMenu
1007 | Specific: Loading
1008 | Specific: Container
1009 | Specific: Dialog
1012 | Specific: Sleep/Wait
1013 | Specific: Pause
1014 | Specific: LockPick
1016 | Specific: Quantity
1027 | Specific: Level Up
1035 | Specific: Pipboy Repair
1036 | Specific: Race / Sex
1047 | Specific: Credits
1048 | Specific: CharGen
1051 | Specific: TextEdit
1053 | Specific: Barter
1054 | Specific: Surgery
1055 | Specific: Hacking
1056 | Specific: VATS
1057 | Specific: Computers
1058 | Specific: Vendor Repair
1059 | Specific: Tutorial
1060 | Specific: You're SPECIAL book

##### Player Action Values

Value | Meaning
------|--------
0 | ??
1 | Swinging Melee Weapon
2 | Throwing Grenade
3 | Fire Weapon
4 | Lay Mine
5 | Z Key Object
6 | Jumping
7 | Knocking Over Objectss
8 | Stand on Table / Chair
9 | Iron Sights
10 | Destroying Object

##### Body Location Values

Value | Meaning
------|--------
-1 | None
0 | Torso
1 | Head 1
2 | Head 2
3 | Left Arm 1
4 | Left Arm 2
5 | Right Arm 1
6 | Right Arm 2
7 | Left Leg 1
8 | Left Leg 2
9 | Left Leg 3
10 | Right Leg 1
11 | Right Leg 2
12 | Right Leg 3
14 | Brain
 
### Run On Values

Value | Meaning
------|--------
0 | Subject
1 | Target
2 | Reference
3 | Combat Target
4 | Linked Reference
