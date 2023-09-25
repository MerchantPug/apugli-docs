---
title: Action On Attacker Hurt (Power Type)
date: 2021-02-06
---

# Action On Attacker Hurt

[Power Type](../power_types.md)

Executes a bi-entity action upon an entity's current target getting hurt.

Type ID: `apugli:action_on_attacker_hurt`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | | The bi-entity action to run with the power holder as the actor and that entity's current target as the target.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, the bi-entity condition that must be met with the power holder as the actor and that entity's current target as the target for the action to run.
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If set, the damage condition that must be met by the source and amount of the damage dealt to the power holder's attacker.


### Examples

```json
{
    "type": "toomanyorigins:action_on_target_hurt",
    "bientity_action": {
        "type": "origins:actor_action",
        "action": {
            "type": "origins:feed",
            "food": 1,
            "saturation": 2.4
        }
    },
    "damage_condition": {
        "type": "origins:or",
        "conditions": [
            {
              "type": "origins:name",
              "name": "wither"
            },
            {
              "type": "origins:name",
              "name": "wither.player"
            }
        ]
    }
}
```
This example feeds the player upon having their current target take damage from damage sources named `wither` or `wither.player`.
