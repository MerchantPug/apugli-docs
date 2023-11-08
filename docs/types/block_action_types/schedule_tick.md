---
title: Schedule Tick (Block Action Type)
date: 2021-11-08
---

# Schedule Tick

[Block Action Type](../block_action_types.md).

Schedules a block to start ticking after a randomised interval between a min value and a max value.

Type ID: `apugli:schedule_tick`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`min` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The minimum value (inclusive) that the block will start ticking after.
`max` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The maximum value (inclusive) that the block will start ticking after.

### Example
```json
{
    "type": "apugli:schedule_tick",
    "min": 20,
    "max": 60
}
```
