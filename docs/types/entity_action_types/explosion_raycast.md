---
title: Explosion Raycast (Entity Action Type)
date: 2022-03-04
---

# Explosion Raycast

[Entity Action Type](../entity_action_types.md)

Raycasts and summons an explosion at the hit location.

Type ID: `apugli:explosion_raycast`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`distance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | If set, this is the maximum reach of the raycast. Otherwise this defaults to the entity's respective reaches if not present. |
`particle` | [Particle Effect](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | *optional* | If set, the particle effect that is displayed on the ray.
`spacing` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.5` | If there is a particle effect, the spacing between the particles displayed on the ray.
`direction` | [Vector](https://origins.readthedocs.io/en/latest/types/data_types/vector/) | *optional* | If specified, the direction in which the raycast will travel in.
`space` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"world"` | If `direction` is specified, the [Space](https://origins.readthedocs.io/en/latest/misc/extras/space/) to perform the raycast in.
`power` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | Determines the power of the explosion.
`block_action` | [Block Action](../entity_action_types.md) | *optional* | If set, the block action(s) to be executed on the block the entity has targeted.
`bientity_action` | [Bi-entity Action](../bientity_action_types.md) | *optional* | If set, the bi-entity action(s) to be executed on the target entity with the entity that initiated the raycast as the actor and the entity targeted by the raycast as the target.
`action_on_hit` | [Entity Action](../entity_action_types.md) | *optional* | If set, the entity action(s) to execute upon hitting a block or entity with the raycast. 
`destruction_type` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"break"` | Determines if the explosion should destroy the terrain, destroy the terrain and drop the loot of the blocks, or none (`"destroy"`, `"break"` or `"none"` respectively).
`damage_self` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/data_types/boolean/) | `true` | Determines if the player should take damage from the summoned explosion.
`indestructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfills the specified block condition type is not destroyed by the summoned explosion.
`destructible` | [Block Condition Type](../block_condition_types.md) | _optional_ | If specified, the blocks that fulfills this specified block condition type are the **only** blocks that are destroyed by the summoned explosion.
`create_fire` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/data_types/boolean/) | `false` | Determines if the explosion should create fire.
`damage_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the damage value towards other entities from this explosion.
`damage_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the damage value towards other entities from this explosion.
`knockback_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the knockback towards other entities from this explosion.
`knockback_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the knockback towards other entities from this explosion.
`volume_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the volume of the sound event from this explosion.
`volume_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the volume of the sound event from this explosion.
`pitch_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the pitch of the sound event from this explosion.
`pitch_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the pitch of the sound event from this explosion.
`targetable_bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If set, determines if an entity may be targeted by the raycast with the entity that initiated the raycast as the actor and the raycast target as the target.
`explosion_damage_bientity_condition` | [Bi-entity Condition](../bientity_condition_types.md) | *optional* | If set, determines if an entity will be damaged by the explosion with the entity that initiated the raycast as the actor and the entity in the explosion radius as the target.
`charged_condition` | [Entity Condition Type](../entity_condition_types.md) | *optional* | If set, determined when the `charged_modifier` and `charged_modifiers` fields will be used. 
`charged_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the power of the explosion when the `charged_condition` is met.
`charged_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the power of the explosion when the `charged_condition` is met.

### Examples
```json
"entity_action": {
    "type": "apugli:explode",
    "power": 5,
    "destruction_type": "break",
    "damage_self": true,
    "spawn_effect_cloud": true
}
```

This example will summon an explosion that will damage the entity that has summoned the explosion and will break blocks caught in the explosion. This will also spawn lingering effect clouds relating to any status effects the entity has at the time.
