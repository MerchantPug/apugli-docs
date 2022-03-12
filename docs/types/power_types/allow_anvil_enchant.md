---
title: Allow Anvil Enchant (Power Type)
date: 2022-03-12
---

# Allow Anvil Enchant

[Power Type](../power_types.md)

Allows a `PlayerEntity` to enchant an item with specified enchants that may not have been accessible to an item before.

Type ID: `apugli:allow_anvil_enchant`

### Fields
Field | Type | Default | Description
------|------|---------|------------
`enchantment` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If set, this will determine a new enchantment that can be put on an item that meets conditions.
`enchantment` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If set, this will determine the new enchantments that can be put on an item that meets conditions.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `0` | The enchantment level of the item in the middle slot of the anvil to check for.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)	| `">="` | The comparison applied the the enchantment level of the item in the middle. If this comparison isn't met, you are unable to enchant the item.
`item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/types/item_condition_types/) | | The item condition that an item must meet to be able to be enchanted through this power.

### Example
```json
{
    "type": "apugli:allow_anvil_enchant",
    "enchantments": [
        "minecraft:sharpness",
        "minecraft:smite",
        "minecraft:bane_of_arthropods"
    ],
    "item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:netherite_hoe"
        }
    }
}
```
This power allows the three sword/axe damage enchants to be put on a netherite hoe.