WTHR
====

Weather

## Format

Some of the field IDs begin with unprintable or whitespace characters. Such characters are given below using their hex values. Eg. `IIAD` would be `0x49 IAD` below if `I` were unprintable.

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | 0x00 IAD | Sunrise Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x01 IAD | Day Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x02 IAD | Sunset Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x03 IAD | Night Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
+ | DNAM | Cloud Textures - Layer 0 | cstring |
+ | CNAM | Cloud Textures - Layer 1 | cstring |
+ | ANAM | Cloud Textures - Layer 2 | cstring |
+ | BNAM | Cloud Textures - Layer 3 | cstring |
 | | [Model Data](Fields/Model.md) | collection |
+ | LNAM | Unknown | byte[4] |
+* | ONAM | Cloud Layer Speed | uint8 | Value is divided by 2550. There are 4 ONAMs, each for a different cloud layer.
-* | PNAM | Cloud Layer Color | struct | There are 4 PNAMs, each for a different cloud layer.
+* | NAM0 | Colors by Time & Type | struct | There are 10 NAM0s. The mapping to types is given below.
+ | FNAM | Fog Distance | struct |
+ | INAM | Unused | byte[304] |
+ | DATA | | struct |
-* | SNAM | Sound | struct |

### PNAM / NAM0

Name | Type | Info
-----|------|-----
Sunrise | rgba |
Day | rgba |
Sunset | rgba |
Night | rgba |
 
### NAM0 Mapping

NAM0 Index | Type
-----------|-----
0 | Sky-Upper
1 | Fog
2 | Unused
3 | Ambient
4 | Sunlight
5 | Sun
6 | Stars
7 | Sky-Lower
8 | Horizon
9 | Unused

### FNAM

Name | Type | Info
-----|------|-----
Day - Near | float32 |
Day - Far | float32 |
Night - Near | float32 |
Night - Far | float32 |
Day - Power | float32 |
Night - Power | float32 |

### DATA

Name | Type | Info
-----|------|-----
Wind Speed | uint8 |
Cloud Speed (Lower) | uint8 |
Cloud Speed (Upper) | uint8 |
Transition Delta | uint8 |
Sun Glare | uint8 |
Sun Damage | uint8 |
Precipitation - Begin Fade In | uint8 |
Precipitation - End Fade Out | uint8 |
Thunder / Lightning - Begin Fade In | uint8 |
Thunder / Lightning - End Fade Out | uint8 |
Thunder / Lightning - Frequency | uint8 |
Weather Classification | uint8 | Enum - see values below.
Lightning Color | rgb |
 
#### Weather Classification Values

Value | Meaning
------|--------
0 | None
1 | Pleasant
2 | Cloudy
4 | Rainy
8 | Snow

### SNAM

Name | Type | Info
-----|------|-----
Sound | formid | FormID of a [SOUN](SOUN.md) record.
Type | uint32 | Enum - see values below.
 
#### Type Values

Value | Meaning
------|--------
0 | Default
1 | Precipitation
2 | Wind
3 | Thunder
