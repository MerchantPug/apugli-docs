---
title: Edible Item (Power Type)
date: 2021-08-19
---

# Edible Item

[Power Type](../power_types.md).

A power that makes any item that matches an item condition edible.

Type ID: `apugli:edible_item`

!!! NOTE
    The actual food saturation level is determined by the `food * saturation * 2` formula.

!!! NOTE
    This power type will only work on players.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/types/item_condition_types/) |  | The item condition that items must satisfy to be affected by this power.
`food_component` | [Food Component](../data_types/food_component.md) | | The food component that the item grants upon eating it.
`use_action` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | The action to associate with the player. One of `eat` or `drink`. Defaults to eat when null.
`return_stack` | [Item Stack](https://origins.readthedocs.io/en/latest/types/data_types/item_stack/) | *optional* | The item stack to replace the item with upon consumption.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | ID of the sound to play while eating an item affected by this power. If not set this will be the default eating/drinking sound.
`entity_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | If set, this action will be executed on the entity eating this item.
`tick_rate` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `10` | The frequency (in ticks) with which to set the items that satisfy the condition's food components. Lower values set the component quicker, but this comes at a potentially huge performance cost.

### Example
```json
{
    "type": "apugli:edible_item",
    "item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:axolotl_bucket"
        }
    },
    "food_component": {
        "hunger": 4,
        "saturation": 1,
        "meat": true
    },
    "use_action": "eat",
    "return_stack": {
        "item": "minecraft:water_bucket",
        "amount": 1
    }
}
```
This power allows for axolotl in buckets to be edible. Eating an axolotl in a bucket gives 4 hunger shanks and 8 saturation, it also counts as meat. This returns a water bucket upon consumption and uses the eat action.