---
title: Destroy (Block Action)
date: 2021-08-19
---

# Destroy

[Block Action](../block_action_types.md).

A block action that destroys the block that calls this action, leaving particles behind.

Type ID: `apugli:destroy`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`drop_block` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | | Whether the block is dropped upon destroying it.

### Example
```json
{
    "block_action": {
        "type": "apugli:destroy"
    }
}
```
This block action destroys the block that called this action, no item is dropped from it.