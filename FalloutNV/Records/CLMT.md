CLMT
====

Climate

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
-* | WLST | Weather Type | struct | 
 | FNAM | Sun Texture | cstring |
 | GNAM | Sun Glare Texture | cstring |
- | | [Model Data](Subrecords/Model.md) | collection |
+ | TNAM | Timing | struct |


### WLST

Name | Type | Info
-----|------|-----
Weather | formid | FormID of a [WTHR](WTHR.md) record, or null.
Chance | int32 | 
Global | formid | FormID of a [GLOB](GLOB.md) record, or null.

### TNAM

Name | Type | Info
-----|------|-----
Sunrise Begin | uint8 | 
Sunrise End | uint8 |
Sunset Begin | uint8 |
Sunset End | uint8 |
Volatility | uint8 |
Moons / Phase Length | uint8 |
 

