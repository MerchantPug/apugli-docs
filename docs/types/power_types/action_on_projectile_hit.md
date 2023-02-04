---
title: Action On Bonemeal (Power Type)
date: 2023-02-04
---

# Action On Bonemeal

[Power Type](../power_types.md)

Execute actions upon landing a projectile on a target.

Type ID: `apugli:action_on_projectile_hit`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, a bi-entity action that applies to the projectile as the actor and the harmed target as the target.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, a bi-entity condition that must be met with the projectile as the actor and the harmed target as the target for any actions of this power to run.
`owner_bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, a bi-entity action that must be met with the owner as the actor and the harmed target as the target.
`owner_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, a bi-entity condition that must be met with the owner as the actor and the harmed target as the target for any actions of this power to run.

### Examples

```json
{
    "type": "apugli:action_on_projectile_hit",
    "owner_bientity_action": {
        "type": "origins:set_in_love"
    },
    "bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "compare_to": 10.0,
            "type": "apugli:max_health",
            "comparison": ">="
        }
    }
}
```
This example sets an entity in love if hit with any projectile as long as the entity's generic max health attribute is 10 or above.