---
title: Entity in Radius (Entity Condition)
date: 2021-08-19
---

# Entity in Radius

[Entity Condition](../entity_conditions.md).

Checks whether the player has a specified number of entities that match a specified entity condition in a specified radius. The radius originates at the center of the entity with this condition.

Type ID: `apugli:entity_in_radius`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` |	[Entity Condition](https://origins.readthedocs.io/en/latest/entity_conditions/) | | The block condition which is applied to the block at the player's feet.
`radius` | [Float](https://origins.readthedocs.io/en/latest/data_types/float/) | | The radius to check blocks in.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/data_types/comparison/)	| `">="` | How the number of blocks in the radius which fulfill block_condition should be compared to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | `1` | The value to compare the number to.

### Example
```json
"condition": {
  "type": "apugli:entity_in_radius",
  "condition": {
    "type": "apoli:entity_type",
    "entity_type": "minecraft:creeper"
  },
  "radius": 5.0,
  "comparison": ">=",
  "compare_to": 1
}
```
This condition checks whether the entity is near at least one creeper within 5x the size of their hurtbox.