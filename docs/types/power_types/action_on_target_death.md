---
title: Action On Target Death (Power Type)
date: 2021-08-11
---

# Action On Target Death

[Power Type](../power_types.md)

Executes an action upon a target's death.

Type ID: `apugli:action_on_target_death`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | *optional* | Determines how the resource is visualized on the HUD.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | | A bi-entity action that applies to the power holder as the actor and the entity that died as the target.
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, a damage condition that must be met for any actions of this power to run.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, a bi-entity condition that must be met for any actions of this power to run.
`includes_prime_adversary` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Whether this power will run if the power holder is the most recent attacker.

### Examples

```json
{
    "type": "apugli:action_on_target_death",
    "bientity_action": {
    "type": "apoli:actor_action",
    "action": {
            "type": "apugli:fire_projectile",
            "entity_type": "minecraft:small_fireball"
        }
    },
    "damage_condition": {
        "type": "apugli:magic"
    },
    "includes_prime_adversary": false
}
```
This example will cause the actor to fire a small fireball upon killing a target with a damage source that is specified as magic and if the target is the direct cause of death.