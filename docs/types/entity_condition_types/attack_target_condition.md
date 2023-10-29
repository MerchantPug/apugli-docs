---
title: Attack Target Condition (Entity Condition Type)
date: 2023-02-08
---

# Attack Target Condition

[Entity Condition Type](../entity_condition_types.md).

Applies a bi-entity condition check with an entity as the actor and the attack target of that entity as the target.

Type ID: `apugli:attack_target_condition`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | | The bi-entity condition to test for with the entity as the actor and its attack target as the target.

### Example
```json
"condition": {
    "type": "apugli:attack_target_condition",
    "bientity_condition": {
         "type": "apoli:attacker"
    }
}
```
This example tests if an entity's attacker is their attack target.
