---
title: Base Enchantment (Entity Condition Type)
date: 2021-08-03
---

# Base Enchantment

[Entity Condition Type](../entity_condition_types.md).

Checks the level of an enchantment on the entity's equipment based purely on item nbt.

Type ID: `apugli:base_enchantment`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the enchantment of interest.
`calculation` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | `"sum"` | Which number to compare - either the `sum` of levels of this enchantment on all of the player's equipment, or the `max` level of this enchantment on any of the player's equipment.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | `">="` | How the enchantment level should be compared to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The value to compare the enchantment level to.

### Example
```json
"condition": {
    "type": "origins:base_enchantment",
    "enchantment": "minecraft:thorns",
    "calculation": "max",
    "comparison": ">=",
    "compare_to": 3
}
```
This example checks if the entity has a Thorns level of III or higher on any equipped item. This does not count the `apugli:modify_enchantment_level` power or any other non nbt enchantment level modifications.