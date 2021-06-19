---
title: Detonate (Power Type)
date: 2021-06-20
---

# Detonate

[Power Type](../power_types.md).

Defines the entity group of the player, mostly used for determining enchantment bonus damage towards the player. A player should only have one of this or `origins:entity_group`.

If you'd like to use the vanilla entity groups use `origins:entity_group` instead.

Type ID: `apugli:entity_group`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`explosion_radius` | [Integer](https://origins.readthedocs.io/en/latest/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`spawns_effect_cloud` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | false | Whether the entity should spawn an effect cloud with all their active status effects upon exploding.
`damage_source` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | *optional* | If set, this is the damage source that will be used to deal the damage of the explosion.
`self_damage_source` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | *optional* | If set, this is the damage source that will be dealt to the player who exploded.
`key` | [Float](https://origins.readthedocs.io/en/latest/data_types/float/) | 3.0 | Specifies the size of the explosion's radius.

### Example
```json
{
  "type": "apugli:self_explode",
  "explosion_radius": 3.0,
  "key": {
    "key": "key.origins.primary_active",
    "continuous": true
  },
  "spawns_effect_cloud": true,
  "condition": {
    "type": "origins:or",
    "conditions": [
      {
        "type": "apugli:nearby_entities",
        "entity_type": "minecraft:cat",
        "player_box_multiplier": 5.0,
        "comparison": ">=",
        "compare_to": 1,
        "inverted": "true"
      },
      {
        "type": "apugli:nearby_entities",
        "entity_type": "minecraft:ocelot",
        "player_box_multiplier": 5.0,
        "comparison": ">=",
        "compare_to": 1,
        "inverted": "true"
      }
    ]
  }
}
```
This power allows the player to explode whenever they aren't near a cat or ocelot.