---
title: Velocity (Entity Condition Type)
date: 2022-03-29
---

# Velocity

[Entity Condition Type](../entity_condition_types.md).

Checks the entity's velocity values.

Type ID: `apugli:key_pressed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`x` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | The x velocity value to use for the comparison.
`y` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | The y velocity value to use for the comparison.
`z` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | The z velocity value to use for the comparison.
`axes` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Strings](https://origins.readthedocs.io/en/latest/types/data_types/string/)| *optional* | The axes that should be used for the comparison.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)	| `">="` | How the `axes`' velocity should be compared to the specified value.
`compare_to` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | The value for the axes specified in `axes` to compare to.


### Example
```json
"condition": {
  "axes": [
    "y"
  ],
  "compare_to": 4,
  "comparison": "<="
}
```
This example checks if the entity's y velocity is lesser than or equal to 4.