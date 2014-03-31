Records
=======

## Record Types

Each record type's page documents its fields. The common record header structure is documented further down this page.

Type | Name
-----|------------
[ACHR](Records/ACHR.md) | Placed NPC
[ACRE](Records/ACRE.md) | Placed Creature
ACTI | Activator
ADDN | Addon Node
ALCH | Ingestible
AMMO | Ammunition
ANIO | Animated Object
ARMO | Armor
ARMA | Armor Addon
ASPC | Acoustic Space
AVIF | Actor Value Information
BOOK | Book
BPTD | Body Part Data
CAMS | Camera Shot
CELL | Cell
CLAS | Class
CLMT | Climate
COBJ | Constructable Object
CONT | Container
CPTH | Camera Path
CREA | Creature
CSTY | Combat Style
DEBR | Debris
DIAL | Dialog Topic
DOBJ | Default Object Manager
DOOR | Door
ECZN | Encounter Zone
EFSH | Effect Shader
ENCH | Object Effect
EXPL | Explosion
EYES | Eyes
FACT | Faction
FLST | FormID List
FURN | Furniture
GLOB | Global
GMST | Game Setting
GRAS | Grass
HAIR | Hair
HDPT | Head Part
IDLE | Idle Animation
IDLM | Idle Marker
IMGS | Image Space
IMAD | Image Space Modifier
INFO | Dialog Response
INGR | Ingredient
IPCT | Impact
IPDS | Impact Data Set
KEYM | Key
LAND | Landscape
LGMT | Lighting Template
LIGH | Light
LSCR | Load Screen
LTEX | Landscape Texture
LVLC | Leveled Creature
LVLI | Leveled Item
LVLN | Leveled NPC
MESG | Message
MGEF | Base Effect
MICN | Menu Icon
MISC | Misc. Item
MSTT | Moveable Static
MUSC | Music Type
NAVI | Navigation Mesh Info Map
NAVM | Navigation Mesh
NOTE | Note
NPC_ | Non-Player Character
PACK | Package
PERK | Perk
PGRE | Placed Grenade
PMIS | Placed Missile
PROJ | Projectile
PWAT | Placeable Water
QUST | Quest
RACE | Race
RADS | Radiation Stage
REFR | Placed Object
REGN | Region
RGDL | Ragdoll
SCOL | Static Collection
SCPT | Script
SOUN | Sound
SPEL | Actor Effect
STAT | Static
TACT | Talking Activator
TERM | Terminal
[TES4](Records/TES4.md) | Plugin info
TREE | Tree
TXST | Texture Set
VTYP | Voice Type
WATR | Water
WEAP | Weapon
WRLD | Worldspace
WTHR | Weather

## Record Format

Name | Type | Info
-----|------|-----
type | char[4] | Record type.
dataSize | uint32 | Size of the data.
flags | uint32 | Record flags. See the section below for details.
id | formid | The record FormID. TES4 records have a FormID of `0`.
revision | uint32 | Used for revision control by the Creation Kit, if enabled.
version | uint16 | ??
unknown | uint16 | ??
data | uint8[dataSize] | For uncompressed records, this is a sequence of fields. For compressed records, see the section below for details.

### Flags

Flags have contextual meaning depending on the record type. The known meanings are given below.

Flag | Meaning
-----|--------
0x00000001 | The plugin is a master file.
0x00000002 | ??
0x00000004 | ??
0x00000008 | ??
0x00000010 | ??
0x00000020 | Deleted
0x00000040 | Border Region / Has Tree LOD / Constant / Hidden From Local Map
0x00000080 | Turn Off Fire
0x00000100 | Inaccessible
0x00000200 | Casts shadows / On Local Map / Motion Blur
0x00000400 | Quest item / Persistent reference
0x00000800 | Initially disabled
0x00001000 | Ignored
0x00002000 | No Voice Filter
0x00004000 | ??
0x00008000 | Visible when distant
0x00010000 | Random Anim Start / High Priority LOD
0x00020000 | Dangerous / Off limits (Interior cell) / Radio Station (Talking Activator)
0x00040000 | Compressed
0x00080000 | Can't wait / Platform Specific Texture
0x00100000 | ??
0x00200000 | ??
0x00400000 | ??
0x00800000 | ??
0x01000000 | ??
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
compData | uint8[ dataSize - 4 ] | Collection of fields compressed using [zlib](http://zlib.net/).


## Field Format

Name | Type | Info
-----|------|-----
type | char[4] | Field type.
dataSize | uint16 | Size of the data, unless the preceding field has the type `XXXX`, in which case this will be `0` and the size of the data field will be given by the preceding field's data, interpreted as a 32-bit unsigned integer.
data | uint8[dataSize] | The format of the data depends on the field type and the type of the record containing it.
