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
`cooldown` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The number of ticks the player has to wait between uses of this power.
`distance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | Determines the maximum length of the raycast. Defaults to the entity's reach if not present. |
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render/) |  | Specifies how and if a cooldown bar is rendered.
`damage_type` | [Identifier]() | | If set, this is the damage type that will be used to deal damage to the entity upon using this ability.
`source` | [Damage Source](https://origins.readthedocs.io/en/latest/types/data_types/damage_source/) | **DEPRECATED** | Use `damage_type` instead. [More information here.](https://gist.github.com/apace100/bfbf82a8f9d6bd2db13e4feaf653a6b0)
`amount` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional*| How much damage will be dealt upon using this ability.
`velocity` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The velocity applied to the player in the opposite direction they are facing when using this power.
`horizontal_velocity` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | The velocity applied to the player in the opposite direction they are facing on horizontal axes when using this power. If not set, this will be set to the value of the `velocity` float field.
`vertical_velocity` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | The velocity applied to the player in the opposite direction on the vertical axis they are facing when using this power. If not set, this will be set to the value of the `velocity` float field.
`velocity_clamp_multiplier` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.8` | The amount to multiply by the current base amount to clamp the velocity gained from this power to.
`use_charged` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines if the power should use a status effect inside the tag `apugli:charged_effects` to increase the velocity of the jump and explosion radius of this power.
`charged_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the velocity of the rocket jump when the entity is charged (See `use_charged` field description for charged criteria).
`charged_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the velocity of the rocket jump when the entity is charged (See `use_charged` field description for charged criteria).
`water_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the velocity of the rocket jump when the entity is touching water.
`water_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the velocity of the rocket jump when the entity is touching water.
`damage_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the damage of the explosion caused by the rocket jump.
`damage_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the damage of the explosion caused by the rocket jump.
`targetable_bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If set, a bi-entity condition to check for with the power holder as the actor and the target as the target for the rocket jump to successfully land.
`damage_bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If set, a bi-entity condition that will be applied to any entities damaged by the rocket jump with the power holder as the actor and the target as the target.
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
    "velocity": 1.0
}
```
This power allows a player to launch themself through the air by pressing the use key while taking 1 heart of armor bypassing, unblockable fire damage named overheat. This ability considers the Charged status effect from TooManyOrigins and CursedOrigins and will modify the speed of the velocity application by 1.5x the regular amount.