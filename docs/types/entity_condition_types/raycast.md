---
title: Looking At (Entity Condition)
date: 2021-08-19
---

# Looking At

[Entity Condition](../entity_condition_types.md).

Checks whether a player entity is looking at a specific block or entity within their reach.

Entities are prioritized over blocks.

Type ID: `apugli:raycast`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | *optional* | The block condition which is applied to the block the player is looking at.
`target_condition` | [Entity Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | The entity condition which is applied to the entity the player is looking at.

### Example
```json
"condition": {
  "type": "apugli:block_looking_at",
  "block_condition": {
    "type": "origins:block",
    "block": "minecraft:grass_block"
  }
}
```
This condition applied to a power will make sure it's only active while the player is looking at a grass block.