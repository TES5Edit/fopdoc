IMGS
====

Image Space

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | DNAM |  | struct |

### DNAM

Name | Type | Info
-----|------|-----
HDR Eye Adapt Speed | float32 |
HDR Blur Radius | float32 |
HDR Blur Passes | float32 |
HDR Emissive Multiplier | float32 |
HDR Target LUM | float32 |
HDR Upper LUM Clamp | float32 |
HDR Bright Scale | float32 |
HDR Bright Clamp | float32 |
HDR LUM Ramp No Tex | float32 |
HDR LUM Ramp Min | float32 |
HDR Lum Ramp Max | float32 |
HDR Sunlight Dimmer | float32 |
HDR Grass Dimmer | float32 |
HDR Tree Dimmer | float32 |
HDR Skin Dimmer | float32 |
Bloom Blur Radius | float32 |
Bloom Alpha Mult Interior | float32 |
Bloom Alpha Mult Exterior | float32 |
Get Hit Blur Radius | float32 |
Get Hit Blur Damping Constant | float32 |
Get Hit Damping Constant | float32 |
Night Eye Tint Color | rgb |
Brightness | float32 |
Cinematic Saturation | float32 |
Cinematic Contrast Avg Lum Value | float32 |
Cinematic Contrast Value | float32 |
Cinematic Brightness Tint Color | rgb |
Cinmatic Brightness Tint Value | float32 |
Unused | uint8[16] |
Flags | uint8 | See below for values.
Unused | uint8[3] |
 
The `rgb` data types above are apparently float32 triplets, with the first being for red, the second for green and the third for blue.
 
#### Flag Values

Value | Meaning
------|--------
0x01 | Saturation
0x02 | Contrast
0x04 | Tint
0x08 | Brightness
