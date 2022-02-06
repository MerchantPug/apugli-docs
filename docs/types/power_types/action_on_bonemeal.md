---
title: Action On Bonemeal (Power Type)
date: 2022-02-06
---

#   Action On Bonemeal

[Power Type](../power_types.md)

Execute actions upon applying a Bonemeal to a block.

Type ID: `apugli:action_on_bonemeal`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`block_action` | [Block Action Type](https://origins.readthedocs.io/en/latest/types/block_action_types) | *optional* | If specified, execute this action at the block the Bonemeal is applied on.
`self_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types) | *optional* | If specified, execute this action on the entity that applied the Bonemeal on a block.
`block_condition` | [Block Condition Type](https://origins.readthedocs.io/en/latest/types/block_condition_types) | *optional* | If specified, only execute the specified action(s) if the block the Bonemeal is applied on fulfills this condition.


### Examples

```json
{
    "type": "apugli:action_on_bonemeal",
    "block_action": {
        "type": "apoli:set_block",
        "block": "minecraft:diamond_ore"
    },
    "block_condition": {
        "type": "apoli:block",
        "block": "minecraft:potato"
    }
}
```

This example will replace Potato crop block with a Diamond Ore block if the player that has the power were to apply Bonemeal to the said crop block.