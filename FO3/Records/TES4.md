TES4 Record
===========

## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | HEDR | header | struct | Contains additional details about the plugin, see section below.
- | OFST | unknown | ?? | ??
- | DELE | unknown | ?? | ??
+ | CNAM | author | cstring | Maximum size is 512 bytes, including terminator.
- | SNAM | description | cstring | Maximum size is 512 bytes, including terminator.
-* | | Master Data | | Data on the plugin's master files, listed in the order they were present in when the plugin was written.
- | ONAM | formOverrides | formid[] | Overriden records. Number of records can be obtained by dividing the field size by the size of a FormID.
- | SCRN | screenshot | ?? | ??

### HEDR

Count | Name | Type | Info
------|------|------|-----
+ | version | float32 | 0.94 in most files; 1.7 in recent versions of Update.esm.
+ | numRecords | uint32 | Number of records and groups (not including TES4 record itself).
+ | nextObjectId | uint32 | Next available object ID.

### Master Data

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | MAST | master | cstring | The filename of a master plugin.
+ | DATA | fileSize | uint64 | One DATA field appears directly after each MAST field present. Always `0`, probably vestigial. In TES3, the file size of the previous master was recorded here.
