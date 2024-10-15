---
title: Prevent Entity Selection (Power Type)
date: 2023-11-11
---

# Prevent Entity Selection

[Power Type](../power_types.md).

Prevents a player from selecting an entity with their crosshair, ignoring the entity when looking at them.

Type ID: `apugli:prevent_entity_selection`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_condition` | [Entity Condition Type](https://origins.readthedocs.io/en/latest/types/entity_condition_types) | *optional* | If specified, only entities that fulfills this entity condition type will **not** be able to be selected by players with this power.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types) | *optional* | If specified, only entities which fulfills this bi-entity condition type in relation to the entity that has the power will **not** be able to be selected by players with this power.

### Example
```json
{
    "type": "apugli:prevent_entity_selection",
    "bientity_condition": {
        "type": "origins:owner"
    }
}
```
This example prevents the player from selecting their tames, which in turn does not allow the player to attack them.