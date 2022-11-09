---
title: Action On Target Death (Power Type)
date: 2021-08-11
---

# Action On Target Death

[Power Type](../power_types.md)

Executes an action upon placing a block.

Type ID: `apugli:action_on_block_placed`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`block_action` | [Block Action Type](https://origins.readthedocs.io/en/latest/types/block_action_types) | _optional_ | If specified, this action type will be executed upon placing a block using a certain block item.
`item_condition` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types) | | The block item used for placing a block.


### Examples

```json
{
    "type": "apugli:action_on_block_placed",
    "block_action": {
        "type": "apoli:execute_command",
        "command": "summon armor_stand ~ ~ ~ {Marker: 1b, Tags: [\"test\"]}"
    },
    "item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:cobblestone"
        }
    }
}
```

This example will summon a marker Armor Stand at the position of the placed Cobblestone block.