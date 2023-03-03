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
`texture_url` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | If specified, the url to a .png file imported into the game as a texture for this power's use. This will be used as a fallback if `texture_location` is not specified or if a texture is not present.
`show_first_person` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether the texture overlay should show up in first person.
`use_rendering_powers` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether the power should have rendering powers such as `apoli:model_color` applied to them.
`render_original_model` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Whether the original model of the entity should be rendered. Layers will remain untouched.
`render_player_outer_player` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Whether the power will prevent the outer layer of the player from rendering.

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
This will have the texture at `test/steve.png` overlayed over any entity with the `default` player model type.