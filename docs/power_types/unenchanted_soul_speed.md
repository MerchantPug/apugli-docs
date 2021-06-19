---
title: Unenchanted Soul Speed (Power Type)
date: 2021-06-20
---

# Unenchanted Soul Speed

[Power Type](../power_types.md).

Sets an entity's specified amount of Soul Speed levels to the value specified when their Soul Speed level is lower than the value.

Type ID: `apugli:unenchanted_soul_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) |  | The amount of Soul Speed to add to the player.

### Example
```json
{
  "type": "apugli:unenchanted_soul_speed",
  "modifier": 3
}
```
This power sets the player's Soul Speed level to 3 at all times.