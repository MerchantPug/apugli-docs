---
title: Particle in Radius (Entity Condition)
date: 2021-03-05
---

# Particle In Radius

[Entity Condition](../entity_condition_types.md).

Checks whether the player has a specified number of particles that match a specified particle effect(s) in a specified radius. The radius originates at the center of the entity with this condition.

Type ID: `apugli:particle_in_radius`

!!! caution

    This condition is only effective client-side. That means any server-sided power types will not work as intended.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`particle` | [Particle Effect](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | *optional* | The particle effect to match with the checked particles.
`particles` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Particle Effects](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | *optional* | The particle effects to match with the checked particles.
`radius` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The radius to check the particles that match the specified particle effect within.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)	| `">="` | How the amount of particles within the specified radius which are the specified should be compared to the specified value.
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