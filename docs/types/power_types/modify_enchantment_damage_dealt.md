---
title: Modify Enchantment Damage Dealt (Power Type)
date: 2022-03-05
---

# Modify Enchantment Damage Dealt

[Power Type](../power_types.md).

Modifies how much melee damage the entity that has the power deals based on how many levels of enchantments the entity has.

Type ID: `apugli:modify_enchantment_damage_dealt`

### Fields
Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The enchantment required to activate this power.
`base_value` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The base value of the extra damage.
`damage_condition` | [Damage Condition Type](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, the specified base value with the modifier(s) applied and/or action(s) will only apply if the dealt damage fulfills this condition.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, the specified base value with the modifier(s) applied and/or action(s) will only apply if either or both 'actor' (the entity that has the power) and 'target' (the entity that has been hit) fulfills this bi-entity condition type.
`target_condition` | [Entity Condition Type](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | If specified, the specified base value with the modifier(s) applied and/or action(s) will only be applied if the entity/entities that has been hit fulfills this condition.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the base value. Modifiers will be applied as many times as `enchantment_level - 1` the power holder has of the specified enchantment.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the base value. Modifiers will be applied as many times as `enchantment_level - 1` the power holder has of the specified enchantment.
`bientity_action` | [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, this bi-entity action type will be executed on either or both 'actor' (the entity that has the power) and 'target' (the entity that has been hit).

### Example
```json
{
  "type": "apugli:modify_enchantment_damage_dealt",
  "enchantment": "minecraft:sharpness",
  "base_value": 2.5,
  "modifier": {
        "operation": "multiply_base",
        "value": 2
    }
}
```
This example will make target entities take `2.5 * (enchantment_level * 2)` extra damage when hit by a weapon with the Sharpness enchantment.