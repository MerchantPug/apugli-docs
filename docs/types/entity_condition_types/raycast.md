---
title: Raycast (Entity Condition Type)
date: 2021-08-19
---

# Raycast

[Entity Condition Type](../entity_condition_types.md).

Checks whether a player entity is looking at a specific block or entity within their reach.

Entities are prioritized over blocks.

Type ID: `apugli:raycast`

!!! note

    If the `distance` field is not set, the distance of the raycast will be dependent on the entity's reach and attack range for blocks and entities respectively.

    Reach defaults to 5.0 in creative mode and 4.5 outside of creative mode.
    Attack Range defaults to 6.0 in creative mode and 3.0 outside of creative mode.

    Any attribute modifiers from Reach Entity Attributes are applied to these initial values.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`distance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | If set, the maximum reach of the raycast otherwise defaults to the entity's reach if not present. |
`block_condition` | [Block Condition](../block_condition_types.md) | *optional* | If specified, the block condition which must be fulfilled relating to the block that is hit by the raycast.
`target_condition` | [Entity Condition](../entity_condition_types.md) | *optional* | If specified, the entity condition which must be fulfilled relating to the entity that is hit by the raycast.
`bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If specified, the bi-entity condition which must be fulfilled relating to the entity the raycast originates from and the entity that was hit by the raycast.
`direction` | [Vector](https://origins.readthedocs.io/en/latest/types/data_types/vector/) | *optional* | If specified, the direction in which the raycast will travel in.
`space` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"world"` | If `direction` is specified, the [Space](https://origins.readthedocs.io/en/latest/misc/extras/space/) to perform the raycast in.

### Example
```json
"condition": {
    "type": "apugli:block_looking_at",
    "block_condition": {
        "type": "apoli:block",
        "block": "minecraft:grass_block"
    }
}
```
This condition applied to a power will make sure it's only active while the player is looking at a grass block.