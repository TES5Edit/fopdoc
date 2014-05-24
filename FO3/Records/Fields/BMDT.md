BMDT Field
==========

As used in the [ARMO](../ARMO.md) and [ARMA](../ARMA.md) record types.

## Format

Count | Name | Type | Info
------|------|------|-----
 | Biped Flags | uint32 |
 | General Flags | uint8 |
 | Unused | uint8
 
#### Biped Flag Values

Value | Meaning
-----|--------
0x00000001 | Head
0x00000002 | Hair
0x00000004 | Upper Body
0x00000008 | Left Hand
0x00000010 | Right Hand
0x00000020 | Weapon
0x00000040 | PipBoy
0x00000080 | Backpack
0x00000100 | Necklace
0x00000200 | Headband
0x00000400 | Hat
0x00000800 | Eye Glasses
0x00001000 | Nose Ring
0x00002000 | Earrings
0x00004000 | Mask
0x00008000 | Choker
0x00010000 | Mouth Object
0x00020000 | Body AddOn 1
0x00040000 | Body AddOn 2
0x00080000 | Body AddOn 3

#### General Flag Values

Value | Meaning
-----|--------
0x01 | ??
0x02 | ??
0x04 | ??
0x08 | ??
0x10 | ??
0x20 | Power Armor
0x40 | Non-Playable
0x80 | Heavy
