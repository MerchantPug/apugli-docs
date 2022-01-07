---
title: Modify Soul Speed (Power Type)
date: 2021-08-19
---

# Modify Soul Speed

[Power Type](../power_types.md).

Modifies the amount of Soul Speed levels of an entity.

Type ID: `apugli:modify_soul_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the entity's amount of Soul Speed.
`modifiers` | [Array of Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the entity's amount of Soul Speed.
`block_condition` | [Block Condition](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | *optional* | If set, this will determine what blocks the soul speed effect will activate on.

### Example
```json
{
  "type": "origins:modify_soul_speed",
  "modifier": {
     "operation": "addition",
    "value": 1
  },
    "condition": {
    "type": "origins:enchantment",
    "enchantment": "minecraft:soul_speed",
    "calculation": "max",
    "comparison": "=",
    "compare_to": 0
  }
}
```
This power adds 1 level of Soul Speed to an entity if the entity is wearing equipment without the Soul Speed enchantment.