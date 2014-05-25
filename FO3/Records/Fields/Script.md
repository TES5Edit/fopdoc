# Script Field Collection

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SCHR](SCHR.md) | Basic Script Data | struct |
+ | SCDA | Compiled Script Source | uint8[] |
+ | SCTX | Script Source | char[] |
-* | | [Local Variables](#local-variables) | | A field collection, see below for details.
-* | SCRO | Reference | formid *or* uint32 | A FormID or local variable reference.

### Local Variables


Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SLSD](#slsd) | Local Variable Data | struct |
+ | SCVR | Local Variable Name | cstring |

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
