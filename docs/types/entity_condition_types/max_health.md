---
title: Max Health (Entity Condition Type)
date: 2023-02-08
---

# Max Health

[Entity Condition Type](../entity_condition_types.md).

Applies a check towards the max health attribute value of an entity.

Type ID: `apugli:max_health`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)	| `">="` | How the max health of the entity should be compared to the specified value.
`compare_to` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The value to compare the value to.

### Example
```json
"condition": {
    "type": "apugli:max_health",
    "comparison": ">=",
    "compare_to": 1
}
```
This example tests if an entity's max health is greater than or equal to 1.
