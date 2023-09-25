---
title: Explode (Apugli) (Entity Action Type)
date: 2022-03-04
---

# Explode

[Entity Action Type](../entity_action_types.md)

Summons an explosion at the position of the entity.

Type ID: `apugli:explode`


### Fields

Field | Type | Default | Description
------|------|---------|-------------
`power` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | Determines the power of the explosion.
`destruction_type` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"break"` | Determines if the explosion should destroy the terrain, destroy the terrain and drop the loot of the blocks, or none (`"destroy"`, `"break"` or `"none"` respectively).
`damage_self` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/data_types/boolean/) | `true` | Determines if the player should take damage from the summoned explosion.
`indestructible` | [Block Condition Type](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | _optional_ | If specified, the blocks that fulfills the specified block condition type is not destroyed by the summoned explosion.
`destructible` | [Block Condition Type](https://origins.readthedocs.io/en/latest/types/block_condition_types/) | _optional_ | If specified, the blocks that fulfills this specified block condition type are the **only** blocks that are destroyed by the summoned explosion.
`create_fire` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/data_types/boolean/) | `false` | Determines if the explosion should create fire.
`use_charged` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/data_types/boolean/) | `false` | Determines if the power should use either the `toomanyorigins:charged` or `cursedorigins:charged` status effects to increase the poewr of the summoned explosion (This requires either of the two mods to use this but this power will function normally without either mod).
`damage_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the damage value towards other entities from this explosion.
`damage_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the damage value towards other entities from this explosion.
`knockback_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the knockback towards other entities from this explosion.
`knockback_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the knockback towards other entities from this explosion.
`volume_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the volume of the sound event from this explosion.
`volume_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the volume of the sound event from this explosion.
`pitch_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the pitch of the sound event from this explosion.
`pitch_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the pitch of the sound event from this explosion.
`damage_bientity_condition` | [Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | If set, determines if an entity will be damaged by the explosion with the entity who ran this action as the actor and the entity in the explosion radius as the target.
`charged_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the power of the explosion when the entity is charged (See `use_charged` field description for charged criteria).
`charged_modifiers` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the power of the explosion when the entity is charged (See `use_charged` field description for charged criteria).
`spawn_effect_cloud` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/data_types/boolean/) | `false` | Determines if the power holder should lose all of their current status effects to create lingering effect clouds with these effects upon exploding.

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
