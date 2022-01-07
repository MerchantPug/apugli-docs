---
title: Bunny Hop (Power Type)
date: 2021-07-13
---

# Bunny Hop

[Power Type](../power_types.md).

An active power that adds velocity to the player each specified tick whenever they aren't on the ground, in water, in lava, in a vehicle (boat, horse, etc), fall flying or not moving at all. The active power button adds a specified amount of velocity to this counter.

Type ID: `apugli:bunny_hop`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |  | The number of ticks the player has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`increase_per_tick` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.000375` | The increase in velocity each tick this power updates velocity.
`ability_velocity` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `5` | The amount of velocity to add to the entity upon using the active power. (this * `increase_per_tick`)
`max_velocity` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.000375` | The amount of velocity that this power is capped to.
`tick_rate` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `10` | The frequency (in ticks) with which to add to the player's velocity. Lower values mean the condition changes are detected more quickly, but this comes at a potentially huge performance cost.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | ID of the sound to play when using this ability.
`key` | [Key](https://origins.readthedocs.io/en/latest/types/data_types/key/) | | Which active key this power should respond to.


### Example
```json
{
  "type": "apugli:bunny_hop",
  "cooldown": 240,
  "hud_render": {
    "should_render": true,
    "sprite_location": "toomanyorigins:textures/gui/tmo_resource_bar.png",
    "bar_index": 7
  },
  "key": {
    "key": "key.origins.primary_active",
    "continuous": false
  },
  "increase_per_tick": 0.000375,
  "ability_velocity": 5,
  "max_velocity": 0.015,
  "tick_rate": 10,
  "sound": "toomanyorigins:origin.hare.dash"
}
```
This power increases the player's velocity by 0.000375 every 10 ticks while the conditions stated above aren't met. The power stays at 0.015 increased velocity as soon as it reaches this velocity/has increased 40 times (0.015 / 0.000375). The ability increases the velocity multiplier by 5 * 0.000375.