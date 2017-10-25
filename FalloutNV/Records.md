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
[ACHR](Records/ACHR.html) | Placed NPC
[ACRE](Records/ACRE.html) | Placed Creature
[ACTI](Records/ACTI.html) | Activator
[ADDN](Records/ADDN.html) | Addon Node
[ALCH](Records/ALCH.html) | Ingestible
[ALOC](Records/ALOC.html) | Media Relation Controller
[AMEF](Records/AMEF.html) | Ammo Effect
[AMMO](Records/AMMO.html) | Ammunition
[ANIO](Records/ANIO.html) | Animated Object
[ARMO](Records/ARMO.html) | Armor
[ARMA](Records/ARMA.html) | Armor Addon
[ASPC](Records/ASPC.html) | Acoustic Space
[AVIF](Records/AVIF.html) | Actor Value Information
[BOOK](Records/BOOK.html) | Book
[BPTD](Records/BPTD.html) | Body Part Data
[CAMS](Records/CAMS.html) | Camera Shot
[CCRD](Records/CCRD.html) | Caravan Card
[CDCK](Records/CDCK.html) | Caravan Deck
[CELL](Records/CELL.html) | Cell
[CHAL](Records/CHAL.html) | Challenge
[CHIP](Records/CHIP.html) | Casino Chip
[CLAS](Records/CLAS.html) | Class
[CLMT](Records/CLMT.html) | Climate
[CMNY](Records/CMNY.html) | Caravan Money
[COBJ](Records/COBJ.html) | Constructable Object
[CONT](Records/CONT.html) | Container
[CPTH](Records/CPTH.html) | Camera Path
[CREA](Records/CREA.html) | Creature
[CSNO](Records/CSNO.html) | Casino
[CSTY](Records/CSTY.html) | Combat Style
[DEBR](Records/DEBR.html) | Debris
[DEHY](Records/DEHY.html) | Dehydration Stage
[DIAL](Records/DIAL.html) | Dialog Topic
[DOBJ](Records/DOBJ.html) | Default Object Manager
[DOOR](Records/DOOR.html) | Door
[ECZN](Records/ECZN.html) | Encounter Zone
[EFSH](Records/EFSH.html) | Effect Shader
[ENCH](Records/ENCH.html) | Object Effect
[EXPL](Records/EXPL.html) | Explosion
[EYES](Records/EYES.html) | Eyes
[FACT](Records/FACT.html) | Faction
[FLST](Records/FLST.html) | FormID List
[FURN](Records/FURN.html) | Furniture
[GLOB](Records/GLOB.html) | Global
[GMST](Records/GMST.html) | Game Setting
[GRAS](Records/GRAS.html) | Grass
[HAIR](Records/HAIR.html) | Hair
[HDPT](Records/HDPT.html) | Head Part
[HUNG](Records/HUNG.html) | Hunger Stage
[IDLE](Records/IDLE.html) | Idle Animation
[IDLM](Records/IDLM.html) | Idle Marker
[IMGS](Records/IMGS.html) | Image Space
[IMAD](Records/IMAD.html) | Image Space Modifier
[IMOD](Records/IMOD.html) | Item Mod
[INFO](Records/INFO.html) | Dialog Response
[INGR](Records/INGR.html) | Ingredient
[IPCT](Records/IPCT.html) | Impact
[IPDS](Records/IPDS.html) | Impact Data Set
[KEYM](Records/KEYM.html) | Key
[LAND](Records/LAND.html) | Landscape
[LGMT](Records/LGMT.html) | Lighting Template
[LIGH](Records/LIGH.html) | Light
[LSCR](Records/LSCR.html) | Load Screen
[LSCT](Records/LSCT.html) | Load Screen Type
[LTEX](Records/LTEX.html) | Landscape Texture
[LVLC](Records/LVLC.html) | Leveled Creature
[LVLI](Records/LVLI.html) | Leveled Item
[LVLN](Records/LVLN.html) | Leveled NPC
[MESG](Records/MESG.html) | Message
[MGEF](Records/MGEF.html) | Base Effect
[MICN](Records/MICN.html) | Menu Icon
[MISC](Records/MISC.html) | Misc. Item
[MSET](Records/MSET.html) | Media Set
[MSTT](Records/MSTT.html) | Moveable Static
[MUSC](Records/MUSC.html) | Music Type
[NAVI](Records/NAVI.html) | Navigation Mesh Info Map
[NAVM](Records/NAVM.html) | Navigation Mesh
[NOTE](Records/NOTE.html) | Note
[NPC_](Records/NPC_.html) | Non-Player Character
[PACK](Records/PACK.html) | Package
[PERK](Records/PERK.html) | Perk
[PGRE](Records/PGRE.html) | Placed Grenade
[PMIS](Records/PMIS.html) | Placed Missile
[PROJ](Records/PROJ.html) | Projectile
[PWAT](Records/PWAT.html) | Placeable Water
[QUST](Records/QUST.html) | Quest
[RACE](Records/RACE.html) | Race
[RADS](Records/RADS.html) | Radiation Stage
[RCCT](Records/RCCT.html) | Recipe Category
[RCPE](Records/RCPE.html) | Recipe
[REFR](Records/REFR.html) | Placed Object
[REGN](Records/REGN.html) | Region
[REPU](Records/REPU.html) | Reputation
[RGDL](Records/RGDL.html) | Ragdoll
[SCOL](Records/SCOL.html) | Static Collection
[SCPT](Records/SCPT.html) | Script
[SLPD](Records/SLPD.html) | Sleep Deprivation Stage
[SOUN](Records/SOUN.html) | Sound
[SPEL](Records/SPEL.html) | Actor Effect
[STAT](Records/STAT.html) | Static
[TACT](Records/TACT.html) | Talking Activator
[TERM](Records/TERM.html) | Terminal
[TES4](Records/TES4.html) | Plugin info
[TREE](Records/TREE.html) | Tree
[TXST](Records/TXST.html) | Texture Set
[VTYP](Records/VTYP.html) | Voice Type
[WATR](Records/WATR.html) | Water
[WEAP](Records/WEAP.html) | Weapon
[WRLD](Records/WRLD.html) | Worldspace
[WTHR](Records/WTHR.html) | Weather

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
