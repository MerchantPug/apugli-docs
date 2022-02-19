---
title: Modify Block Placed (Power Type)
date: 2022-02-06
---

# Modify Block Placed

[Power Type](../power_types.md)

Modifies the placed block upon placing one.

Type ID: `apugli:modify_block_placed`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`block` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier) | *optional* | If specified, replaces the placed block with the block that has the specified namespace and ID.
`block_state` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string) | *optional* | If specified, replaces the placed block with the block that has the specified namespace, ID and block state.
`blocks` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier) | *optional* | If specified, replaces the placed block with the blocks that has the specified namespace and IDs in a random fashion.
`block_states` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier) | *optional* | If specified, replaces the placed block with the blocks that has the specified namespace, ID and block state in a random fashion.
`block_action` | [Block Action Type](https://origins.readthedocs.io/en/latest/types/block_action_types) | *optional* | If specified, executes the specified action at the placed block.
`item_condition` | [Item Condition Type](https://origins.readthedocs.io/en/latest/types/item_condition_types) | | The block item used for placing a block.


### Examples

```json
{
    "type": "apugli:modify_block_placed",
    "blocks": [
        "minecraft:white_wool",
        "minecraft:orange_wool",
        "minecraft:magenta_wool",
        "minecraft:light_blue_wool",
        "minecraft:yellow_wool",
        "minecraft:lime_wool",
        "minecraft:pink_wool",
        "minecraft:gray_wool",
        "minecraft:light_gray_wool",
        "minecraft:cyan_wool",
        "minecraft:purple_wool",
        "minecraft:blue_wool",
        "minecraft:brown_wool",
        "minecraft:green_wool",
        "minecraft:red_wool",
        "minecraft:black_wool"
    ],
    "item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "tag": "minecraft:wool"
        }
    }
}
```

This example will randomly replace the color of the Wool block that you place.
<br>

```json
{
    "type": "apugli:modify_block_placed",
    "block_states": [
        "minecraft:chest[facing=north]",
        "minecraft:chest[facing=south]",
        "minecraft:chest[facing=east]",
        "minecraft:chest[facing=west]"
    ],
    "item_condition": {
        "type": "apoli:ingredient",
        "ingredient": {
            "item": "minecraft:chest"
        }
    }
}
```

This example will randomly "rotate" the Chest block that you place.
