---
layout: fallout3rec
title: fopdoc
---
GMST
====

Game Setting

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | DATA | Value | cstring *or* int32 *or* float32 | The value is interpreted as a cstring if the Editor ID starts with `s`, or as a float32 if it starts with `f`. Otherwise it is interpreted as an int32.
