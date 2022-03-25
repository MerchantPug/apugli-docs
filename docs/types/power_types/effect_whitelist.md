---
title: Effect Whitelist (Power Type)
date: 2022-03-25
---

# Effect Whitelist

[Power Type](../power_types.md).

Prevents all status effects but those specified from being applied to the entity that has the power.

Type ID: `apugli:effect_whitelist`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, the status effect with this namespace and ID is the only effect that can be applied to the entity that has the power.
`effects` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, the status effects with the specified namespace and IDs are the only effects that can be applied to the entity that has the power.

### Example
```json
{
    "type": "origins:effect_whitelist",
    "effects": [
        "minecraft:weakness",
        "minecraft:strength"
    ]
}
```
This example will make the entity immune to all status effects except weakness and strength.