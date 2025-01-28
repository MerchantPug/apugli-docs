---
title: Dimensions (Entity Condition Type)
date: 2023-11-11
---

# Dimensions

[Entity Condition Type](../entity_condition_types.md).

Compares the entity's dimensions to a specified value.

Type ID: `apugli:dimensions`

### Fields

Field | Type | Default | Description
------|------|---------|------------
`dimensions` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array) of [Strings](https://origins.readthedocs.io/en/latest/types/data_types/string) | `["width", "height"]` | Determines which axes should be checked for the hitbox. Accepts `"width"`, `"height"` or both.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison) | `>=` | Determines how the entity's dimensions should be compared to the specified value.
`compare_to` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float) | | The value at which the entity's dimensions will be compared to.

### Example
```json
{
    "entity_condition": {
        "type": "apugli:dimensions"
    }
}
```