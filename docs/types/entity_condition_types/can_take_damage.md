---
title: Can Take Damage (Entity Condition Type)
date: 2023-02-08
---

# Can Take Damage

[Entity Condition Type](../entity_condition_types.md).

Checks for if the entity is immune to a damage source.

Type ID: `apugli:can_take_damage`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`source` | [Damage Source](https://origins.readthedocs.io/en/latest/types/data_types/damage_source/) | | The damage source to be tested by this condition.

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
