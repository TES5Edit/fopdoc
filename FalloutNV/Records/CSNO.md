CSNO
====

Casino

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
 | FULL | Name | cstring |
 | DATA | Data | struct |
 | MODL | Casino $1 Chip Model | cstring |
 | MODL | Casino $5 Chip Model | cstring |
 | MODL | Casino $10 Chip Model | cstring |
 | MODL | Casino $25 Chip Model | cstring |
 | MODL | Casino $100 Chip Model | cstring |
 | MODL | Casino $500 Chip Model | cstring |
 | MODL | Casino Roulette Chip Model | cstring |
 | MODL | Slot Machine Model | cstring |
 | MOD2 | Slot Machine Model | cstring | Duplicate?
 | MOD3 | BlackJack Table Model | cstring |
 | MOD4 | Roulette Table Model | cstring |
 | ICON | Slot Reel Texture - Symbol 1 | cstring |
 | ICON | Slot Reel Texture - Symbol 2 | cstring |
 | ICON | Slot Reel Texture - Symbol 3 | cstring |
 | ICON | Slot Reel Texture - Symbol 4 | cstring |
 | ICON | Slot Reel Texture - Symbol 5 | cstring |
 | ICON | Slot Reel Texture - Symbol 6 | cstring |
 | ICON | Slot Reel Texture - Symbol W | cstring |
 | ICO2 | BlackJack Texture - Deck 1 | cstring |
 | ICO2 | BlackJack Texture - Deck 2 | cstring |
 | ICO2 | BlackJack Texture - Deck 3 | cstring |
 | ICO2 | BlackJack Texture - Deck 4 | cstring |

### DATA

Name | Type | Info
-----|------|-----
Decks % Before Shuffle | float32 |
BlackJack Payout Ratio | float32 |
Slot Reel Stop - Symbol 1 | uint32 |
Slot Reel Stop - Symbol 2 | uint32 |
Slot Reel Stop - Symbol 3 | uint32 |
Slot Reel Stop - Symbol 4 | uint32 |
Slot Reel Stop - Symbol 5 | uint32 |
Slot Reel Stop - Symbol 6 | uint32 |
Slot Reel Stop - Symbol W | uint32 |
Number of Decks | uint32 |
Max Winnings | uint32 |
Currency | formid | FormID of a [CHIP](CHIP.md) record.
Casino Winnings Quest | formid | FormID of a [QUST](QUST.md) record.
Flags | uint32 | See values below.

#### Flag Values

Value | Meaning
------|--------
0x00000001 | Dealer Stay on Soft 17
