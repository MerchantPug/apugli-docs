---
title: Step Height (Power Type)
date: 2023-11-08
---

# Step Height

[Power Type](../power_types.md).

Allows a player to walk into a block to step up it at certain heights.

Type ID: `apugli:step_height`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`lower_height` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.0` | The height at which the entity's lower body must meet compared to the upper bounds of the block to step up onto it.
`upper_height` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.0` | The height at which the entity's upper body must meet compared to the lower bounds of the block to step below it.
`allow_jump_after` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether a player can jump straight after stepping up a block.

### Example
```json
{
    "type": "apugli:step_height",
    "lower_height": 1.0
}
```
This example allows an entity to step up an entire block by walking into it.