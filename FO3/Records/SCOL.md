SCOL
====

Static Collection

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | [OBND](Fields/OBND.md) | Object Bounds | struct |
+ | | [Model Data](Fields/Model.md) | | This is a field collection.
+* | | Part | | A field collection, see below for details.

### Part Field Collection

Count | Field | Name | Type | Info
------|-------|------|------|-----
 | ONAM | Static | formid | FormID of a [STAT](STAT.md) record.
+* | DATA | Placement | struct |

#### DATA

Count | Name | Type | Info
------|------|------|-----
 | X Position | float32 |
 | Y Position | float32 |
 | Z Position | float32 |
 | X Rotation | float32 |
 | Y Rotation | float32 |
 | Z Rotation | float32 |
 | Scale | float32 |
