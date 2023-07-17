---
title: Action When Tame Hit (Power Type)
date: 2022-03-05
---

# Action When Tame Hit

[Power Type](../power_types.md).

Runs an action when an owner's `TameableEntity` gets harmed by another entity.

Type ID: `apugli:action_when_tame_hit`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the entity has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`bientity_action` | [Bi-entity Action](../bientity_action_types.md) | *optional* | If specified, a bi-entity action that applies to the attacker as the actor and the tame as the target.
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, a damage condition that must be met for any actions of this power to run.
`bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If specified, a bi-entity condition that must be met with the attacker as the actor and tame as the target for any actions of this power to run.
`owner_bientity_action` | [Bi-entity Action](../bientity_action_types.md) | *optional* | If specified, a bi-entity action that must be met with the attacker as the actor and the owner as the target.
`owner_bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If specified, a bi-entity condition that must be met with the attacker as the actor and the owner as the target for any actions of this power to run.

### Example
```json
{
    "type": "apugli:action_when_tame_hit",
    "owner_bientity_action": {
        "type": "origins:add_velocity",
        "z": 2
    }
}
```
This example will push the owner away from any tame's attacker whenever it is hit.