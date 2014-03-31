ACTI Record
===========

Activator

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | OBND | Object Bounds | struct |
+ | OBND | Object Bounds | struct |
- | FULL | Name | cstring | Activator name
- | MODL | Model Filename | struct | Model data
- | MODB | Unknown | uint8[4] | Model data
- | MODT | Texture File Hashes | ?? | Model data
- | MODS | Alternate Textures | struct | Model data
- | MODD | FaceGen Model Flags | uint8 | Model data 
- | SCRI | Script | formid | FormID of a SCPT record.
- | DEST | Destruction Data | struct | 

### OBND

Count | Name | Type | Info
------|------|------|-----
- | X | int16 |
- | Y | int16 |
- | Z | int16 |

### MODS

Count | Name | Type | Info
------|------|------|-----
+ | Count | uint32 | Number of alternate textures. All following fields are present as one block that is repeated this number of times.
-* | Alternate Texture | struct | A sub-field structure detailed immediately below.

#### Aternate Texture

Count | Name | Type | Info
------|------|------|-----
- | Name Length | uint32 | Alternate texture data. Length of the following 3D name.
- | 3D Name | char[Name Length] | Alternate texture data. 
- | New Texture | formid | Alternate texture data. FormID of a TXST record.
- | 3D Index | int32 | Alternate texture data. 

### DEST
