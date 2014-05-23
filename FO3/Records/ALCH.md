ALCH Record
===========

Ingestible

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | FULL | Name | cstring |
 | | [Model Data](Fields/Model.md) | | This is a field collection.
 | ICON | Large Icon Filename | cstring | 
 | MICO | Small Icon FIlename | cstring |
 | SCRI | Script | formid | FormID of a SCPT record.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | YNAM | Sound - Pick Up | formid | FormID of a [SOUN](SOUN.md) record.
 | ZNAM | Sound - Drop | formid | FormID of a [SOUN](SOUN.md) record.
+ | [ETYP](#etyp-enum-values) | Equipment Type | int32 |
+ | DATA | Weight | float32 |
+ | [ENIT](#enit) | Effect Data | struct |
+* | EFID | Base Effect | formid | FormID of a [MGEF](MGEF.md) record.
+* | [EFIT](#efit) | Effect Data | struct |
+* | CTDA | Condition | struct |
 
### ETYP Enum Values

Value | Meaning
------|--------
-1 | None
0 | Big Guns
1 | Energy Weapons
2 | Small Guns
3 | Melee Weapons
4 | Unarmed Weapon
5 | Thrown Weapons
6 | Mine
7 | Body Wear
8 | Head Wear
9 | Hand Wear
10 | Chems
11 | Stimpack
12 | Food
13 | Alcohol

### ENIT

Count | Name | Type | Info
------|------|------|-----
 | Value | int32 |
 | Flags | uint8 | See below for flags.
 | Unused | uint8[3] | ??
 | Withdrawal Effect | formid | FormID of a [SPEL](SPEL.md) record, or null.
 | Addiction Chance | float32 |
 | Sound - Consume | formid | FormID of a [SOUN](SOUN.md) record.

#### Flag Values

Flag | Meaning
-----|--------
0x00000001 | No Auto-Calc (Unused)
0x00000002 | Food Item
0x00000004 | Medicine

### EFIT

Count | Name | Type | Info
------|------|------|-----
 | Magnitude | uint32 | 
 | Area | uint32 |
 | Duration | uint32 |
 | Type | uint32 | See below for values.
 | Actor Value | int32 | See below for values.
 
#### Type Enum Values

Value | Meaning
------|--------
0 | Self
1 | Touch
2 | Target
 
#### Actor Values

Value | Meaning
------|--------
0 | Aggression
1 | Confidence
2 | Energy
3 | Responsibility
4 | Mood
5 | Strength
6 | Perception
7 | Endurance
8 | Charisma
9 | Intelligence
10 | Agility
11 | Luck
12 | Action Points
13 | Carry Weight
14 | Critical Chance
15 | Heal Rate
16 | Health
17 | Melee Damage
18 | Damage Resistance
19 | Poison Resistance
20 | Rad Resistance
21 | Speed Multiplier
22 | Fatigue
23 | Karma
24 | XP
25 | Perception Condition
26 | Endurance Condition
27 | Left Attack Condition
28 | Right Attack Condition
29 | Left Mobility Condition
30 | Right Mobility Condition
31 | Brain Condition
32 | Barter
33 | Big Guns
34 | Energy Weapons
35 | Explosives
36 | Lockpick
37 | Medicine
38 | Melee Weapons
39 | Repair
40 | Science
41 | Small Guns
42 | Sneak
43 | Speech
44 | Throwing (unused)
45 | Unarmed
46 | Inventory Weight
47 | Paralysis
48 | Invisibility
49 | Chameleon
50 | Night Eye
51 | Detect Life Range
52 | Fire Resistance
53 | Water Breathing
54 | Rad Level
55 | Bloody Mess
56 | Unarmed Damage
57 | Assistance
58 | Electric Resistance
59 | Frost Resistance
60 | Energy Resistance
61 | EMP Resistance
62 | ??
63 | ??
64 | ??
65 | ??
66 | ??
67 | ??
68 | ??
69 | ??
70 | ??
71 | ??
72 | Ignore Negative Effects

### CTDA

Count | Name | Type | Info
------|------|------|-----
 | Type | uint8 |
 | Unused | uint8[3] |
 | Comparison Value | formid *or* float32 | If not a valid [GLOB](GLOB.md) record FormID, is interpreted as a float32.
 | Function | uint32 | A function index. See below for a list of function indicies.
 | Parameter #1 | uint8[4] | First parameter to pass to the function. 
 | Parameter #2 | uint8[4] | Second parameter to pass to the function.
 | Run On | uint32 | Values and what they correspond to are given below.
 | Reference | formid | A FormID of a [PLYR](PLYR.md), [ACHR](ACHR.md), [ACRE](ACRE.md), [REFR](REFR.md), [PMIS](PMIS.md) or [PGRE](PGRE.md) reference on which to apply the function, or null.
 
#### Function Indicies

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
 
#### Run On Values

Value | Meaning
------|--------
0 | Subject
1 | Target
2 | Reference
3 | Combat Target
4 | Linked Reference
