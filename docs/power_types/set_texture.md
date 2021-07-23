---
title: Set Texture (Power Type)
date: 2021-07-14
---

# Set Texture

[Power Type](../power_types.md).

A power that sets an entity's base texture.

Type ID: `apugli:set_texture`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`texture_location` | [Identifier](https://origins.readthedocs.io/en/latest/data_types/identifier/) |  | Where the new texture is located.

### Example
```json
{
  "type": "apugli:set_texture",
  "texture_location": "mario:textures/gilbert.png"
}
```
This power sets an entity's base texture to gilbert.png that is located in the textures folder in the mario folder.