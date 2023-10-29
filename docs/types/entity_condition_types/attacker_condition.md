---
title: Attacker Condition (Entity Condition Type)
date: 2023-02-08
---

# Attacker Condition

[Entity Condition Type](../entity_condition_types.md).

Applies a bi-entity condition check with an entity as the actor and the attacker of that entity as the target.

Type ID: `apugli:attacker_condition`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | | The bi-entity condition to test for with the entity as the actor and its attacker as the target.

### Example
```json
"condition": {
    "type": "apugli:attacker_condition",
    "bientity_condition": {
        "type": "apoli:relative_rotation",
        "actor_rotation": "head",
        "target_rotation": "body",
        "comparison": ">=",
        "compare_to": -0.8
    }
}
```
This example tests if an entity's attacker is essentially facing the entity.
