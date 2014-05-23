# Embedded Script Field Collection


## Format

Count | Field | Name | Type | Info
------|-------|------|------|-----
+ | [SCHR](#schr) | Basic Script Data | struct | Patrol data, embedded script.
+ | SCDA | Compiled Embedded Script Source | uint8[] | Patrol data, embedded script.
+ | SCTX | Embedded Script Source | char[] | Patrol data, embedded script.
-* | | [Local Variables](#local-variables-field-collection) | | This is a field collection.
-* | SCRO | Reference | formid *or* uint32 | Patrol data, embedded script. A FormID or local variable reference.
