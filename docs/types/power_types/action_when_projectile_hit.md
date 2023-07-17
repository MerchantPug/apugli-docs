---
title: Action When Projectile Hit (Power Type)
date: 2023-02-04
---

# Action On Projectile Hit

[Power Type](../power_types.md)

Execute actions upon having a projectile land on the power holder.

Type ID: `apugli:action_on_projectile_hit`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`bientity_action` | [Bi-entity Action](../bientity_action_types.md) | *optional* | If specified, a bi-entity action that applies to the projectile owner as the actor and the power holder as the target as the target.
`bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If specified, a bi-entity condition that must be met with the projectile owner as the actor and the power holder as the target for any actions of this power to run.
`owner_bientity_action` | [Bi-entity Action](../bientity_action_types.md) | *optional* | If specified, a bi-entity action that must be met with the projectile owner as the actor and the power holder as the target for any actions of this power to run.
`owner_bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If specified, a bi-entity condition that must be met with the projectile owner as the actor and the power holder as the target as the target for any actions of this power to run.

### Examples
```json
{
    "type": "apugli:action_on_projectile_hit",
    "owner_bientity_action": {
        "type": "apoli:set_on_fire",
        "duration": 5
    },
    "bientity_condition": {
        "type": "apoli:actor_condition",
        "condition": {
            "type": "apoli:on_fire"
        }
    }
}
```
This power sets an entity on fire for 5 seconds each time they are hit by a projectile from a burning entity. 