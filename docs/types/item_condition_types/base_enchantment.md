---
title: Base Enchantment (Item Condition Type)
date: 2023-06-07
---

# Base Enchantment

[Item Condition Type](../item_condition_types.md).

Checks the level of an enchantment on an item based purely on item nbt.

Type ID: `apugli:base_enchantment`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the enchantment of interest, e.g. `minecraft:protection`.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | `">="` | How to compare the enchantment level to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The value to compare the enchantment level against.

### Example
```json
"condition": {
    "type": "apugli:base_enchantment",
    "enchantment": "minecraft:fortune",
    "calculation": "max",
    "comparison": ">=",
    "compare_to": 3
}
```
This example checks if the item has a Fortune level of III or higher based on nbt alone. This does not count the `apugli:modify_enchantment_level` power or any other non nbt enchantment level modifications.