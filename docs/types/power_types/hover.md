---
title: Hover (Power Type)
date: 2022-03-05
---

# Hover

[Power Type](../power_types.md).

Multiplies the Y velocity of the entity by 0, effectively making them stationary on the Y axis.

Type ID: `apugli:hover`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`step_assist` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) |  | The range from the top or bottom of a block at which this power will correct the entity's orientation.

### Example
```json
{
    "type": "apugli:hover"
}
```