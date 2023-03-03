---
title: Energy Swirl (Power Type)
date: 2021-08-19
---

# Energy Swirl

[Power Type](../power_types.md).

Creates a translucent energy swirl around an entity (Similar to a Charged Creeper or a Wither on 50% health or less).

Type ID: `apugli:energy_swirl`

!!! note
    Any `texture_url` specified files have a size limit of 1MB. You are able to change this through the Apugli config.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`texture_location` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, the texture used for the energy swirl overlay.
`texture_url` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | If specified, the url to a .png file imported into the game as a texture for this power's use. This will be used as a fallback if `texture_location` is not specified or if a texture is not present.
`size` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The scale relative to the entity at which the energy swirl will render at.
`speed` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.01` | The speed at which the overlay swirls around the player. You can set this to 0 if you want a static overlay.


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