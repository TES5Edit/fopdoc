SCOL
====

Static Collection

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Subrecords/OBND.md) | Object Bounds | struct |
+ | | [Model Data](Subrecords/Model.md) | collection |
+* | | Part | collection | See below for details.

### Part Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | ONAM | Static | formid | FormID of a [STAT](STAT.md) record.
+ | DATA | Placements | struct |

#### DATA

The DATA subrecord consists of an array of objects with the following structure.

Name | Type | Info
-----|------|-----
X Position | float32 |
Y Position | float32 |
Z Position | float32 |
X Rotation | float32 |
Y Rotation | float32 |
Z Rotation | float32 |
Scale | float32 |
