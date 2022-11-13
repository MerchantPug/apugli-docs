---
title: Redirect Lightning (Power Type)
date: 2022-03-05
---

# Redirect Lightning

[Power Type](../power_types.md).

Redirects lightning to the power holder if a specified chance happens.

Type ID: `apugli:redirect_lightning`



### Fields
Field | Type | Default | Description
------|------|---------|------------
`chance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The chance at which lightning will be redirected to an entity. (Ranges from 0.0-1.0).

### Example
```json
{
    "type": "apugli:redirect_lightning",
    "chance": 0.5
}
```
This example creates a 50% chance that lightning will be redirected to the position of the power holder upon the lightning spawning in the world.