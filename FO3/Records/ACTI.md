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
- | | Destruction Data | | This is a complex arrangement of fields, see below for details
- | SNAM | Sound - Looping | formid | FormID of a SOUN record.
- | VNAM | Sound - Activation | formid | FormID of a SOUN record.
- | RNAM | Radio Station | formid | FormID of a TACT record.
- | WNAM | Water Type | formid | FormID of a WATR record.

### OBND

Count | Name | Type | Info
------|------|------|-----
- | X | int16 |
- | Y | int16 |
- | Z | int16 |

### MODS

Count | Name | Type | Info
------|------|------|-----
+ | Count | uint32 | Number of alternate textures.
-* | Alternate Texture | struct | A sub-field structure detailed immediately below.

#### Aternate Texture

Count | Name | Type | Info
------|------|------|-----
- | Name Length | uint32 | Alternate texture data. Length of the following 3D name.
- | 3D Name | char[Name Length] | Alternate texture data. 
- | New Texture | formid | Alternate texture data. FormID of a TXST record.
- | 3D Index | int32 | Alternate texture data. 

### Destruction Data


Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | DEST | Header | struct | 
-* | DSTD | Stage Data | struct | 
-* | DMDL | Stage Model Filename | cstring |
-* | DMDT | Stage Model Texture Files Hashes | ?? | ??

The stage fields form a repeated block, rather than the individual fields being repeated.

#### DEST

Count | Name | Type | Info
------|------|------|-----
+ | Health | int32 |
+ | Count | uint8 |
+ | Flags | uint8 |
+ | unknown | uint8[2] | ??

#### DSTD

Count | Name | Type | Info
------|------|------|-----
+ | Health Percentage | int32 | 
+ | Index | uint8 |
+ | Damage Stage | uint8 |
+ | Flags | uint8 |
+ | Self Damage per Second | int32 |
+ | Explosion | formid | FormID of a EXPL record or null.
+ | Debris | formid | FormID of a DEBR record or null.
+ | Debris Count | int32 | 

