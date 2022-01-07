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
head | item_conditions | *optional* | Item condition to match the `head` item.
chest | item_conditions | *optional* | Item condition to match the `chest` item.
legs | item_conditions | *optional* | Item condition to match the `legs` item.
feet | item_conditions | *optional* | Item condition to match the `feet` item.
offhand | item_conditions | *optional* | Item condition to match the `offhand` item.
action | entity_actions | | Action to apply when the matching item is equipped.

### Example
```json
{
    "type": "apugli:action_on_equip",
    "head": {
        "type": "origins:ingredient",
        "ingredient": {
            "item": "minecraft:netherite_helmet"
        }
    },
    "action": {
        "type": "origins:heal",
        "amount": 6
    }
}
```
This power heals you for 3 hearts when you equip a netherite helmet.