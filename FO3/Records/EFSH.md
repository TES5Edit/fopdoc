EFSH
====

Effect Shader

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | ICON | Fill Texture | cstring |
 | ICO2 | Particle Shader Texture | cstring |
 | NAM7 | Holes Texture | cstring |
+ | DATA | Data | struct
 
### DATA

Name | Type | Info
-----|------|-----
Flags | uint8 |
Unused | byte[3] |
Membrane Shader - Source Blend Mode | uint32 | See below for blend mode values.
Membrane Shader - Blend Operation | uint32 | See below for blend operation values.
Membrane Shader - Z Test Function | uint32 | See below for Z test function values.
Fill/Texture Effect - Color | rgba |
Fill/Texture Effect - Alpha Fade In Time | float32 |
Fill/Texture Effect - Full Alpha Time | float32 |
Fill/Texture Effect - Alpha Fade Out Time | float32 |
Fill/Texture Effect - Presistent Alpha Ratio | float32 |
Fill/Texture Effect - Alpha Pulse Amplitude | float32 |
Fill/Texture Effect - Alpha Pulse Frequency | float32 |
Fill/Texture Effect - Texture Animation Speed (U) | float32 |
Fill/Texture Effect - Texture Animation Speed (V) | float32 |
Edge Effect - Fall Off | float32 |
Edge Effect - Color | rgba |
Edge Effect - Alpha Fade In Time | float32 |
Edge Effect - Full Alpha Time | float32 |
Edge Effect - Alpha Fade Out Time | float32 |
Edge Effect - Persistent Alpha Ratio | float32 |
Edge Effect - Alpha Pulse Amplitude | float32 |
Edge Effect - Alpha Pulse Frequence | float32 |
Edge Effect - Fill/Texture Effect - Full Alpha Ratio | float32 |
Edge Effect - Full Alpha Ratio | float32 |
Membrane Shader - Dest Blend Mode | uint32 | See below for blend mode values.
Particle Shader - Source Blend Mode | uint32 | See below for blend mode values.
Particle Shader - Blend Operation | uint32 | See below for blend operation values.
Particle Shader - Z Test Function | uint32 | See below for Z test function values.
Particle Shader - Dest Blend Mode | uint32 | See below for blend mode values.
Particle Shader - Particle Birth Ramp Up Time | float32 |
Particle Shader - Full Particle Birth Time | float32 |
Particle Shader - Particle Birth Ramp Down Time | float32 |
Particle Shader - Full Particle Birth Ratio | float32 |
Particle Shader - Persistant Particle Birth Ratio | float32 |
Particle Shader - Particle Lifetime | float32 |
Particle Shader - Particle Lifetime +/- | float32 |
Particle Shader - Initial Speed Along Normal | float32 |
Particle Shader - Acceleration Along Normal | float32 |
Particle Shader - Initial Velocity #1 | float32 |
Particle Shader - Initial Velocity #2 | float32 |
Particle Shader - Initial Velocity #3 | float32 |
Particle Shader - Acceleration #1 | float32 |
Particle Shader - Acceleration #2 | float32 |
Particle Shader - Acceleration #3 | float32 |
Particle Shader - Scale Key 1 | float32 |
Particle Shader - Scale Key 2 | float32 |
Particle Shader - Scale Key 1 Time | float32 |
Particle Shader - Scale Key 2 Time | float32 |
Particle Shader - Color Key 1 - Color | rgba |
Particle Shader - Color Key 2 - Color | rgba |
Particle Shader - Color Key 3 - Color | rgba |
Color Key 1 - Color Alpha | float32 |
Color Key 2 - Color Alpha | float32 |
Color Key 3 - Color Alpha | float32 |
Color Key 1 - Color Key Time | float32 |
Color Key 2 - Color Key Time | float32 |
Color Key 3 - Color Key Time | float32 |
Particle Shader - Initial Speed Along Normal +/- | float32 |
Particle Shader - Initial Rotation (deg) | float32 |
Particle Shader - Initial Rotation (deg) +/- | float32 |
Particle Shader - Rotation Speed (deg/sec) | float32 |
Particle Shader - Rotation Speed (deg/sec) +/- | float32 |
Addon Models | formid | FormID of a [DEBR](DEBR.md) record, or null.
Holes - Start Time | float32 |
Holes - End Time | float32 |
Holes - Start Value | float32 |
Holes - End Value | float32 |
Edge Width (alpha units) | float32 |
Edge Color | rgba |
Explosion Wind Speed | float32 |
Texture Count U | uint32 |
Texture Count V | uint32 |
Addon Models - Fade In Time | float32 |
Addon Models - Fade Out Time | float32 |
Addon Models - Scale Start | float32 |
Addon Models - Scale End | float32 |
Addon Models - Scale In Time | float32 |
Addon Models - Scale Out Time | float32 |
 
 
#### Flag Values

Value | Meaning
------|--------
0x01 | No Membrane Shader
0x02 | ??
0x04 | ??
0x08 | No Particle Shader
0x10 | Edge Effect - Inverse
0x20 | Membrane Shader - Affect Skin Only

#### Blend Mode Values

Value | Meaning
------|--------
0 | ??
1 | Zero
2 | One
3 | Source Color
4 | Source Inverse Color
5 | Source Alpha
6 | Source Inerted Alpha
7 | Destination Alpha
8 | Destination Inverted Alpha
9 | Destination Color
10 | Destimation Inverse Color
11 | Source Alpha SAT

#### Blend Operation Values

Value | Meaning
------|--------
0 | ??
1 | Add
2 | Subtract
3 | Reverse Subtract
4 | Minimum
5 | Maximum

#### Z Test Function Value

Value | Meaning
------|--------
0 | ??
1 | ??
2 | ??
3 | Equal To
4 | Normal
5 | Greater Than
6 | ??
7 | Greater Than or Equal Than
8 | Always Show
