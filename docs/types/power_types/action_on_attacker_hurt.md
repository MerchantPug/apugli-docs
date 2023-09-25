---
title: Action On Attacker Hurt (Power Type)
date: 2021-02-06
---

# Action On Attacker Hurt

[Power Type](../power_types.md)

Executes a bi-entity action upon an entity's most recent attacker getting hurt.

Type ID: `apugli:action_on_attacker_hurt`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | | The bi-entity action to run with the power holder as the actor and that entity's most recent attacker as the target.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, the bi-entity condition that must be met with the power holder as the actor and that entity's most recent attacker as the target for the action to run.
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If set, the damage condition that must be met by the source and amount of the damage dealt to the power holder's most recent attacker.


### Examples

```json
{
    "type": "apugli:action_on_attacker_hurt",
    "bientity_action": {
        "type": "apoli:heal",
        "amount": 6
    },
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:entity_type",
            "entity_type": "minecraft:player"
        }
    }
}
```
This example heals the entity each time their most recent attacker is hurt if they're a player.