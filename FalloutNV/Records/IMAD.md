---
layout: falloutnvrec
title: fopdoc
---
IMAD
====

Image Space Adapter

## Format

Some of the subrecord codes begin with unprintable or whitespace characters. Such characters are given below using their hex values. Eg. `IIAD` would be `0x49 IAD` below if `I` were unprintable. The Time and Color structures used by many of the subrecords are detailed below.

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | EDID | Editor ID | cstring |
 | DNAM | Data Count | struct |
 | BNAM | Blur Radius | struct[] | An array of Time structures.
 | VNAM | Double Vision Strength | struct[] | An array of Time structures.
 | TNAM | Tint Color | struct[] | An array of Color structures.
 | NAM3 | Fade Color | struct[] | An array of Color structures.
 | RNAM | Radial Blur Strength | struct[] | An array of Time structures.
 | SNAM | Radial Blur Ramp Up | struct[] | An array of Time structures.
 | UNAM | Radial Blur Start | struct[] | An array of Time structures.
 | NAM1 | Radial Blur Ramp Down | struct[] | An array of Time structures.
 | NAM2 | Radial Blur Down Start | struct[] | An array of Time structures.
 | WNAM | DoF Strength | struct[] | An array of Time structures.
 | XNAM | DoF Distance | struct[] | An array of Time structures.
 | YNAM | DoF Range | struct[] | An array of Time structures.
 | NAM4 | Motion Blur Strength | struct[] | An array of Time structures.
 | 0x00 IAD | HDR Eye Adapt Speed Mult | struct[] | An array of Time structures.
 | @IAD | HDR Eye Adapt Speed Add | struct[] | An array of Time structures.
 | 0x01 IAD | HDR Bloom Blur Radius Mult | struct[] | An array of Time structures.
 | AIAD | HDR Bloom Blur Radius Add | struct[] | An array of Time structures.
 | 0x02 IAD | HDR Bloom Threshold Mult | struct[] | An array of Time structures.
 | BIAD | HDR Bloom Threshold Add | struct[] | An array of Time structures.
 | 0x03 IAD | HDR Bloom Scale Mult | struct[] | An array of Time structures.
 | CIAD | HDR Bloom Scale Add | struct[] | An array of Time structures.
 | 0x04 IAD | HDR Target Lum Min Mult | struct[] | An array of Time structures.
 | DIAD | HDR Target Lum Min Add | struct[] | An array of Time structures.
 | 0x05 IAD | HDR Target Lum Max Mult | struct[] | An array of Time structures.
 | EIAD | HDR Target Lum Max Add | struct[] | An array of Time structures.
 | 0x06 IAD | HDR Sunlight Scale Mult | struct[] | An array of Time structures.
 | FIAD | HDR Sunlight Scale Add | struct[] | An array of Time structures.
 | 0x07 IAD | HDR Sky Scale Mult | struct[] | An array of Time structures.
 | GIAD | HDR Sky Scale Add | struct[] | An array of Time structures.
 | 0x08 IAD | Unknown | ?? |
 | HIAD | Unknown | ?? |
 | 0x09 IAD | Unknown | ?? |
 | IIAD | Unknown | ?? |
 | 0x0A IAD | Unknown | ?? |
 | JIAD | Unknown | ?? |
 | 0x0B IAD | Unknown | ?? |
 | KIAD | Unknown | ?? |
 | 0x0C IAD | Unknown | ?? |
 | LIAD | Unknown | ?? |
 | 0x0D IAD | Unknown | ?? |
 | MIAD | Unknown | ?? |
 | 0x0E IAD | Unknown | ?? |
 | NIAD | Unknown | ?? |
 | 0x0F IAD | Unknown | ?? |
 | OIAD | Unknown | ?? |
 | 0x10 IAD | Unknown | ?? |
 | PIAD | Unknown | ?? |
 | 0x11 IAD | Cinematic Saturation Mult | struct[] | An array of Time structures.
 | QIAD | Cinematic Saturation Add | struct[] | An array of Time structures.
 | 0x12 IAD | Cinematic Brightness Mult | struct[] | An array of Time structures.
 | RIAD | Cinematic Brightness Add | struct[] | An array of Time structures.
 | 0x13 IAD | Cinematic Contrast Mult | struct[] | An array of Time structures.
 | SIAD | Cinematic Contrast Add | struct[] | An array of Time structures.
 | 0x14 IAD | Unknown | ?? |
 | TIAD | Unknown | ?? |
 | RDSD | Sound - Intro | formid | FormID of a [SOUN](SOUN.html) record.
 | RDSI | Sound - Outro | formid | FormID of a [SOUN](SOUN.html) record.


### DNAM

Name | Type | Info
-----|------|-----
Flags | uint32 | See below for flag values.
Duration | float32 |
HDR Eye Adapt Speed Mult | uint32 |
HDR Eye Adapt Speed Add | uint32 |
HDR Bloom Blur Radius Mult | uint32 |
HDR Bloom Blur Radius Add | uint32 |
HDR Bloom Threshold Mult | uint32 |
HDR Bloom Threshold Add | uint32 |
HDR Bloom Scale Mult | uint32 |
HDR Bloom Scale Add | uint32 |
HDR Target Lum Min Mult | uint32 |
HDR Target Lum Min Add | uint32 |
HDR Target Lum Max Mult | uint32 |
HDR Target Lum Max Add | uint32 |
HDR Sunlight Scale Mult | uint32 |
HDR Sunlight Scale Add | uint32 |
HDR Sky Scale Mult | uint32 |
HDR Sky Scale Add | uint32 |
Unknown | uint8[72] |
Cinematic Saturation Mult | uint32 |
Cinematic Saturation Add | uint32 |
Cinematic Brightness Mult | uint32 |
Cinematic Brightness Add | uint32 |
Cinematic Contrast Mult | uint32 |
Cinematic Contrast Add | uint32 |
Unknown | uint8[8] |
Tint Color | uint32 |
Blur Radius | uint32 |
Double Vision Strength | uint32 |
Radial Blur Strength | uint32 |
Radial Blur Ramp Up | uint32 |
Radial Blur Start | uint32 |
Radial Blur Flags | uint32 | See below for flag values.
Radial Blur Center X | uint32 |
Radial Blur Center Y | uint32 |
Depth of Field Strength | uint32 |
Depth of Field Distance | uint32 |
Depth of Field Range | uint32 |
Depth of Field Flags | uint32 | See below for flag values.
Radial Blur Ramp Down | uint32 |
Radial Blur Down Start | uint32 |
Fade Color | uint32 |
Motion Blur Strength | uint32 |

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Animatable

#### Radial Blur Flag Values

Value | Meaning
------|--------
0x00000001 | Use Target

#### Depth of Field Flag Values

Value | Meaning
------|--------
0x00000001 | Use Target

### Time Structure

Name | Type | Info
-----|------|-----
Time | float32 |
Value | float32 |

### Color Structure

Name | Type | Info
-----|------|-----
Time | float32 |
Red | float32 |
Green | float32 |
Blue | float32 |
Alpha | float32 |
