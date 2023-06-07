---
title: Status Effect Tag (Entity Condition Type)
date: 2023-06-07
---

# Status Effect Tag

[Entity Condition Type](../entity_condition_types.md).

Checks whether an entity has any of the effects within a status effect tag with a specified amplifier and/or duration.

Type ID: `apugli:status_effect_tag`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`tag` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the tag to check for.
`min_amplifier` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `0` | The minimum amplifier the status effect should have in order to pass the check.
`max_amplifier` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `2147483647` | The maximum amplifier the status effect should have in order to pass the check.
`min_duration` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `0` | The minimum duration in ticks the status effect should have left in order to pass the check.
`max_duration` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `2147483647` | The maximum duration in ticks the status effect should have left in order to pass the check.

### Example
```json
"condition": {
    "type": "apugli:status_effect_tag",
    "tag": "apugli:charged_effects",
    "max_amplifier": 0
}
```
This condition checks if the entity has any status effect contained within the `apugli:charged_effects` mob effect tag and if that effect has an amplifier of 0 (level 1).