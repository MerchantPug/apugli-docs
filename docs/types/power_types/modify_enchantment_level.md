---
title: Modify Enchantment Level (Power Type)
date: 2022-02-18
---

# Modify Enchantment Level

[Power Type](../power_types.md)

Modifies the entity's enchantment levels.

Type ID: `apugli:modify_enchantment_level`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`enchantment` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The enchantment to apply to the entity.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the entity's.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the entity's amount of Soul Speed.

### Examples

```json
{
    "type": "apugli:modify_enchantment_level",
    "enchantment": "minecraft:fortune",
    "modifiers": [
        {
            "operation": "addition",
            "value": 1
        },
        {
            "operation": "multiply_total",
            "value": 2
        }
    ]
}
```

This example gives the entity 1 level of Fortune and then multiplies this new value by 2.
