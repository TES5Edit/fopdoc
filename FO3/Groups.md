Groups
======

Groups are collections of records, and are used to improve scanning of files to make it easier to skip over records that the reading program is not interested in. In addition to this, subgroups for WRLD and CELL provide some useful structural information (e.g., the division of cell data into persistent and non-persistent references).

## Group Format

Name | Type | Description
-----|------|------------
type | char[4] | Always "GRUP".
groupSize | uint32 | Size of the group, *including* the 24 bytes before the data.
label | uint8 | 
groupType | int32 | 
stamp | uint16 | 
unknown | uint16 |
version | uint16 |
unknown | uint16 |
data | uint8[groupSize - 25] |

## Top Level Groups

## Misc