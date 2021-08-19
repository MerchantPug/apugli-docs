---
title: Visual Timer (Power Type)
date: 2021-08-19
---

# Visual Timer

[Power Type](../power_types.md).

Gives a visual timer that depletes from a filled bar. This timer can then have its value checked by the `origins:resource` condition.

Type ID: `apugli:visual_timer`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) |  | The number of ticks the player has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`reset_on_respawn` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | | Specifies if the power resets when a player respawns.

### Examples
```json
{
  "type": "apugli:visual_timer",
  "cooldown": 1800,
  "hud_render": {
    "should_render": true,
    "sprite_location": "toomanyorigins:textures/gui/tmo_resource_bar.png",
    "bar_index": 5
  },
  "reset_on_respawn": true
}
```
This power gives the player a timer whenever they select the origin or respawn.

```json
{
  "condition": {
    "type": "origins:resource",
    "resource": "namespace:visual_timer_json_name",
    "comparison": "<=",
    "compare_to": 0
  }
}
```
This condition is fulfilled when the above visual timer power has run out.