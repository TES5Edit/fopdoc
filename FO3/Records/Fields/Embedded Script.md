# Embedded Script Field Collection


## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SCHR](#schr) | Basic Script Data | struct | Patrol data, embedded script.
+ | SCDA | Compiled Embedded Script Source | uint8[] | Patrol data, embedded script.
+ | SCTX | Embedded Script Source | char[] | Patrol data, embedded script.
-* | | [Local Variables](#local-variables) | | A field collection, see below for details.
-* | SCRO | Reference | formid *or* uint32 | Patrol data, embedded script. A FormID or local variable reference.


### SCHR

Count | Name | Type | Info
------|------|------|-----
 | Unused | uint8[4] | 
 | Ref Count | uint32 |
 | Compiled Size | uint32 |
 | Variable Count | uint32 |
 | Type | uint16 | See below for values.
 | Flags | uint16 | See below for values.
 
#### Type Enum Values

Value | Meaning
------|--------
0 | Object
1 | Quest
0x100 | Effect

#### Flag Values

Value | Meaning
------|--------
0x0001 | Enabled

### Local Variables


Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SLSD](#slsd) | Local Variable Data | struct | Patrol data, embedded script.
+ | SCVR | Local Variable Name | cstring | Patrol data, embedded script.

#### SLSD

Count | Name | Type | Info
------|------|------|-----
 | Index | uint32 |
 | Unused | uint8[12] |
 | Flags | uint8 | See below for values.
 | Unused | uint8[7] |
 
##### Flag Values

Value | Meaning
------|--------
0x01 | IsLongOrShort
