---
title: Action On Tame Hit (Power Type)
date: 2021-08-11
---

# Action On Tame Hit

[Power Type](../power_types.md).

Runs an action when an owner's `TameableEntity` harms a target.

Type ID: `apugli:action_on_tame_hit`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, a bi-entity action that applies to the tame as the actor and the harmed target as the target.
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, a damage condition that must be met for any actions of this power to run.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, a bi-entity condition that must be met with the tame as the actor and the harmed target as the target for any actions of this power to run.
`owner_bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, a bi-entity action that applies to the owner as the actor and the harmed target as the target.
`owner_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, a bi-entity condition that must be met with the owner as the actor and the harmed target as the target for any actions of this power to run.

### Example
```json
{
    "type": "apugli:action_on_tame_hit",
    "bientity_action": {
        "type": "apoli:mount"
    }
}
```
This example will cause the tamed entity to mount the target entity whenever the target is harmed by the tame.