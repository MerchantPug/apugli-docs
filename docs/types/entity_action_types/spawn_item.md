---
title: Spawn Item (Entity Action Type)
date: 2022-07-29
---

# Spawn Item

[Entity Action Type](../entity_action_types.md).

Drops an item where the action is executed.

Type ID: `apugli:spawn_item`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`stack` | [Item Stack](https://origins.readthedocs.io/en/latest/types/data_types/item_stack/) | | The item stack to drop using this power.


### Example
```json
"entity_action": {
    "type": "apugli:spawn_item",
    "stack": {
        "item": "minecraft:coal",
        "amount": 64
    }
}
```
This action drops an `ItemStack` of 64 coal where it was executed.