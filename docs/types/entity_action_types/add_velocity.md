---
title: Add Velocity (Apugli) (Entity Action Type)
date: 2023-09-26
---

# Add Velocity

[Entity Action Type](../entity_action_types.md)

Adds or sets velocity towards a specific direction.

Type ID: `apugli:add_velocity`

!!! note

    If the entity action type behaves unexpectedly, try setting either the `client` (should always work) or `server` (might not work) boolean fields to `false`. [Here are some examples.](https://github.com/apace100/apoli/blob/3115c41ea4390ad9ced3ae5be86151131accc36f/testdata/apoli/powers/add_velocity.json)


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`x` | [Float](../data_types/float.md) | `0.0` | The amount of velocity to add on the x-axis.
`y` | [Float](../data_types/float.md) | `0.0` | The amount of velocity to add on the y-axis.
`z` | [Float](../data_types/float.md) | `0.0` | The amount of velocity to add on the z-axis.
`horizontal_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, a modifier to apply to the horizontal velocity of this actio prior to adding the velocity of the entity.n.
`horizontal_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, modifiers to apply to the horizontal velocity of this action prior to adding the velocity of the entity..
`vertical_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, a modifier to apply to the vertical velocity of this action prior to adding the velocity of the entity..
`vertical_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, modifiers to apply to the vertical velocity of this action prior to adding the velocity of the entity.
`horizontal_post_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, a modifier to apply to the horizontal velocity of this action after adding the velocity of the entity.n.
`horizontal_post_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, modifiers to apply to the horizontal velocity of this action after adding the velocity of the entity..
`vertical_post_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, a modifier to apply to the vertical velocity of this action after adding the velocity of the entity..
`vertical_post_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, modifiers to apply to the vertical velocity of this action after adding the velocity of the entity.
`space` | [Space](../data_types/space.md) | `"world"` | The space to perform the addition/setting of velocity in.
`client` | [Boolean](../data_types/boolean.md) | `true` | If this is false, the action will not execute on the client.
`server` | [Boolean](../data_types/boolean.md) | `true` | If this is false, the action will not execute on the server.
`set` | [Boolean](../data_types/boolean.md) | `false` | If this is true, the action will act as a "set" velocity action, overriding the entity's current velocity instead of adding to it.



### Examples

```json
"entity_action": {
    "type": "origins:add_velocity",
    "z": 2,
    "space": "LOCAL",
    "horizontal_post_modifiers": [
        {
            "operation": "min_total",
            "value": -2.2
        },
        {
            "operation": "max_total",
            "value": 2.2
        }
    ]
}
```

This example will add velocity to the entity's positive Z axis in the local space, making the entity go towards the direction they are looking. It is also modified to make sure that the entity is capped between -2.2 and 2.2 on the horizontal axes (x, z).
