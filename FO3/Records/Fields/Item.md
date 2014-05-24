Item Field Collection
=====================

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | [CNTO](#cnto) | Item | struct | 
 | [COED](#coed) | Extra Data | struct |

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
