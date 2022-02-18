---
title: Force Particle Render (Power Types)
date: 2022-02-18
---

# Force Particle Render

[Power Type](../power_types.md)

Forces one or multiple particles to render for the player, regardless of their "Particle Settings".

Type ID: `apugli:force_particle_render`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`particle` | [Particle Effect](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | *optional* | If specified, the specified particle will be forced to render for the player.
`particles` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Particle Effects](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | *optional* | If specified, the specified particles will be forced to render for the player.


### Examples

```json
{
    "type": "apugli:force_particle_render",
    "particles": [
        "minecraft:large_smoke",
        "minecraft:campfire_cosy_smoke",
        "minecraft:campfire_signal_smoke"
    ]
}
```

This example will force the `minecraft:large_smoke`, `minecraft:campfire_cosy_smoke` and `minecraft:campfire_signal_smoke` particles to render for the player.
