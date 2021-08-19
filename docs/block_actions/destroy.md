---
title: Destroy (Block Action)
date: 2021-08-19
---

# Destroy

[Block Action](../block_actions.md).

A block action that destroys the block that calls this action, leaving particles behind.

Type ID: `apugli:destroy`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
*None.*


### Example
```json
{
    "block_action": {
        "type": "apugli:destroy"
    }
}
```
This block action destroys the block that called this action.