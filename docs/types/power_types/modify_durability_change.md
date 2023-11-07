---
title: Modify Durability Change (Power Type)
date: 2022-11-08
---

# Modify Durability Change

[Power Type](../power_types.md).



Type ID: `apugli:modify_durability_change`

### Fields
Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition](../item_condition_types.md) | *optional* | If set, any item that has a change in durability must meet this condition for this power to come into effect.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | *optional* | How the item's damage value should be compared. 
`compare_to` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `-2147483648` | The value that the item's damage value must be compared to the comparison for this power to come into effect.
`comparisons` | [Comparison Map](../data_types/comparison_map.md) with [Floats](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | If set, values and comparisons that the item's damage value must be compared to for this power to come into effect.
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to any time that an item meets the item condition's has a change in durability.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to any time that an item meets the item condition's has a change in durability.

### Example
```json
{
    "type": "apugli:modify_durability_change",
    "comparisons": [
        {
            "comparison": ">=",
            "compare_to": 1,
        },
        {
            "comparison": "<=",
            "compare_to": 100
        }
    ],
    "modifier": {
        "operation": "set_total",
        "value": 2
    }
}
```
This example will make all items lose 2 durability upon having any change in durability whilst the item's damage value is between 1 and 100 (inclusive).