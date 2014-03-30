Groups
======

Groups are collections of records, and are used to improve scanning of files to make it easier to skip over records that the reading program is not interested in. In addition to this, subgroups for WRLD and CELL provide some useful structural information (e.g., the division of cell data into persistent and non-persistent references).

## Group Format

<table>
    <thead>
        <tr><th>Name<th>Type<th>Description
    <tbody>
        <tr><td>type<td>char[4]<td>Always "GRUP".
        <tr><td>groupSize<td>uint32<td>Size of the group, *including* the 24 bytes before the data.
        <tr><td>label<td>uint8<td>
        <tr><td>groupType<td>int32<td>
        <tr><td>stamp<td>uint16<td>
        <tr><td>unknown<td>uint16<td>
        <tr><td>version<td>uint16<td>
        <tr><td>unknown<td>uint16<td>
        <tr><td>data<td>uint8<td>
</table>

## Top Level Groups

## Misc