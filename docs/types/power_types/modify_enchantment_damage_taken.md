---
title: Modify Enchantment Damage Taken (Power Type)
date: 2022-03-05
---

# Modify Enchantment Damage Taken

[Power Type](../power_types.md).

Modifies how much melee damage the entity that has the power takes based on how many levels of enchantments the attacker has.

Type ID: `apugli:modify_enchantment_damage_taken`

### Fields
Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The enchantment required to activate this power.
`base_value` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The base value of the extra damage.
`damage_condition` | [Damage Condition Type](https://origins.readthedocs.io/en/latest/types/damage_condition_types/) | *optional* | If specified, the specified base value with the modifier(s) applied and/or action(s) will only apply if the taken damage fulfills this condition.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If specified, the specified modifier(s) and/or action(s) will only apply if either or both 'actor' (the attacker) and 'target' (the entity that has the power) fulfills this bi-entity condition type.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the base value. Modifiers will be applied as many times as the enchantment level the attacker has of the specified enchantment.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the base value. Modifiers will be applied as many times as the enchantment level the attacker has of the specified enchantment.
`bientity_action` | [Bi-entity Action Type](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If specified, this bi-entity action type will be executed on either or both 'actor' (the attacker) and 'target' (the entity that has the power).

### Example
```json
{
    "type": "apugli:modify_enchantment_damage_taken",
    "enchantment": "minecraft:smite",
    "base_value": 1.5,
    "modifier": {
        "operation": "addition",
        "value": 2.5
    }
}
```
This example will make the power holder take `1.5 + (enchantment_level * 2.5)` extra damage when hit by a weapon with the Smite enchantment.