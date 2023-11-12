---
title: Can Take Damage (Entity Condition Type)
date: 2023-02-08
---

# Can Take Damage

[Entity Condition Type](../entity_condition_types.md).

Checks if the entity is immune to a damage source.

Type ID: `apugli:can_take_damage`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`damage_type` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The damage type to be tested by this condition.
`source` | [Damage Source](https://origins.readthedocs.io/en/latest/types/data_types/damage_source/) | **DEPRECATED** | Use `damage_type` instead. [More information here.](https://gist.github.com/apace100/bfbf82a8f9d6bd2db13e4feaf653a6b0)

### Example
```json
"condition": {
    "type": "apugli:can_take_damage",
    "source": {
        "name": "lava"
    }
}
```
This example tests if an entity can take damage from a damage source named `lava`.
