ADDN Record
===========

Addon Node

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | MODL | Model Filename | cstring | Model data
- | MODB | Unknown | uint8[4] | Model data
- | MODT | Texture File Hashes | ?? | Model data
- | [MODS](Fields/MODS.md) | Alternate Textures | struct | Model data
- | [MODD](Fields/MODD.md) | FaceGen Model Flags | uint8 | Model data
+ | DATA | Node Index | int32 |
+ | DNAM | Data | struct |

### DNAM

Count | Name | Type | Info
------|------|------|-----
- | Master Particle System Cap | uint16 |
- | unknown | uint8[2] |
