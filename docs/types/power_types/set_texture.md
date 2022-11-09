---
title: Set Texture (Power Type)
date: 2021-08-19
---

# Set Texture

[Power Type](../power_types.md).

A power that sets an entity's base texture.

Type ID: `apugli:set_texture`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`texture_location` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) |  | Where the new texture is located.
`player_model` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) |  | The player model to associate with the player entity. One of `default` or `slim`. This only works for player entities.

### Example
```json
{
    "type": "apugli:set_texture",
    "texture_location": "apugli:textures/test.png",
    "player_model": "default"
}
```
This power sets an entity's base texture to test.png, this texture is located in the textures folder in the apugli namespace.