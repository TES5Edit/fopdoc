DOBJ
====

Default Object Manager

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+* | DATA | Default Object | formid | Each DATA subrecord is mapped to a different type of object. The mapping is given below.

### DATA Mapping

DATA Subrecord Index | Object Type
-----------------|------------
0 | Stimpack
1 | SuperStimpack
2 | RadX
3 | RadAway
4 | Morphine
5 | Perk Paralysis
6 | Player Faction
7 | Mysterious Stranger NPC
8 | Mysterious Stranger Faction
9 | Default Music
10 | Battle Music
11 | Death Music
12 | Success Music
13 | Level Up Music
14 | Player Voice (Male)
15 | Player Voice (Male Child)
16 | Player Voice (Female)
17 | Player Voice (Female Child)
18 | Eat Package Default Food
19 | Every Actor Ability
20 | Drug Wears Off Image Space
21 | Doctor's Bag
22 | Miss Fortune NPC
23 | Miss Fortune Faction
24 | Meltdown Explosion
25 | Unarmed Forward PA
26 | Unarmed Backward PA
27 | Unarmed Left PA
28 | Unarmed Right PA
29 | Unarmed Crouch PA
30 | Unarmed Counter PA
31 | Spotter Effect
32 | Item Detected Efect
33 | Cateye Mobile Effect (NYI)
