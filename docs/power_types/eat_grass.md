---
title: Eat Grass (Power Type)
date: 2021-07-17
---

# Eat Grass

[Power Type](../power_types.md).

An active power that allows the user to eat types of grass block.

Type ID: `apugli:eat_grass`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) |  | The number of ticks the player has to wait between uses of this power.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`key` | [Key](https://origins.readthedocs.io/en/latest/data_types/key/) | | Which active key this power should respond to.

### Example
```json
{
  "type": "apugli:eat_grass",
  "cooldown": 5,
  "hud_render": {
    "should_render": false
  },
  "key": {
    "key": "key.use",
    "continuous": true
  },
  "condition" : {
    "type" : "origins:equipped_item",
    "equipment_slot": "mainhand",
    "item_condition": {
      "type": "origins:ingredient",
      "ingredient": {
        "item": "minecraft:air"
      }
    }
  }
}
```
This power eats grass when pressing the use key whilst holding nothing in your main hand slot.