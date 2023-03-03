---
title: Action When Harmed (Power Type)
date: 2023-04-03
---

# Action When Harmed

[Power Type](../power_types.md)

Execute actions for each bit of damage received from an attacker when compared to a specific value.

Type ID: `apugli:action_when_harmed`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`damage_condition` | [Damage Condition Type](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, a damage condition that must be met by the damage source of the attack for any actions of this power to be run.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, a bi-entity action that is executed with the attacker as the actor and the power holder as the target.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, a bi-entity condition that must be met with the attacker as the actor and the power holder as the target for any actions of this power to be run.
`amount_to_trigger` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The damage amount required for this power to trigger each individual time.
`overflow` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether the power will run the extra actions if the power holder dies and takes more damage than what was required to kill them.

### Examples

```json
{
    "type": "apugli:action_when_harmed",
    "bientity_action": {
        "type": "origins:invert",
        "action": {
            "type": "apoli:damage",
            "amount": 2,
            "source": {
                "name": "thorns",
                "magic": true
            }
        }
    },
    "amount_to_trigger": 4.0
}
```
This example causes a power holder to exhaust for every 4 damage points it deals to other entities.