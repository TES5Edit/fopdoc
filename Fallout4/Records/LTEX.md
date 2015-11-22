LTEX
====

Landscape Texture

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | editorID | zstring | Faction name
 | TNAM | Texture | formid | Reference to a [[Tes5Mod:Mod_File_Format/TXST|TXST]]. ''only 1 without this, LScrub01''
 | MNAM | Material | formid | Reference to a [[Tes5Mod:Mod_File_Format/MATT|MATT]].
 | HNAM | | ubyte[2] | Havok Data
 | SNAM | | ubyte | Texture Specular Exponent ''always 0x1E (30)''
 | GNAM | Grass |  formid | Not required.  Possible Grass.
 
 ** Existing Data Below Subject to change Copied from previous UESP **

### HNAM

Name | Info
-----|-----
Friction | 
Restitution |