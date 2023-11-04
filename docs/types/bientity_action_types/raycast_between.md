---
title: Raycast Between (Bi-entity Action Type)
date: 2021-06-20
---

# Raycast Between

[Bi-entity Action Type](../bientity_action_types.md).

Raycasts to the target entity from the actor entity.

Type ID: `apugli:raycast_between`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_action` | [Block Action](../entity_action_types.md) | *optional* | If set, the block action to be executed on blocks targeted by this raycast.
`block_condition` | [Block Condition](../block_condition_types.md) | *optional* | If set, the block condition that must be met by any block that is targeted in order to do actions on it.
`particle` | [Particle Effect](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | | The particle effect that is displayed on the ray.
`spacing` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.5` | If there is a particle effect, the spacing between the particles displayed on the ray.

### Example
```json
"bientity_action": {
    "type": "apugli:raycast_between",
    "particle": "minecraft:dragon_breath"
}
```
This example is a visual raycast with the `minecraft:dragon_breath` particle type from the actor to the target.