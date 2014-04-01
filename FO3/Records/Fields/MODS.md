MODS Field
==========

As used in the [ACTI](../ACTI.md) and [ADDN](../ADDN.md) record types.

## Format

Count | Name | Type | Info
------|------|------|-----
+ | Count | uint32 | Number of alternate textures.
-* | Alternate Texture | struct | A sub-field structure detailed below.

### Aternate Texture

Count | Name | Type | Info
------|------|------|-----
- | Name Length | uint32 | Alternate texture data. Length of the following 3D name.
- | 3D Name | char[Name Length] | Alternate texture data.
- | New Texture | formid | Alternate texture data. FormID of a TXST record.
- | 3D Index | int32 | Alternate texture data.