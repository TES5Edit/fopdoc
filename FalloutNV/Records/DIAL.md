---
layout: falloutnvrec
title: fopdoc
---
DIAL
====

Dialog Topic

## Format

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
+ | EDID | Editor ID | cstring |
-* | | Added Quest | collection |
-* | QSTR | Removed Quest | formid | FormID of a [QUST](QUST.md) record.
-* | | Unused | collection | Probably exists due to an error in the GECK.
+ | FULL | Name | cstring |
+ | PNAM | Priority | float32 |
 | TDUM | ?? | cstring |
+ | DATA | Data | struct |

### Added Quest Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
 | QSTI | Quest | formid | FormID of a [QUST](QUST.md) record.
-* | | Shared Info | collection |

#### Shared Info Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
 | INFC | Info Connection | formid | FormID of an [INFO](INFO.md) record.
 | INFX | Info Index | int32 |

### Unused Subrecord Collection

Count | Subrecord | Name | Type | Info
------|-----------|------|------|-----
 | INFC | ?? | ?? |
 | INFX | ?? | ?? |

### DATA

Name | Type | Info
-----|------|-----
Type | uint8 | Enum - see below for values.
Flags | uint8 | See below for values.

#### Type Enum Values

Value | Meaning
------|--------
0 | Topic
1 | Conversation
2 | Combat
3 | Persuasion
4 | Detection
5 | Service
6 | Miscellaneous
7 | Radio

#### Flag Values

Value | Meaning
------|--------
0x01 | Rumors
0x02 | Top-Level

