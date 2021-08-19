---
title: Item Attribute (Power Type)
date: 2021-08-19
---

# Item Attribute

[Power Type](../power_types.md).

Adds an additional attribute modifier to item stacks. These attributes also show up in the description of the item.

Type ID: `apugli:item_attribute`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/item_conditions/) | | The item condition that items must satisfy to be affected by this power.
`modifier` | [Attributed Attribute Modifier](https://origins.readthedocs.io/en/latest/data_types/attributed_attribute_modifier/) | *optional* | If specified, this modifier will be applied to its corresponding attribute.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/data_types/array/) of [Attributed Attribute Modifiers](https://origins.readthedocs.io/en/latest/data_types/attributed_attribute_modifier/)	|*optional* | If specified, these modifiers will be applied to their corresponding attributes.

### Example
```json
{
  "type": "apugli:item_attribute",
  "item_condition": {
    "type": "apoli:ingredient",
    "ingredient": {
        "tag": "miner:pickaxes"
    }
  },
  "modifier": {
        "attribute": "minecraft:generic.attack_damage",
        "operation": "addition",
        "value": 2
    }
}
```
This example adds 2 extra attack damage to any item that is in the `miner:pickaxes` tag.