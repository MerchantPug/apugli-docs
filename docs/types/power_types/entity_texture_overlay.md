---
title: Entity Texture Overlay (Power Type)
date: 2022-06-01
---

# Entity Texture Overlay

[Power Type](../power_types.md).

Overlays a texture over an entity's texture.

Type ID: `apugli:entity_texture_overlay`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`texture_location` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) |  | The texture to overlay onto the entity.

### Example
```json
{
    "type": "apugli:entity_texture_overlay",
    "texture_location": "test:steve.png",
    "condition": {
      "type": "apugli:player_model_type",
      "model_type": "default"
    }
}
```
This will have the texture at `test:textures/steve.png` overlayed over any entity with the `default` player model type.