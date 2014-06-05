ADDN Record
===========

Addon Node

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | | [Model Data](Subrecords/Model.md) | collection |
+ | DATA | Node Index | int32 |
+ | DNAM | Data | struct |

### DNAM

Name | Type | Info
-----|------|-----
Master Particle System Cap | uint16 |
Unknown | byte[2] |
