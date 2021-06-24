---
title: Modify Soul Speed (Power Type)
date: 2021-06-25
---

# Modify Soul Speed

[Power Type](../power_types.md).

Adds the specified amount of Soul Speed levels to an entity.

Type ID: `apugli:modify_soul_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the entity's amount of Soul Speed.
`modifiers` | [Array of Attribute Modifiers](https://origins.readthedocs.io/en/latest/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the entity's amount of Soul Speed.

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