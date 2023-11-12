---
title: Damage Nearby On Hit (Power Type)
date: 2023-11-13
---

# Damage Nearby On Hit

[Power Type](../power_types.md)

Damages other nearby entities with the initial hit's damage upon damaging a target.

Type ID: `apugli:damage_nearby_on_hit`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, the damage condition required for this power to act upon damaging an entity.
`damage_type` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | 
`source` | [Damage Source](https://origins.readthedocs.io/en/latest/types/data_types/damage_source/) | | The damage source used to deal damage to the nearby entities.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the damage value dealt to the nearby entities.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the damage value dealt to the nearby entities.
`self_target_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, this condition must be met with the power holder as the actor and the initial attack target as the target to apply damage to nearby entities.
`self_nearby_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, this condition must be met with the power holder as the actor and an entity that should be damaged by this power as the target to apply damage to that entity.
`target_nearby_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, this condition must be met with the initial attack target as the actor and an entity that should be damaged by this power as the target to apply damage to that entity.
`radius` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `16.0` | The radius in which this power will act.

### Examples
```json
{
    "type": "apugli:damage_nearby_on_hit",
    "damage_type": "minecraft:on_fire",
    "modifier": {
        "operation": "multiply_total_multiplicative",
        "value": -0.5
    },
    "self_target_bientity_condition": {
        "type": "apoli:target_condition",
        "condition": {
            "type": "origins:on_fire"
        }
    },
    "radius": 6
}
```
This example will damage any entity within a radius of 6 for `minecraft:on_fire` damage that has 50% of the initial damage value provided the initial attack target is on fire.