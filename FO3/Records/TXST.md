TXST
====

Texture Set

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | TX00 | Base Image / Transparency | cstring | The alpha channel holds the transparency data.
 | TX01 | Normal Map / Specular | cstring | The alpha channel holds the specular data.
 | TX02 | Environment Map Mask | cstring |
 | TX03 | Glow Map | cstring |
 | TX04 | Parallax Map | cstring |
 | TX05 | Enviroment Map | cstring |
 | DODT | Decal Data | struct |
+ | DNAM | Flags | uint16 | See below for values.
 
### DNAM

Count | Name | Type | Info
------|------|------|-----
 | Min Width | float32 |
 | Max Width | float32 |
 | Min Height | float32 |
 | Max Height | float32 |
 | Depth | float32 |
 | Shininess | float32 |
 | Parallax Scale | float32 |
 | Parallax Passes | uint8 |
 | Flags | uint8 | See below for values.
 | Unused | uint8[2] | 
 | Color | rgba |
 
#### Flag Values

Value | Meaning
------|--------
0x01 | Parallax
0x02 | Aplha - Blending
0x04 | Alpha - Testing

### DNAM Flag Values

Value | Meaning
------|--------
0x0001 | No Specular Map
