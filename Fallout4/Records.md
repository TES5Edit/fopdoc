---
layout: fallout4rec
title: fopdoc
---
Records
=======

## Record Types

Each record type's page documents its subrecords. The common record header structure is documented further down this page.

Type | Name
-----|------------
[AACT](Records/AACT.md) | Action
[BNDS](Records/BNDS.md) | Bendable Spline { New to Fallout 4 }
[CLAS](Records/CLAS.md) | Class
[DMGT](Records/DMGT.md) | Damage Type { New to Fallout 4 }
[FACT](Records/FACT.md) | Faction
[GLOB](Records/GLOB.md) | Global Variable
[GMST](Records/GMST.md) | Game Setting
[KYWD](Records/KYWD.md) | Keyword
[LCRT](Records/LCRT.md) | Location Reference Type
[LTEX](Records/LTEX.md) | Landscape Texture
[LVLI](Records/LVLI.md) | Leveled Item
[LVLN](Records/LVLN.md) | Leveled NPC
[TRNS](Records/TRNS.md) | TRNS Record { New to Fallout 4 }
[TXST](Records/TXST.md) | Texture Set

## Record Format

Name | Type | Info
-----|------|-----
type | char[4] | Record type.
dataSize | uint32 | Size of the data.
flags | uint32 | Record flags. See the section below for details.
id | formid | The record FormID. TES4 records have a FormID of `0`.
revision | uint32 | ??
version | uint16 | ??
unknown | uint16 | ??
data | uint8[dataSize] | For uncompressed records, this is a sequence of subrecords. For compressed records, see the section below for details.

### Flags

Flags have contextual meaning depending on the record type. The known meanings are given below.

Flag | Meaning
-----|--------
0x00000001 | The plugin is a master file.
0x00000200 | The plugin is a light master.


### Compressed Data

Compressed data has the following format.

Name | Type | Info
-----|------|-----
decompSize | uint32 | Size of the decompressed data.
compData | uint8[ dataSize - 4 ] | Collection of subrecords compressed using [zlib](http://zlib.net/).


## Subrecord Format

Name | Type | Info
-----|------|-----
type | char[4] | Subrecord type.
dataSize | uint16 | Size of the data.
data | uint8[dataSize] | The format of the data depends on the subrecord type and the type of the record containing it.
