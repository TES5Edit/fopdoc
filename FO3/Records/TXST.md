TXST Record
===========

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | Editor ID
- | [OBND](Fields/OBND.md) | Object Bounds | struct | 
- | TX00 | texture00 | zstring | texture path, base Image / transparency
- | TX01 | texture01 | zstring | texture path, normal map (tangent- or model-space)
- | TX02 | texture02 | zstring | texture path, mask (environment or light)
- | TX03 | texture03 | zstring | texture path, tone map (for skins) or glow map (for things)
- | TX04 | texture04 | zstring | texture path, detail map (parallax, roughness, complexion, age)
- | TX05 | texture05 | zstring | texture path, environment map (cubemaps mostly)
- | DODT | Decal Data | struct | 
- | DNAM | Flags | uint16 | See Notes

### DODT

Name | Type | Info
------|------|-----
Min Width | float32 | 
Max Width | float32 | 
Min Height | float32 | 
Max Height | float32 | 
Depth | float32 | 
Shininess | float32 | 
Parallax | struct | 
 | float32 | Scale
 | uint8 | Passes
Flags | uint8 | See below
Unused | uint16 |
Color | rgba | 

Flag | Meaning
-----|--------
0x00000001 | Parallax
0x00000002 | Alpha - Blending
0x00000004 | Alpha - Testing

### DNAM

Flag | Meaning
-----|--------
0x00000001 | No Specular Map
