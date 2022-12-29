---
title: Player Model Type (Power Type)
date: 2022-12-29
---

# Player Model Type

[Power Type](../power_types.md).

A power type that sets a player's model type.

Type ID: `apugli:player_model_type`

!!! note

    This power will not update the player's texture, so you may be left with transparent pixels as a result of this.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`model` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) |  | The player model to associate with a player entity. One of `default` or `slim`.

### Example
```json
{
    "type": "apugli:player_model_type",
    "model": "slim"
}
```
This example sets a `PlayerEntity`'s model type to the `slim` model type. 