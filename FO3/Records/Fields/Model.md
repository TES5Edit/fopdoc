Model Field Collection
======================

The MODL, MODB, MODT, MODS and MODD fields hold model data, and always appear together. In cases where multiple collections are present in the same record, the field IDs are numbered, eg.

Original | Second Instance | Third Instance | Fourth Instance
---------|-----------------|----------------|----------------
MODL | MOD2 | MOD3 | MOD4
MODB | ?? | ?? | ??
MODT | MO2T | MO3T | MO4T
MODS | MO2S | MO3S | MO4S
MODD | ?? | MOSD | ??

Whenever a model field collection is referenced in these docs, the instance number will be given, so substitute the appropriate field IDs below.

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | MODL | Model Filename | cstring |
- | MODB | Unknown | uint8[4] |
- | MODT | Texture File Hashes | ?? |
- | MODS | Alternate Textures | struct | See below for details.
- | MODD | FaceGen Model Flags | uint8 | See below for flag values.

### MODS

Count | Name | Type | Info
------|------|------|-----
+ | Count | uint32 | Number of alternate textures.
-* | Alternate Texture | struct | A sub-field structure detailed below.

#### Aternate Texture

Count | Name | Type | Info
------|------|------|-----
- | Name Length | uint32 | Alternate texture data. Length of the following 3D name.
- | 3D Name | char[Name Length] | Alternate texture data.
- | New Texture | formid | Alternate texture data. FormID of a TXST record.
- | 3D Index | int32 | Alternate texture data.

### MODD Flag Values

Flag | Meaning
-----|--------
0x01 | Head
0x02 | Torso
0x04 | Right Hand
0x08 | Left Hand
