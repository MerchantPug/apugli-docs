---
title: Entity In Radius (Entity Condition Type)
date: 2021-08-19
---

# Entity In Radius

[Entity Condition Type](../entity_condition_types.md).

Checks whether the player has a specified number of entities that match a specified entity condition in a specified radius. The radius originates at the center of the entity with this condition.

Type ID: `apugli:entity_in_radius`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`condition` |	[Entity Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | The entity condition type to check for.
`bientity_condition` |	[Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | The bi-entity condition type to check for with the entity with this condition as the actor and the entities in the radius as the targets.
`radius` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The radius to check the entities that fulfill the specified entity condition type within.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)	| `">="` | How the amount of entities within the specified radius which fulfills the specified entity/bi-entity condition type(s) should be compared to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The value to compare the amount to.

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