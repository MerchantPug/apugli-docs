---
title: Apugli Entity Group (Entity Condition)
date: 2021-06-20
---

# Apugli Entity Group

[Entity Condition](../entity_conditions.md).

Checks whether a player is nearby a specified amount of entities.

Type ID: `apugli:nearby_entities`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](https://origins.readthedocs.io/en/latest/block_conditions/) |  | The block condition which is applied to the block the player is looking at.

### Example
```json
"condition": {
  "type": "apugli:nearby_entities",
  "entity_type": "minecraft:creeper",
  "player_box_multiplier": 5.0,
  "comparison": ">=",
  "compare_to": 1
}
```
This condition checks whether the entity is near at least one creeper within 5x the size of their hurtbox.