CONT
====

Container

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring | 
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
 | FULL | Name | cstring |
+ | | [Model Data](Fields/Model.md) | | This is a field collection.
 | SCRI | Script | formid | FormID of a [SCPT](SCPT.md) record.
-* | | Item | | This is a field collection. See below for details.
 | | [Destruction Data](Fields/Destruction.md) | | This is a field collection.
 | DATA | Data | struct
 | SNAM | Sound - Open | formid | FormID of a [SOUN](SOUN.md) record.
 | QNAM | Sound - Close | formid | FormID of a [SOUN](SOUN.md) record.
 
 
### Item Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | CNTO | Item | struct | 
 | COED | Extra Data | struct |

#### CNTO

Count | Name | Type | Info
------|------|------|-----
 | Item | formid | FormID of a [ARMO](.md), [AMMO](AMMO.md), [MISC](MISC.md), [WEAP](WEAP.md), [BOOK](BOOK.md), [LVLI](LVLI.md), [KEYM](KEYM.md), [ALCH](ALCH.md), [NOTE](NOTE.md), [MSTT](MSTT.md) or [STAT](STAT.md) record.
 | Count | int32 | 

#### COED

Count | Name | Type | Info
------|------|------|-----
 | Owner | formid | FormID of a [NPC_](NPC_.md) or [FACT](FACT.md) record, or null.
 | Global Variable / Required Rank | formid *or* uint32 | FormID of a [GLOB](GLOB.md) record, an integer representing the required rank, or null.
 | Item Condition | float32 |
 
 
 
