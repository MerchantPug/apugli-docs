---
title: Action When Lightning Struck (Power Type)
date: 2023-11-11
---

# Action When Lightning Struck

[Power Type](../power_types.md)

Execute an entity action when the power holder is struck by lightning.

Type ID: `apugli:action_when_lightning_struck`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`bientity_condition` | [Bi-entity Action](../bientity_action_types.md) | | The bi-entity condition that must be met with the entity as the actor and the lightning bolt as the target for any actions of this power to run
`entity_action` | [Bi-entity Action](../bientity_action_types.md) | | The entity action to execute on the power holder whenever they are struck by lightning.

### Examples

```json
{
    "type": "apugli:action_when_lightning_struck",
    "bientity_condition": {
        "type": "apoli:actor_condition",
        "condition": {
            "type": "apoli:or",
            "axes": [
                "y"
            ],
            "compare_to": 0,
            "comparison": "<"
        }
    },
    "entity_action": {
        "type": "apoli:add_velocity",
        "y": 2
    }
}
```
This example will launch the entity up in the air at a velocity of 2 if they have a y velocity lower than 0 whilst being hit by a lightning bolt.