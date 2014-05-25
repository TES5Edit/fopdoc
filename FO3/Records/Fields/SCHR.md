SCHR Field
==========

As used in the [SCPT](../SCPT.md) record type and the [embedded script](Embedded Script.md) field collection.

## Format

Count | Name | Type | Info
------|------|------|-----
 | Unused | uint8[4] | 
 | Ref Count | uint32 |
 | Compiled Size | uint32 |
 | Variable Count | uint32 |
 | Type | uint16 | See below for values.
 | Flags | uint16 | See below for values.
 
#### Type Enum Values

Value | Meaning
------|--------
0 | Object
1 | Quest
0x100 | Effect

#### Flag Values

Value | Meaning
------|--------
0x0001 | Enabled
