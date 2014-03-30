Conventions
===========

This page sets out the conventions used within this documentation. They are roughly similar to those used on [UESP.net](http://www.uesp.net/wiki/Tes5Mod:File_Format_Conventions).

## Data Types

These denote the type of data held in a field.

Type | Byte Size | Description
-----|-----------|------------
null | 0 | Field with no data.
char | 1 | A single 8-bit character
wchar | 2 | A single 16-bit character.
int8 | 1 | Value stored as an 8-bit unsigned integer.
uint8 | 1 | Value stored as an 8-bit signed integer.
int16 | 2 | Value stored as a 16-bit unsigned integer.
uint16 | 2 | Value stored as a 16-bit signed integer.
int32 | 4 | 
uint32 | 4 | 
int64 | 8 | 
uint64 | 8 | 
float32 | 4 | 
float64 | 8 | 
formid | 4 | A ulong used to identify a data object. May refer to a data object from a mod or new object created in-game.
cstring | variable | Null terminated string.

## Field Counts

These symbols are used to denote whether a record field is required or not, and how many times it may appear.

Symbol | Meaning
-------|--------
? | Unknown
+ | Appears once or more times.
* | Appears zero or more times.
- | Optional
