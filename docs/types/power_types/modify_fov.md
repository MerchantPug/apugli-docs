---
title: Modify FoV Change (Power Type)
date: 2022-11-08
---

# Modify FoV

[Power Type](../power_types.md).

Changes the FoV of a player on their client.

Type ID: `apugli:modify_fov`

### Fields
Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to any time that an item meets the item condition's has a change in durability.
`modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to any time that an item meets the item condition's has a change in durability.
`change_divisor` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The divisor at which the FoV will smooth into the next value. A higher value will make it slower.

### Example
```json
{
    "type": "apugli:modify_fov",
    "modifier": {
      "operation": "multiply_base_multiplicative",
      "value": 0.025,
      "modifier": {
        "name": "Additional FOV from stored resource",
        "operation": "multiply_total_multiplicative",
        "value": 0.0,
        "resource": "example:resource"
      }
    },
    "change_divisor": 8
}
```
This example will change the FoV by `0.025` * `example:resource`'s value, with a change divisor of `8`.