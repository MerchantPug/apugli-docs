---
title: Light Up Block (Power Type)
date: 2021-07-13
---

# Light Up Block

[Power Type](../power_types.md).

An active power that lights up furnaces, campfires and brewing stands.

Type ID: `apugli:light_up_block`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) |  | The number of ticks the player has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`burn_time` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | `1600` | The number of ticks that a furnace is lit for.
`brew_time` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | `20` | The amount of fuel given to a brewing stand upon use.
`particle` | [Identifier](https://origins.readthedocs.io/en/latest/data_types/identifier/) | *optional* | ID of the particle type to use.
`particle_count` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | *optional* | The amount of particles to spawn when using this ability.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/data_types/identifier/) | *optional* | ID of the sound to play when using this ability.
`key` | [Key](https://origins.readthedocs.io/en/latest/data_types/key/) | | Which active key this power should respond to.


### Example
```json
{
  "type": "apugli:light_up_block",
  "cooldown": 80,
  "hud_render": {
    "should_render": true,
    "sprite_location": "toomanyorigins:textures/gui/tmo_resource_bar.png",
    "bar_index": 1
  },
  "burn_time": 2600,
  "brew_time": 20,
  "particle": "minecraft:dragon_breath",
  "particle_count": 15,
  "sound": "minecraft:entity.ender_dragon.shoot",
  "key": {
    "key": "key.origins.primary_active",
    "continuous": false
  },
  "condition": {
    "type": "apugli:block_looking_at",
    "block_condition": {
      "type": "origins:block",
      "block": "toomanyorigins:furnace",
      "inverted": true
    }
  }
}
```
This power allows a player to light up a furnace for 2600 ticks and fill a brewing stand if they are looking at any blocks that can be lit by this power other than a furnace. This emits 15 dragon breath particles upon lighting something up.