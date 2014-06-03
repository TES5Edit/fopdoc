Conventions
===========

This page sets out the conventions used within this documentation. They are roughly similar to those used on [UESP.net](http://www.uesp.net/wiki/Tes5Mod:File_Format_Conventions).

Anything unknown is marked as such with a double question mark `??`. If a table cell is blank, that just means that it hasn't yet been documented.

## Data Types

These denote the type of data held in a subrecord or field. Type arrays are represented by `type[array length]`. Variable-length arrays are represented by `type[]`.

### Basic Types

Type | Byte Size | Description
-----|-----------|------------
null | 0 | Subrecord with no data.
char | 1 | A single 8-bit character
int8 | 1 | Value stored as an 8-bit signed integer.
uint8 | 1 | Value stored as an 8-bit unsigned integer.
int16 | 2 | Value stored as a 16-bit signed integer.
uint16 | 2 | Value stored as a 16-bit unsigned integer.
int32 | 4 | Value stored as a 32-bit signed integer.
uint32 | 4 | Value stored as a 32-bit unsigned integer.
int64 | 8 | Value stored as a 64-bit signed integer.
uint64 | 8 | Value stored as a 64-bit unsigned integer.
float32 | 4 | Value stored as a 32-bit floating point number.
float64 | 8 | Value stored as a 64-bit floating point number.

### Semantic Types

Type | Byte Size | Description
-----|-----------|------------
formid | 4 | Used to identify a data object. May refer to a data object from a mod or new object created in-game.
cstring | variable | Null terminated string.
struct | variable | Used for subrecords containing more than one data type. The subrecord structure should be documented on the same page.
rgba | 4 | The first three bytes are red, green and blue color values respectively. The fourth byte is unused.
collection | variable | Used for collections of subrecords that appear together.
byte | 1 | Used when the data type of a subrecord or field is unknown, or can be of many different types depending on some factor (which is detailed elsewhere).

## Subrecord Counts

These symbols are used to denote whether a record subrecord is required or not, and how many times it may appear. A blank count table cell is equivalent to one containing a `-`.

Symbol | Meaning
-------|--------
+ | Required. Such subrecords are always present in official plugins and plugins made with the GECK.
- | Optional. Such subrecords are not always present in official plugins and plugins made with the GECK.
* | Can appear more than once (stacks with `+` and `-`).
