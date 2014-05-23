Model Field Collection
======================

The MODL, MODB, MODT, MODS and MODD fields hold model data, and always appear together.

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
