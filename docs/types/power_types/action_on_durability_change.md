---
title: Action on Durability Change (Power Type)
date: 2022-03-05
---

# Action on Durability Change

[Power Type](../power_types.md).

Executes entity actions whenever an item either gains durability, loses durability or breaks.

Type ID: `apugli:action_on_durability_change`

!!! note

    This power type does not trigger when you use `apoli:damage`, use `apugli:damage` instead.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Stack](https://origins.readthedocs.io/en/latest/types/data_types/item_stack/) | *optional* | If set, the item condition to check for before executing the action on the damaged item. If not set this is true all the time.
`increase_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types) | *optional* | If set, these action(s) will be executed when an item that meets the condition's durability increases.
`decrease_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types) | *optional* | If set, these action(s) will be executed when an item that meets the condition's durability decreases.
`break_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types) | *optional* | If set, these action(s) will be executed when an item that meets the condition breaks.

### Example
```json
{
  "type": "apugli:action_on_durability_change",
  "item_condition": {
    "type": "origins:ingredient",
    "ingredient": {
      "item": "minecraft:elytra"
    }
  },
  "break_action": {
    "type": "apoli:explode",
    "power": 5,
    "destruction_type": "break",
    "damage_self": true
}
```
This example will cause an explosion whenever the power holder breaks an elytra.