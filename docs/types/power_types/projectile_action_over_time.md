---
title: Action On Projectile Hit (Power Type)
date: 2023-02-04
---

# Projectile Action Over Time

[Power Type](../power_types.md)

Execute actions upon landing a projectile on a target.

Type ID: `apugli:projectile_action_over_time`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`interval` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `20` | The interval at which the power's action(s) trigger.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | A bi-entity action that is run with the power holder as the actor and the projectile as the target each interval.
`rising_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | A bi-entity action that is run with the power holder as the actor and the projectile as the target as soon as the power's bi-entity condition becomes true.
`falling_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | A bi-entity action that is run with the power holder as the actor and the projectile as the target as soon as the power's bi-entity condition becomes false.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | A bi-entity condition that must be met with the power holder as the actor and the projectile as the target for this power to be run.

### Examples

```json
{
    "type": "apugli:projectile_action_over_time",
    "bientity_action": {
        "type": "origins:add_velocity",
        "z": 0.1
    },
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "apoli:in_tag",
            "tag": "minecraft:arrows"
        }
    }
}
```
This example will push any arrows that the power holder shot away from them.