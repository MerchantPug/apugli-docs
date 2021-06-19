---
title: Eat Grass (Power Type)
date: 2021-06-20
---

# Eat Grass

[Power Type](../power_types.md).

Defines the entity group of the player, mostly used for determining enchantment bonus damage towards the player. A player should only have one of this or `origins:entity_group`.

If you'd like to use the vanilla entity groups use `origins:entity_group` instead.

Type ID: `apugli:entity_group`

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
This power eats grass when pressing the Use key whilst holding nothing in your main hand slot.