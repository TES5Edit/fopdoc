---
layout: fallout3rec
title: fopdoc
---
Model Subrecord Collection
==========================

The MODL, MODB, MODT, MODS and MODD subrecords hold model data, and always appear together. In cases where multiple collections are present in the same record, the subrecord codes are numbered:

Original | Second Instance | Third Instance | Fourth Instance
---------|-----------------|----------------|----------------
MODL | MOD2 | MOD3 | MOD4
MODB | (always missing) | (always missing) | (always missing)
MODT | MO2T | MO3T | MO4T
MODS | MO2S | MO3S | MO4S
MODD | (always missing) | MOSD | (always missing)

Whenever a model subrecord collection is referenced in these docs, assume it is the first instance unless a number is given. If so, substitute the appropriate subrecord codes as shown above.

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | MODL | Model Filename | cstring |
- | MODB | Unknown | byte[4] |
- | [MODT](Subrecords/MODT.md) | Texture Filename Hashes | struct[] |
- | MODS | Alternate Textures | struct | See below for details.
- | MODD | FaceGen Model Flags | uint8 | See below for flag values.

### MODS Subrecord

Count | Name | Type | Info
------|------|------|-----
+ | Count | uint32 | Number of alternate textures.
-* | Alternate Texture Data | struct | See below for details.

#### Alternate Texture Data

Name | Type | Info
-----|------|-----
Name Length | uint32 | Length of the following 3D name.
3D Name | char[Name Length] |
New Texture | formid | FormID of a [TXST](../TXST.md) record.
3D Index | int32 |

### MODD Flag Values

Value | Meaning
------|--------
0x01 | Head
0x02 | Torso
0x04 | Right Hand
0x08 | Left Hand
