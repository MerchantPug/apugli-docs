---
title: Structure (Entity Condition)
date: 2021-07-13
---

# Structure

[Entity Condition](../entity_condition_types.md).

Checks whether the entity is of a specific entity group.

This condition only works for server side powers due to how structure detection works.

Type ID: `apugli:structure`

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