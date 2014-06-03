WATR
====

Water

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
+ | NNAM | Noise Map | cstring |
+ | ANAM | Opacity | uint8 | 
+ | FNAM | Flags | uint8 | See below for values.
+ | MNAM | Material ID | cstring |
 | SNAM | Sound | formid | FormID of a [SOUN](SOUN.md) record.
 | XNAM | Actor Effect | formid | FormID of a [SPEL](SPEL.md) record.
+ | DATA | Damage | uint16 |
+ | DNAM *or* DATA | Visual Data | struct |
+ | GNAM | Related Waters | struct | Unused

### Flag Values

Value | Meaning
------|--------
0x01 | Causes Damage
0x02 | Reflective

### DNAM

Name | Type | Info
-----|------|-----
Unknown | byte[16] |
Water Properties - Sun Power | float32 |
Water Properties - Reflectivity Amount | float32 |
Water Properties - Fresnel Amount | float32 |
Unused | byte[4] |
Fog Properties - Above Water - Fog Near Plane Distance | float32 |
Fog Properties - Above Water - Fog Far Plane Distance | float32 |
Shallow Color | rgba |
Deep Color | rgba |
Reflection Color | rgba |
Unused | byte[4] |
Rain Simulator - Force | float32 |
Rain Simulator - Velocity | float32 |
Rain Simulator - Falloff | float32 |
Rain Simulator - Dampener | float32 |
Displacement Simulator - Starting Size | float32 |
Displacement Simulator - Force | float32 |
Displacement Simulator - Velocity | float32 |
Displacement Simulator - Falloff | float32 |
Displacement Simulator - Dampener | float32 |
Rain Simulator - Starting Size | float32 |
Noise Properties - Normals - Noise Scale | float32 |
Noise Properties - Noise Layer One - Wind Direction | float32 |
Noise Properties - Noise Layer Two - Wind Direction | float32 |
Noise Properties - Noise Layer Three - Wind Direction | float32 |
Noise Properties - Noise Layer One - Wind Speed | float32 |
Noise Properties - Noise Layer Two - Wind Speed | float32 |
Noise Properties - Noise Layer Three - Wind Speed | float32 |
Noise Properties - Normals - Depth Falloff Start | float32 |
Noise Properties - Normals - Depth Falloff End | float32 |
Fog Properties - Above Water - Fog Amount | float32 |
Noise Properties - Normals - UV Scale | float32 |
Fog Properties - Under Water - Fog Amount | float32 |
Fog Properties - Under Water - Fog Near Plane Distance | float32 |
Fog Properties - Under Water - Fog Far Plane Distance | float32 |
Water Properties - Distortion Amount | float32 |
Water Properties - Shininess | float32 |
Water Properties - Reflection HDR Multiplier | float32 |
Water Properties - Light Radius | float32 |
Water Properties - Light Brightness | float32 |
Noise Properties - Noise Layer One - UV Scale | float32 |
Noise Properties - Noise Layer Two - UV Scale | float32 |
Noise Properties - Noise Layer Three - UV Scale | float32 |
Noise Properties - Noise Layer One - Amplitude Scale | float32 |
Noise Properties - Noise Layer Two - Amplitude Scale | float32 |
Noise Properties - Noise Layer Three - Amplitude Scale | float32 |

### DATA

Name | Type | Info
-----|------|-----
Unknown | byte[16] |
Water Properties - Sun Power | float32 |
Water Properties - Reflectivity Amount | float32 |
Water Properties - Fresnel Amount | float32 |
Unused | byte[4] |
Fog Properties - Above Water - Fog Near Plane Distance | float32 |
Fog Properties - Above Water - Fog Far Plane Distance | float32 |
Shallow Color | rgba |
Deep Color | rgba |
Reflection Color | rgba |
Unused | byte[4] |
Rain Simulator - Force | float32 |
Rain Simulator - Velocity | float32 |
Rain Simulator - Falloff | float32 |
Rain Simulator - Dampener | float32 |
Displacement Simulator - Starting Size | float32 |
Displacement Simulator - Force | float32 |
Displacement Simulator - Velocity | float32 |
Displacement Simulator - Falloff | float32 |
Displacement Simulator - Dampener | float32 |
Rain Simulator - Starting Size | float32 |
Noise Properties - Normals - Noise Scale | float32 |
Noise Properties - Noise Layer One - Wind Direction | float32 |
Noise Properties - Noise Layer Two - Wind Direction | float32 |
Noise Properties - Noise Layer Three - Wind Direction | float32 |
Noise Properties - Noise Layer One - Wind Speed | float32 |
Noise Properties - Noise Layer Two - Wind Speed | float32 |
Noise Properties - Noise Layer Three - Wind Speed | float32 |
Noise Properties - Normals - Depth Falloff Start | float32 |
Noise Properties - Normals - Depth Falloff End | float32 |
Fog Properties - Above Water - Fog Amount | float32 |
Noise Properties - Normals - UV Scale | float32 |
Fog Properties - Under Water - Fog Amount | float32 |
Fog Properties - Under Water - Fog Near Plane Distance | float32 |
Fog Properties - Under Water - Fog Far Plane Distance | float32 |
Water Properties - Distortion Amount | float32 |
Water Properties - Shininess | float32 |
Water Properties - Reflection HDR Multiplier | float32 |
Water Properties - Light Radius | float32 |
Water Properties - Light Brightness | float32 |
Noise Properties - Noise Layer One - UV Scale | float32 |
Noise Properties - Noise Layer Two - UV Scale | float32 |
Noise Properties - Noise Layer Three - UV Scale | float32 |
Noise Properties - Noise Layer One - Amplitude Scale | float32 |
Noise Properties - Noise Layer Two - Amplitude Scale | float32 |
Noise Properties - Noise Layer Three - Amplitude Scale | float32 |
Damage | uint16 |

### GNAM

Name | Type | Info
-----|------|-----
Daytime | formid | FormID of a [WATR](WATR.md) record, or null.
Nighttime | formid | FormID of a [WATR](WATR.md) record, or null.
Underwater | formid | FormID of a [WATR](WATR.md) record, or null.

