---
title: Structure (Entity Condition)
date: 2021-07-13
---

# Structure

[Entity Condition](../entity_condition_types.md).

Checks whether the entity is of a specific entity group.

This condition only works for server side powers due to how structure detection works.

Type ID: `apugli:structure`

!!! caution

    This condition is only effective server-side. That means client-side power types such as [`apoli:climbing`](https://origins.readthedocs.io/en/latest/types/power_types/climbing/), [`apoli:entity_glow`](https://origins.readthedocs.io/en/latest/types/power_types/entity_glow/), [`apoli:shader`](https://origins.readthedocs.io/en/latest/types/power_types/shader/), etc. won't work with this.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`structure` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) |  | ID of the structure the entity needs to be in to pass the check.

### Example
```json
"condition": {
  "type": "apugli:structure",
  "structure": "minecraft:fortress"
}
```
This example checks if the entity is standing in a nether fortress.