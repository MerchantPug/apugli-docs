---
title: Player Model (Power Type)
date: 2021-07-14
---

# Player Model

[Power Type](../power_types.md).

A power that sets a player entity's model as either `default` or `slim`.

Type ID: `apugli:player_model`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`model` | [String](https://origins.readthedocs.io/en/latest/data_types/string/) |  | The player model to associate with the player entity. One of `default` or `slim`

### Example
```json
{
  "type": "apugli:player_model",
  "model": "default"
}
```
This power sets a player with this power's model to the default (Steve) model.