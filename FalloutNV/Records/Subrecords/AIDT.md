---
layout: falloutnvrec
title: fopdoc
---
AIDT Subrecord
==========

As used in the [CREA](../CREA.md) and [NPC_](../NPC_.md) record types.

## Format

Name | Type | Info
-----|------|-----
Aggression | uint8 | Enum - see below for values.
Confidence | uint8 | Enum - see below for values.
Energy Level | uint8 |
Responsibility | uint8 |
Mood | uint8 | Enum - see below for values.
Unused | byte[3] |
[Buys/Sells and Services](../Values/Services.md) | uint32 | Flags - see link for values.
[Teaches](../Values/Skills.md) | int8 | Enum - see link for values.
Maximum Training Level | uint8 | 
Assistance | int8 | Enum - see below for values.
Aggro Radius Behaviour | uint8 | Flags - see below for values.
Aggro Radius | int32 |
 
 
### Aggression Enum Values

Value | Meaning
------|--------
0 | Unaggressive
1 | Aggressive
2 | Very Aggressive
3 | Frenzied
 
### Confidence Enum Values

Value | Meaning
------|--------
0 | Cowardly
1 | Cautious
2 | Average
3 | Brave
4 | Foolhardy

### Mood Enum Values

Value | Meaning
------|--------
0 | Neutral 
1 | Afraid
2 | Annoyed
3 | Cocky
4 | Drugged
5 | Pleasant
6 | Angry
7 | Sad

### Assistance Enum Values

Value | Meaning
------|--------
0 | Helps Nobody
1 | Helps Allies
2 | Helps Friends and Allies

### Aggro Radius Behavior Flag Values

Value | Meaning
------|--------
0x01 | Aggro Radius Behavior
