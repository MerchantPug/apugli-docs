---
title: Apugli Entity Group (Entity Condition)
date: 2021-06-20
---

# Apugli Entity Group

[Entity Condition](../entity_conditions.md).

Checks whether a player entity is looking at a specific block within their reach.

Type ID: `apugli:block_looking_at`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition](https://origins.readthedocs.io/en/latest/block_conditions/) |  | The block condition which is applied to the block the player is looking at.

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