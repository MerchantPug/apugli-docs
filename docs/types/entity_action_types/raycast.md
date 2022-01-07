---
title: Rasycast (Entity Action)
date: 2021-08-19
---

# Raycast

[Entity Action](../entity_action_types.md).

An entity action that raycasts from an entity and performs actions based on what's specified.

Type ID: `apugli:raycast`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`block_action` | [Block Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | The block action to be executed on the block the player has targeted.
`block_condition` | [Block Condition](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | *optional* | The block condition that must be met by the entity the player is targeting in order to do actions.
`target_action` | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | The entity action to be executed on the entity the player has targeted.
`target_condition` | [Entity Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | *optional* | The entity condition that must be met by the entity the player is targeting in order to do actions.
`self_action` | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | *optional* | The action(s) to be executed on the entity that used the raycast upon successfully raycasting.

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