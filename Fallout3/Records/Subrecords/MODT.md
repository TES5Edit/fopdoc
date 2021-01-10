---
layout: fallout3rec
title: fopdoc
---
MODT Subrecord
==============

Texture Filename Hashes

## Format

Count | Name | Type | Info
------|------|------|-----
+* | Texture Filename Hashes | struct |

### Texture Filename Hashes

Name | Type | Info
-----|------|-----
DDS Hash | byte[8] | DDS filename hash
DDX Hash | byte[8] | DDX filename hash (XBox 360)
DIR Hash | byte[8] | Directory hash

### Notes

May be used to map DDS filenames to XBox 360 DDX filenames. One entry for each texture referenced in the model.

This is unverified as the GECK does not create this subrecord. However it is 'internally' consistent as each texture reference with the same path has the same directory hash value.
