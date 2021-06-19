---
title: Extra Soul Speed (Power Type)
date: 2021-06-20
---

# Extra Soul Speed

[Power Type](../power_types.md).

Adds the specified amount of Soul Speed levels to an entity.

Type ID: `apugli:extra_soul_speed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) |  | The amount of Soul Speed to add to the player.


### Example
```json
{
  "type": "apugli:extra_soul_speed",
  "modifier": 1
}
```
This power adds 1 level of Soul Speed to any entity that has this power.