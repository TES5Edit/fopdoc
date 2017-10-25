---
layout: falloutnvrec
title: fopdoc
---
WTHR
====

Weather

## Format

Some of the subrecord codes begin with unprintable or whitespace characters. Such characters are given below using their hex values. Eg. `IIAD` would be `0x49 IAD` below if `I` were unprintable.

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
 | 0x00 IAD | Sunrise Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x01 IAD | Day Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x02 IAD | Sunset Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x03 IAD | Night Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x04 IAD | High Noon Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
 | 0x05 IAD | Midnight Image Space Modifier | formid | FormID of an [IMAD](IMAD.md) record.
+ | DNAM | Cloud Textures - Layer 0 | cstring |
+ | CNAM | Cloud Textures - Layer 1 | cstring |
+ | ANAM | Cloud Textures - Layer 2 | cstring |
+ | BNAM | Cloud Textures - Layer 3 | cstring |
 | | [Model Data](Subrecords/Model.md) | collection |
+ | LNAM | Unknown | byte[4] |
+ | ONAM | Cloud Layer Speed | uint8[4] | Value is divided by 2550. Each uint8 is for a different cloud layer.
- | PNAM | Cloud Layer Color | struct[4] | Array of Time of Day Colors structures. Each structure is for a different cloud layer.
+ | NAM0 | Colors by Time & Type | struct |
+ | FNAM | Fog Distance | struct |
+ | INAM | Unused | byte[304] |
+ | DATA | | struct |
-* | SNAM | Sound | struct |

### Time of Day Colors Structure

Name | Type | Info
-----|------|-----
Sunrise | rgba |
Day | rgba |
Sunset | rgba |
Night | rgba |
High Noon | rgba |
Midnight | rgba |

### NAM0

Name | Type | Info
-----|------|-----
Sky-Upper | struct | A Time of Day Colors structure.
Fog | struct | A Time of Day Colors structure.
Unused | struct | A Time of Day Colors structure.
Ambient | struct | A Time of Day Colors structure.
Sunlight | struct | A Time of Day Colors structure.
Sun | struct | A Time of Day Colors structure.
Stars | struct | A Time of Day Colors structure.
Sky-Lower | struct | A Time of Day Colors structure.
Horizon | struct | A Time of Day Colors structure.
Unused | struct | A Time of Day Colors structure.

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
