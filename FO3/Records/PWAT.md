PWAT
====

Placeable Water

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | | [Model Data](Fields/Model.md) | | This is a field collection.
+ | DNAM | | struct
 
### DNAM

Name | Type | Info
-----|------|-----
Flags | uint32 | See below for values.
Water | formid | FormID of a [WATR](WATR.md) record.

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Reflects
0x00000002 | Reflects - Actors
0x00000004 | Reflects - Land
0x00000008 | Reflects - LOD Land
0x00000010 | Reflects - LOD Buildings
0x00000020 | Reflects - Trees
0x00000040 | Reflects - Sky
0x00000080 | Reflects - Dynamic Objects
0x00000100 | Reflects - Dead Bodies
0x00000200 | Refracts
0x00000400 | Refracts - Actors
0x00000800 | Refracts - Land
0x00001000 | ??
0x00002000 | ??
0x00004000 | ??
0x00008000 | ??
0x00010000 | Refracts - Dynamic Objects
0x00020000 | Refracts - Dead Bodies
0x00040000 | Silhouette Reflections
0x00080000 | ??
0x00100000 | ??
0x00200000 | ??
0x00400000 | ??
0x00800000 | ??
0x01000000 | ??
0x02000000 | ??
0x03000000 | ??
0x08000000 | ??
0x10000000 | Depth
0x20000000 | Object Texture Coordinates
0x40000000 | ??
0x80000000 | No Underwater Fog
