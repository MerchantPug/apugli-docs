---
title: Instant Effect Immunity (Power Type)
date: 2022-03-05
---

# Instant Effect Immunity

[Power Type](../power_types.md).

Prevents instant status effects from being applied to the entity that has the power from direct sources.

Type ID: `apugli:instant_effect_immunity`

### Fields
Field | Type | Default | Description
------|------|---------|------------
`effect` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, only the instant status effect with this namespace and ID can not be applied to the entity that has the power.
`effects` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, only the instant status effects with the specified namespace and IDs can not be applied to the entity that has the power.
`inverted` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether to make the entity immune to the status effect(s) that aren't specified.

### Example
```json
{
    "type": "apugli:instant_effect_immunity",
    "effect": "minecraft:instant_damage",
    "inverted": true
}
```
This example makes the power holder immune to all instant status effects from direct sources that aren't instant damage.