---
title: Item Cooldown (Entity Action Type)
date: 2023-08-11
---

# Item Cooldown

[Entity Action Type](../entity_action_types.md).

Sets the cooldown of a specific item. (Does not operate on specific stacks).

Type ID: `apugli:item_cooldown`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`items` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | The type of items to add a cooldown to if it is present in the inventory.
`item_tags` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | A tag of items to add a cooldown to if they are present in the inventory.
`ticks` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `20` | The amount of ticks that the cooldown should be active for.

### Example
```json
"condition": {
    "items": [
        "minecraft:ender_pearl"
    ],
    "ticks": 20
}
```
This example sets the cooldown to use any Ender Pearl to 20 ticks/1 second.