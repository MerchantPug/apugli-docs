---
title: Rocket Jump (Power Type)
date: 2021-08-19
---

# Rocket Jump

[Power Type](../power_types.md).

An active power that launches the player through the air while leaving an explosion at their crosshair location.

Type ID: `apugli:rocket_jump`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |  | The number of ticks the player has to wait between uses of this power.
`distance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | Determines the maximum length of the raycast. Defaults to the entity's reach if not present. |
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`source` | [Damage Source](https://origins.readthedocs.io/en/latest/types/data_types/damage_source/) | *optional* | If set, this is the damage source that will be used to deal damage to the entity upon using this ability.
`amount` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional*| How much damage will be dealt upon using this ability.
`speed` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The speed of the velocity applied to the player in the opposite direction they are facing when using this power.
`use_charged` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines if the power should use either the `toomanyorigins:charged` or `cursedorigins:charged` status effect to increase the velocity of the jump and explosion radius of this power (This requires either of the two mods to use this but this power will function normally without either mod).
`charged_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the speed of the rocket jump when the entity is charged (See `use_charged` field description for charged criteria).
`charged_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the speed of the rocket jump when the entity is charged (See `use_charged` field description for charged criteria).
`key` | [Key](https://origins.readthedocs.io/en/latest/types/data_types/key/) | | Which active key this power should respond to.

### Example
```json
{
  "type": "apugli:rocket_jump",
  "cooldown": 5,
  "hud_render": {
    "should_render": true,
    "sprite_location": "toomanyorigins:textures/gui/tmo_resource_bar.png",
    "bar_index": 2
  },
  "source": {
    "name": "overheat",
    "bypasses_armor": "true",
    "fire": "true",
    "unblockable": "true"
  },
  "charged_modifier": {
    "operation": "multiply_base",
    "value": 0.5
  },
  "key": {
    "key": "key.use",
    "continuous": false
  },
  "amount": 2.0,
  "should_use_charged": true,
  "speed": 1.0
}
```
This power allows a player to launch themself through the air by pressing the use key while taking 1 heart of armor bypassing, unblockable fire damage named overheat. This ability considers the Charged status effect from TooManyOrigins and CursedOrigins and will modify the speed of the velocity application by 1.5x the regular amount.