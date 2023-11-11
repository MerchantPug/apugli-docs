---
title: Action On Jump (Power Type)
date: 2023-02-04
---

# Action On Jump

[Power Type](../power_types.md)

Execute an entity action upon the power holder jumping.

Type ID: `apugli:action_on_jump`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`entity_action` | [Bi-entity Action](../bientity_action_types.md) | | The entity action to execute on the power holder whenever they jump.

### Examples

```json
{
    "type": "apugli:action_on_jump",
    "entity_action": {
        "type": "apoli:spawn_particles",
        "particle": "minecraft:happy_villager",
        "count": 6,
        "speed": 1.0,
        "spread": {
            "x": 1.0,
            "y": 0.0,
            "z": 1.0
        }
    }
}
```
This example will spawn 6 happy villager particles with a speed of 1 and a x and z spread of 1 whenever the power holder jumps.