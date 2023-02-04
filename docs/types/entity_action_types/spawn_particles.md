---
title: Spawn Particles (Entity Action Type)
date: 2023-02-04
---

# Spawn Particles

[Entity Action Type](../entity_action_types.md).

Spawns particles on the body of the entity that has the power for visual effects.

Type ID: `apugli:spawn_particles`

### Fields
Field | Type | Default | Description
------|------|---------|------------
`particle` | [Particle Effect](../data_types/particle_effect.md) | | The particle type that will be spawned.
`count` | [Integer](../data_types/integer.md) | | How much of the specified particle type will be spawned.
`speed` | [Float](../data_types/float.md) | `0.0` | Determines the speed of the specified particle type.
`force` | [Boolean](../data_types/boolean.md) | `false` | If set to `true`, the specified particle type that will be spawned can be seen from a far distance.
`velocity` | [Vector](../data_types/vector.md) | *optional* | If set, determines the velocity of the particle. Overrides the `speed` field if set.
`spread` | [Vector](../data_types/vector.md) | `{"x": 0.5, "y": 0.25, "z": 0.5}` | Determines the size of the three-dimensional cuboid volume to spawn the specified particle type in.
`offset_y` | [Float](../data_types/float.md) | `0.5` | The offset of where the particle will be centered in the Y axis.


### Examples

```json
"entity_action": {
    "type": "toomanyorigins:spawn_particles",
    "particle": {
        "type": "minecraft:entity_effect"
    },
    "count": 1,
    "spread": {
        "x": 0.5,
        "y": 1.0,
        "z": 0.5
    },
    "velocity": {
        "x": 0.207843137,
        "y": 0.16470588235,
        "z": 0.15294117647
    }
}
```
This example will spawn a particle cuboid that is about 1x2x1 in size that will use the entity effect texture with a velocity that changes its color to be that of the Wither effect `(53/255, 42/255, 39/255)`. Note that some effects such as this one use the velocity field as a color field, whereas others don't.