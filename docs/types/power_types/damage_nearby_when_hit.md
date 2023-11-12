---
title: Damage Nearby When Hit (Power Type)
date: 2023-11-13
---

# Damage Nearby When Hit

[Power Type](../power_types.md)

Damages other nearby entities with the initial hit's damage upon the power holder being damaged.

Type ID: `apugli:damage_nearby_when_hit`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`damage_condition` | [Damage Condition](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, the damage condition required for this power to act upon damaging an entity.
`source` | [Damage Source](https://origins.readthedocs.io/en/latest/types/data_types/damage_source/) | | The damage source used to deal damage to the nearby entities.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the damage value dealt to the nearby entities.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the damage value dealt to the nearby entities.
`attacker_self_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, this condition must be met with the attacker as the actor and the power holder as the target to apply damage to nearby entities.
`attacker_nearby_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, this condition must be met with the attacker as the actor and an entity that should be damaged by this power as the target to apply damage to that entity.
`self_nearby_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, this condition must be met with the power holder as the actor and an entity that should be damaged by this power as the target to apply damage to that entity.
`radius` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `16.0` | The radius in which this power will act.

### Examples
```json
{
    "type": "apugli:damage_nearby_when_hit",
    "damage_type": "minecraft:fall",
    "damage_condition": {
        "type": "apoli:in_tag",
        "damage_type": "minecraft:is_fall"
    },
    "modifier": {
        "operation": "multiply_total_multiplicative",
        "value": -0.25
    },
    "radius": 6
}
```
This example will damage any entity within a radius of 6 for `minecraft:fall` damage that has 25% of the initial damage value upon having the power holder take fall damage.