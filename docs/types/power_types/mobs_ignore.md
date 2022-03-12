---
title: Mobs Ignore (Power Type)
date: 2021-10-08
---

# Mobs Ignore

[Power Type](../power_types.md)

Makes hostile mobs ignore the player.

Type ID: `apugli:mobs_ignore`

### Fields
Field | Type | Default | Description
------|------|---------|------------
`mob_condition` | [Entity Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | If set, this will determine what entity condition the entity must meet in order to be effected by this power.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, this will determine what bi-entity condition the entity must meet in order to be effected by this power.

### Example
```json
{
    "type": "apugli:mobs_ignore",
    "mob_condition": {
        "type": "apoli:entity_type",
        "entity_type": "minecraft:skeleton"
    }
}
```
This power causes skeletons to ignore the player.