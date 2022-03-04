---
title: Raycast (Entity Action)
date: 2021-08-19
---

# Raycast

[Entity Action](../entity_action_types.md).

An entity action that raycasts from an entity and performs actions based on what's specified.

Type ID: `apugli:raycast`

!!! note

    If the `distance` field is not set, the distance of the raycast will be dependent on the entity's reach and attack range for blocks and entities respectively.

    Reach defaults to 5.0 in creative mode and 4.5 outside of creative mode.
    Attack Range defaults to 6.0 in creative mode and 3.0 outside of creative mode.

    Any attribute modifiers from Reach Entity Attributes are applied to these initial values.


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`distance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | If set, this is the maximum reach of the raycast. Otherwise this defaults to the entity's respective reaches if not present. |
`pierce` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/data_types/boolean/) | `false` | Determines if the raycast pierces through entities.
`particle` | [Particle Effect](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | *optional* | If set, the particle effect that is displayed on the ray.
`spacing` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.5` | If there is a particle effect, the spacing between the particles displayed on the ray.
`block_action` | [Block Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | If set, the block action to be executed on the block the player has targeted.
`block_condition` | [Block Condition](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | *optional* | If set, the block condition that must be met by the entity the player is targeting in order to do actions.
`bientity_action` | [Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | If set, the bi-entity action(s) to be executed on the entities that have been targeted with the entity that initiated the raycast as the actor and each individual entity targeted by the raycast as the target.
`bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, the bi-entity condition(s) that must be met by the entity that initiated the raycast as the actor and each individual entity targeted by the raycast as the target.
`target_action` | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | If set, the action(s) to be executed on the entities the player has targeted.
`target_condition` | [Entity Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | If set, the condition(s) that must be met by each individual entity the player is targeting in order to do actions.
`self_action` | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | If set, the action(s) to be executed on the entity that initiated the raycast upon successfully raycasting.

### Examples
```json
"entity_action": {
    "type": "apugli:raycast",
    "block_action": {
        "type": "apugli:destroy"
    },
    "target_action": {
        "type": "apugli:swing_hand"
    },
    "self_action": {
        "type": "apoli:apply_effect",
        "effect": {
            "effect": "minecraft:wither",
            "duration": 20,
            "amplifier": 0
        }
    }
}
```
This action destroys any block the player is looking at or swings the hand of the entity they're looking at. Upon successfully doing either of these the entity gains a wither effect for a second.