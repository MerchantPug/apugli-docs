---
title: Action On Harm (Power Type)
date: 2023-04-03
---

# Action On Harm

[Power Type](../power_types.md)

Execute actions for each bit of damage dealt to a target when compared to a specific value.

Type ID: `apugli:action_on_harm`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`damage_condition` | [Damage Condition Type](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, a damage condition that must be met by the damage source of the attack for any actions of this power to be run.
`entity_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | If specified, an entity action that is executed on the power holder each trigger.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, a bi-entity action that is executed with the power holder as the actor and the damaged target as the target each trigger.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, a bi-entity condition that must be met with the power holder as the actor and the damaged target as the target for any actions of this power to be run.
`amount_to_trigger` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The damage amount required for this power to trigger each individual time.
`overflow` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether the power will run the extra actions if a killed entity takes more damage than what was required to kill them.

### Examples

```json
{
    "type": "apugli:action_on_harm",
    "bientity_action": {
        "type": "apoli:actor_action",
        "action": {
            "type": "apoli:exhaust",
            "amount": 0.5
        }
    },
    "amount_to_trigger": 2.0
}
```
This example causes a power holder to exhaust for every 2 damage points it deals to other entities.