---
title: Trident Enchantment (Entity Condition Type)
date: 2023-02-08
---

# Trident Enchantment

[Entity Condition Type](../entity_condition_types.md).

Compares a `TridentEntity`'s enchantment level with a specified value.

Type ID: `apugli:trident_enchantment`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The identifier of the enchantment to test.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)	| `">="` | How the amount of particles within the specified radius which are the specified should be compared to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The value to compare the amount to.

### Example
```json
"condition": {
    "type": "apugli:trident_enchantment",
    "enchantment": "minecraft:riptide",
    "comparison": "==",
    "compare_to": 0
}
```
This example tests whether a Trident entity has no levels of riptide.
