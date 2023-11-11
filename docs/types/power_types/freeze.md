---
title: Freeze (Apugli) (Power Type)
date: 2023-11-11
---

# Sprinting

[Power Type](../power_types.md).

Freezes the entity as if they were in powder snow.

Type ID: `apugli:freeze`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the time it takes to fully freeze an entity.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the time it takes to fully freeze an entity.
`should_damage` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) |  | Whether this power type's freeze should damage the power holder. 

### Example
```json
{
    "type": "apugli:freeze",
    "should_damage": false
}
```
This example will freeze an entity but will not damage them.