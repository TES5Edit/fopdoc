CLMT
====

Climate

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
-* | WLST | Weather Type | struct | 
 | FNAM | Sun Texture | cstring |
 | GNAM | Sun Glare Texture | cstring |
- | | [Model Data](Fields/Model.md) | | This is a field collection.
+ | TNAM | Timing | struct |


### WLST

Count | Name | Type | Info
------|------|------|-----
 | Weather | formid | FormID of a [WTHR](WTHR.md) record, or null.
 | Chance | int32 | 
 | Global | formid | FormID of a [GLOB](GLOB.md) record, or null.

### TNAM

Count | Name | Type | Info
------|------|------|-----
 | Sunrise Begin | uint8 | 
 | Sunrise End | uint8 |
 | Sunset Begin | uint8 |
 | Sunset End | uint8 |
 | Volatility | uint8 |
 | Moons / Phase Length | uint8 |
 
