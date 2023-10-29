---
title: Bunny Hop (Power Type)
date: 2021-07-13
---

# Bunny Hop

[Power Type](../power_types.md).

Adds movement velocity to the player whenever they aren't on the ground, in water, in lava, in a vehicle (boat, horse, etc) or fall flying.

Type ID: `apugli:bunny_hop`

!!! note

    This power type provides a variable that can be changed with the [Change Resource (Entity Action Type)](../entity_action_types.mdchange_resource), and check the value of with the [Resource (Entity Condition Type)](../entity_condition_types.mdresource).

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`min` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer) | | The minimum value of the resource.
`max` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer) | | The maximum value of the resource.
`hud_render` | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render) | | Determines how the resource is visualized on the HUD.
`start_value` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer) | _optional_ | The value of the resource when the entity first receives the power. If not set, this will be set to the value of the `min` integer field.
`min_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types) | _optional_ | If specified, this action will be executed on the entity whenever the minimum value is reached.
`max_action` | [Entity Action Type](https://origins.readthedocs.io/en/latest/types/entity_action_types) | _optional_ | If specified, this action will be executed on the entity whenever the maximum value is reached.
`increase_per_tick` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.000375` | The amount of velocity added to the player depending on the resource's value.
`tick_rate` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer) | `10` | The frequency (in ticks) in which to add to the resource. Lower values set the component quicker, but this comes at a potentially huge performance cost.

### Example
```json
{
  "type": "apugli:bunny_hop",
  "min": 0,
  "max": 60,
  "hud_render": {
    "should_render": false
  },
  "increase_per_tick": 0.00025,
  "tick_rate": 10
}
```
This power increases the player's movement velocity by 0.00025 every 10 ticks while the conditions stated above aren't met until it reaches 60. This power does not render on the HUD.