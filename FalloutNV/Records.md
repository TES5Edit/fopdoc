---
layout: falloutnvrec
title: fopdoc
---
Records
=======

## Record Types

Each record type's page documents its subrecords. The common record header structure is documented further down this page.

Type | Name
-----|------------
[ACHR](Records/ACHR.md) | Placed NPC
[ACRE](Records/ACRE.md) | Placed Creature
[ACTI](Records/ACTI.md) | Activator
[ADDN](Records/ADDN.md) | Addon Node
[ALCH](Records/ALCH.md) | Ingestible
[ALOC](Records/ALOC.md) | Media Relation Controller
[AMEF](Records/AMEF.md) | Ammo Effect
[AMMO](Records/AMMO.md) | Ammunition
[ANIO](Records/ANIO.md) | Animated Object
[ARMO](Records/ARMO.md) | Armor
[ARMA](Records/ARMA.md) | Armor Addon
[ASPC](Records/ASPC.md) | Acoustic Space
[AVIF](Records/AVIF.md) | Actor Value Information
[BOOK](Records/BOOK.md) | Book
[BPTD](Records/BPTD.md) | Body Part Data
[CAMS](Records/CAMS.md) | Camera Shot
[CCRD](Records/CCRD.md) | Caravan Card
[CDCK](Records/CDCK.md) | Caravan Deck
[CELL](Records/CELL.md) | Cell
[CHAL](Records/CHAL.md) | Challenge
[CHIP](Records/CHIP.md) | Casino Chip
[CLAS](Records/CLAS.md) | Class
[CLMT](Records/CLMT.md) | Climate
[CMNY](Records/CMNY.md) | Caravan Money
[COBJ](Records/COBJ.md) | Constructable Object
[CONT](Records/CONT.md) | Container
[CPTH](Records/CPTH.md) | Camera Path
[CREA](Records/CREA.md) | Creature
[CSNO](Records/CSNO.md) | Casino
[CSTY](Records/CSTY.md) | Combat Style
[DEBR](Records/DEBR.md) | Debris
[DEHY](Records/DEHY.md) | Dehydration Stage
[DIAL](Records/DIAL.md) | Dialog Topic
[DOBJ](Records/DOBJ.md) | Default Object Manager
[DOOR](Records/DOOR.md) | Door
[ECZN](Records/ECZN.md) | Encounter Zone
[EFSH](Records/EFSH.md) | Effect Shader
[ENCH](Records/ENCH.md) | Object Effect
[EXPL](Records/EXPL.md) | Explosion
[EYES](Records/EYES.md) | Eyes
[FACT](Records/FACT.md) | Faction
[FLST](Records/FLST.md) | FormID List
[FURN](Records/FURN.md) | Furniture
[GLOB](Records/GLOB.md) | Global
[GMST](Records/GMST.md) | Game Setting
[GRAS](Records/GRAS.md) | Grass
[HAIR](Records/HAIR.md) | Hair
[HDPT](Records/HDPT.md) | Head Part
[HUNG](Records/HUNG.md) | Hunger Stage
[IDLE](Records/IDLE.md) | Idle Animation
[IDLM](Records/IDLM.md) | Idle Marker
[IMGS](Records/IMGS.md) | Image Space
[IMAD](Records/IMAD.md) | Image Space Modifier
[IMOD](Records/IMOD.md) | Item Mod
[INFO](Records/INFO.md) | Dialog Response
[INGR](Records/INGR.md) | Ingredient
[IPCT](Records/IPCT.md) | Impact
[IPDS](Records/IPDS.md) | Impact Data Set
[KEYM](Records/KEYM.md) | Key
[LAND](Records/LAND.md) | Landscape
[LGMT](Records/LGMT.md) | Lighting Template
[LIGH](Records/LIGH.md) | Light
[LSCR](Records/LSCR.md) | Load Screen
[LSCT](Records/LSCT.md) | Load Screen Type
[LTEX](Records/LTEX.md) | Landscape Texture
[LVLC](Records/LVLC.md) | Leveled Creature
[LVLI](Records/LVLI.md) | Leveled Item
[LVLN](Records/LVLN.md) | Leveled NPC
[MESG](Records/MESG.md) | Message
[MGEF](Records/MGEF.md) | Base Effect
[MICN](Records/MICN.md) | Menu Icon
[MISC](Records/MISC.md) | Misc. Item
[MSET](Records/MSET.md) | Media Set
[MSTT](Records/MSTT.md) | Moveable Static
[MUSC](Records/MUSC.md) | Music Type
[NAVI](Records/NAVI.md) | Navigation Mesh Info Map
[NAVM](Records/NAVM.md) | Navigation Mesh
[NOTE](Records/NOTE.md) | Note
[NPC_](Records/NPC_.md) | Non-Player Character
[PACK](Records/PACK.md) | Package
[PERK](Records/PERK.md) | Perk
[PGRE](Records/PGRE.md) | Placed Grenade
[PMIS](Records/PMIS.md) | Placed Missile
[PROJ](Records/PROJ.md) | Projectile
[PWAT](Records/PWAT.md) | Placeable Water
[QUST](Records/QUST.md) | Quest
[RACE](Records/RACE.md) | Race
[RADS](Records/RADS.md) | Radiation Stage
[RCCT](Records/RCCT.md) | Recipe Category
[RCPE](Records/RCPE.md) | Recipe
[REFR](Records/REFR.md) | Placed Object
[REGN](Records/REGN.md) | Region
[REPU](Records/REPU.md) | Reputation
[RGDL](Records/RGDL.md) | Ragdoll
[SCOL](Records/SCOL.md) | Static Collection
[SCPT](Records/SCPT.md) | Script
[SLPD](Records/SLPD.md) | Sleep Deprivation Stage
[SOUN](Records/SOUN.md) | Sound
[SPEL](Records/SPEL.md) | Actor Effect
[STAT](Records/STAT.md) | Static
[TACT](Records/TACT.md) | Talking Activator
[TERM](Records/TERM.md) | Terminal
[TES4](Records/TES4.md) | Plugin info
[TREE](Records/TREE.md) | Tree
[TXST](Records/TXST.md) | Texture Set
[VTYP](Records/VTYP.md) | Voice Type
[WATR](Records/WATR.md) | Water
[WEAP](Records/WEAP.md) | Weapon
[WRLD](Records/WRLD.md) | Worldspace
[WTHR](Records/WTHR.md) | Weather

