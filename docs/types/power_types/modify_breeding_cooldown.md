---
title: Modify Breeding Cooldown (Power Type)
date: 2022-02-06
---

# Modify Breeding Cooldown

[Power Type](../power_types.md)

Modifies the breeding cooldown for entities bred by the power holder.

Type ID: `apugli:modify_breeding_cooldown`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the cooldown that entities have before they may breed again.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the cooldown that entities have before they may breed again.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, the bi-entity condition(s) that must be met with the power holder as the actor and the breedable entity as the target.


### Examples

```json
{
    "type": "apugli:modify_breeding_cooldown",
    "modifier": {
        "operation": "multiply_total_multiplicative",
        "value": 2
    },
    "bientity_condition": {
       "type": "apoli:owner",
       "inverted": true
    }
}
```
This power doubles the breeding cooldown for entities if they aren't owned by the power holder.