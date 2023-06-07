---
title: Cached Block In Radius (Entity Condition Type)
date: 2021-04-04
---

# Cached Block In Radius

[Entity Condition Type](../entity_condition_types.md)

Checks whether there is a specified number of blocks that fulfills the specified [Block Condition Type](../block_condition_types.md) within a specified radius relative to the entity's feet. Unlike `apoli:block_in_radius` this caches the return value where the entity is standing, as well as storing the return value of the blocks surrounding the entity.

Pretty much all of this page was taken from the Origins documentation.

Type ID: `apugli:cached_block_in_radius`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_condition` | [Block Condition Type](../block_condition_types.md) | | The block condition type to check for.
`radius` | [Integer](../data_types/integer.md) | | The radius to check the blocks that fulfills the specified block condition type within.
`shape` | [String](../data_types/string.md) | `"cube"` | Determines the shape of the radius. Accepts `"cube"`, `"star"` or `"sphere"`.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the amount of blocks within the specified radius which fulfills the specified block condition type should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | The value to compare the amount to.


### Examples

```json
"condition": {
    "type": "apugli:cached_block_in_radius",
    "block_condition": {
        "type": "apugli:air",
    },
    "radius": 8,
    "shape": "star",
    "comparison": ">=",
    "compare_to": 2
}
```

This example will check if 2 or more blocks that are air are within an 8 block star from the center of the entity.