## Record Format

Name | Type | Info
-----|------|-----
type | char[4] | Record type.
dataSize | uint32 | Size of the data.
flags | uint32 | Record flags. See the section below for details.
id | formid | The record FormID. TES4 records have a FormID of `0`.
revision | uint32 | Used for revision control by the Creation Kit, if enabled.
version | uint16 | Form Version
unknown | uint16 | ??
data | uint8[dataSize] | For uncompressed records, this is a sequence of subrecords. For compressed records, see the section below for details.

### Flags

Flags have contextual meaning depending on the record type. The known meanings are given below.

Flag | Meaning
-----|--------
0x00000001 | The plugin is a master file.
0x00000002 | ??
0x00000004 | ??
0x00000008 | ??
0x00000010 | Form initialized (Runtime only)
0x00000020 | Deleted
0x00000040 | Border Region / Has Tree LOD / Constant / Hidden From Local Map
0x00000080 | Turn Off Fire
0x00000100 | Inaccessible
0x00000200 | Casts shadows / On Local Map / Motion Blur
0x00000400 | Quest item / Persistent reference
0x00000800 | Initially disabled
0x00001000 | Ignored
0x00002000 | No Voice Filter
0x00004000 | Cannot Save (Runtime only)
0x00008000 | Visible when distant
0x00010000 | Random Anim Start / High Priority LOD
0x00020000 | Dangerous / Off limits (Interior cell) / Radio Station (Talking Activator)
0x00040000 | Compressed
0x00080000 | Can't wait / Platform Specific Texture / Dead
0x00100000 | ??
0x00200000 | ??
0x00400000 | ??
0x00800000 | ??
0x01000000 | Destructible (Runtime only)
0x02000000 | Obstacle / No AI Acquire
0x04000000 | NavMesh Generation - Filter
0x08000000 | NavMesh Generation - Bounding Box
0x10000000 | Non-Pipboy / Reflected by Auto Water
0x20000000 | Child Can Use / Refracted by Auto Water
0x40000000 | NavMesh Generation - Ground
0x80000000 | ??


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
dataSize | uint16 | Size of the data, unless the preceding subrecord has the type `XXXX`, in which case this will be `0` and the size of the data field will be given by the preceding subrecord's data, interpreted as a 32-bit unsigned integer.
data | uint8[dataSize] | The format of the data depends on the subrecord type and the type of the record containing it.
