Conventions
===========

This page sets out the conventions used within this documentation. They are roughly similar to those used on [UESP.net](http://www.uesp.net/wiki/Tes5Mod:File_Format_Conventions).

## Data Types

These denote the type of data held in a field.

<table>
  <thead>
    <tr><th>Type<th>Byte Size<th>Description
  <tbody>
    <tr><td>null<td>0<td>Field with no data.
    <tr><td>char<td>1<td>A single 8-bit character.
    <tr><td>wchar<td>2<td>A single 16-bit character.
    <tr><td>int8<td>1<td>Value stored as an 8-bit unsigned integer.
    <tr><td>uint8<td>1<td>Value stored as an 8-bit signed integer.
    <tr><td>int16<td>2<td>Value stored as a 16-bit unsigned integer.
    <tr><td>uint16<td>2<td>Value stored as a 16-bit signed integer.
    <tr><td>int32<td>4<td>
    <tr><td>uint32<td>4<td>
    <tr><td>int64<td>8<td>
    <tr><td>uint64<td>8<td>
    <tr><td>float32<td>4<td>
    <tr><td>float64<td>8<td>
    <tr><td>formid<td>4<td>A ulong used to identify a data object. May refer to a data object from a mod or new object created in-game.
    <tr><td><td><td>
    <tr><td><td><td>
    <tr><td><td><td>
    <tr><td><td><td>
    <tr><td><td><td>
</table>

## Field Counts

These symbols are used to denote whether a record field is required or not, and how many times it may appear.

<table>
  <thead>
    <tr><th>Symbol<th>Meaning
  <tbody>
    <tr><td>?<td>Unknown
    <tr><td>+<td>Appears once or more times.
    <tr><td>*<td>Appears zero or more times.
    <tr><td>-<td>Optional
</table>
