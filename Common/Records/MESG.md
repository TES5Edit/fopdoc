MESG
====

Message

## Format

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
+ | EDID | Editor ID | cstring |
+ | DESC | Description | cstring |
 | FULL | Name | cstring |
+ | INAM | Icon | formid | FormID of a [MICN](MICN.md) record, or null.
 | NAM1 | Unused | ?? |
 | NAM2 | Unused | ?? |
 | NAM3 | Unused | ?? |
 | NAM4 | Unused | ?? |
 | NAM5 | Unused | ?? |
 | NAM6 | Unused | ?? |
 | NAM7 | Unused | ?? |
 | NAM8 | Unused | ?? |
 | NAM9 | Unused | ?? |
+ | DNAM | Flags | uint32 | See below for values.
 | TNAM | Display Time | uint32 |
-* | | Menu Button | collection | See below for details.
 
### DNAM Flag Values

Value | Meaning
------|--------
0x00000001 | Message Box
0x00000002 | Auto Display

### Menu Button Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-------|------|------|-----
 | ITXT | Button Text | cstring |
-* | [CTDA](Subrecords/CTDA.md) | Condition | struct |
