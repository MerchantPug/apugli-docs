---
title: Can Have Effect (Entity Condition)
date: 2021-08-03
---

# Can Have Effect

[Entity Condition](../entity_condition_types.md).

Checks whether the entity isn't immune to the specified status effect.

Type ID: `apugli:can_have_effect`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) |  | ID of the status effect the condition should check.

### Example
```json
"condition": {
  "type": "apugli:can_have_effect",
  "effect": "minecraft:wither",
  "inverted": true
}
```
This example checks if the entity is immune to the wither effect.