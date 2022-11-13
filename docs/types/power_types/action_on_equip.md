---
title: Action On Equip (Power Type)
date: 2022-01-08
---

# Action On Equip

[Power Type](../power_types.md).

Executes an action when an item is equipped.

Type ID: `apugli:action_on_equip`

### Fields
Field  | Type | Default | Description
-------|------|---------|-------------
`head` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types) | *optional* | The condition that the `head` slot item must meet to run the action.
`chest` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types) | *optional* | The condition that the `chest` slot item must meet to run the action.
`legs` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types) | *optional* | The condition that the `legs` slot item must meet to run the action.
`feet` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types) | *optional* | The condition that the `feet` slot item must meet to run the action.
`offhand` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types) | *optional* | The condition that the `offhand` slot item must meet to run the action.
`action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types) | | Action to apply when an item that meets any stated conditions are met.

### Example
```json
{
    "type": "apugli:action_on_equip",
    "head": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:netherite_helmet"
        }
    },
    "action": {
        "type": "apoli:heal",
        "amount": 6
    }
}
```
This power heals you for 3 hearts when you equip a netherite helmet.