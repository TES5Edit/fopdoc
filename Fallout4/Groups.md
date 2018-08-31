Groups
======

Groups are collections of records, and are used to improve scanning of files to make it easier to skip over records that the reading program is not interested in. In addition to this, subgroups for [WRLD](Records/WRLD.md) and [CELL](Records/CELL.md) provide some useful structural information (e.g., the division of cell data into persistent and non-persistent references).

## Group Format

Name | Type | Description
-----|------|------------
type | char[4] | Always "GRUP".
groupSize | uint32 | Size of the group, *including* the 24 bytes before the data.
label | byte[4] | Format depends on the group type.
groupType | int32 | The group type. See the section below for details.
stamp | uint16 | A date stamp. The first byte is the day of the month, and the second byte is the number of months since some unknown point in time (perhaps July 2004, when Bethesda began development of Fallout 3).
Unknown | byte[6] |
data | byte[groupSize - 24] | The records and subgroups contained within the group.

### Group Types

Group Type | Label Type | Group Type Name | Label Info | Group Info
-----------|------------|-----------------|------------|-----------
0 | char[4] | Top Level | A record type. | Contains records of the given type.


TODO: Fill in this table like for Fallout 3 and Fallout: New Vegas.

## Top-Level Groups

The top level groups are stored in the following order in `Fallout4.esm`. It is unknown if this order is required, but it would be best to follow it just in case.

TODO: Fill in this list like for Fallout 3 and Fallout: New Vegas.
