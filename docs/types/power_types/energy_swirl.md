---
title: Energy Swirl (Power Type)
date: 2021-08-19
---

# Energy Swirl

[Power Type](../power_types.md).

Creates a translucent energy swirl around an entity (Similar to a Charged Creeper or a Wither on 50% health or less).

Type ID: `apugli:energy_swirl`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`texture_location` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) |  | The texture used for the energy swirl overlay.
`speed` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) |  | The speed at which the overlay swirls around the player. You can set this to 0 if you want a static overlay.


### Example
```json
{
    "type": "apugli:energy_swirl",
    "texture_location": "minecraft:textures/entity/wither/wither_armor.png",
    "speed": 0.01,
    "condition": {
        "type": "origins:relative_health",
        "comparison": "<=",
        "compare_to": 0.5
    }
}
```
This power will render the Wither Armor overlay at 0.01 speed (Charged Creeper overlay speed) when the player's health is 50% or less.