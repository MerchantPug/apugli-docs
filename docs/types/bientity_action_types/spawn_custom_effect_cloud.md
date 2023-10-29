---
title: Spawn Custom Effect Cloud (Entity Action Type)
date: 2023-10-30
---

# Spawn Custom Effect Cloud

[Bi-entity Action Type](../bientity_action_type.md)

Spawns an effect cloud at either the actor or target's position that is customisable by the fields in the power type.

Type ID: `apugli:spawn_custom_effect_cloud`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_id` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | An identifier for use with custom effect clouds spawned through this entity action. For use with [Custom Entity Id (Entity Condition Type)](../entity_condition_types/custom_entity_id).
`radius` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `3.0` | The starting radius of the custom effect cloud.
`radius_on_use` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `3.0` | The value to subtract from the custom effect cloud's radius each time it affects an entity.
`radius_per_tick` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `3.0` | The value to add to the custom effect cloud's radius each tick.
`wait_time` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `10` | The time that the custom effect cloud must wait for before being able to execute actions.
`duration` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `600` | The duration of the custom effect cloud.
`reapplication_delay` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `20` | The time that the custom effect cloud must wait before executing an action on an entity again.
`particle` | [Particle Effect](https://origins.readthedocs.io/en/latest/types/data_types/particle_effect/) | | The particle effect that the custom effect cloud emits.
`height_increase` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `0.0` | Extra y distance that the entity needs to be in in order to be effected by this area effect cloud.
`powers_to_apply` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | `0.0` | Extra y distance that the entity needs to be in in order to be effected by this area effect cloud.
`owner_cloud_bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | A bi-entity action with the cloud's owner as the actor, and the cloud as the target to execute whenever an entity should be affected by the cloud.
`cloud_target_bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | A bi-entity action with the cloud as the actor, and the entity that is affected by the cloud as the target to execute whenever an entity should be affected by the cloud.
`owner_target_bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | A bi-entity action with the cloud's owner as the actor, and the entity that is affected by the cloud as the target to execute whenever an entity should be affected by the cloud.
`bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | *optional* | A bi-entity condition that must be met with the cloud as the actor and any entity that is inside the cloud as the target for any actions to execute.
`owner_target_bientity_condition` | [Bi-entity Condition Type](../bientity_condition_types.md) | *optional* | A bi-entity condition that must be met with the cloud's owner as the actor and any entity that is inside the cloud as the target for any actions to execute.
`spawn_target` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"target"` | Whether the cloud will spawn on the actor or the target. Accepts either `"actor"`, `"ACTOR"`, `"target"` or `"TARGET"`.


### Examples

```json
{
    "type": "apugli:spawn_custom_effect_cloud",
    "entity_id": "example:dragon_fireball_cloud",
    "radius": 2.5,
    "radius_on_use": 0.0,
    "wait_time": 0,
    "radius_per_tick": -0.00375,
    "duration": 100,
    "particle": "minecraft:dragon_breath",
    "powers_to_apply": [
        "example:dragon_cloud_debuff"
    ],
    "bientity_condition": {
        "type": "origins:invert",
        "condition": {
            "type": "apugli:owner"
        },
        "inverted": true
    },
    "spawn_target": "actor"
}
```
This example action will spawn a custom effect cloud with an id of `example:dragon_fireball_cloud`, it starts out with a radius of 2.5, does not decrease upon affecting an entity and decreases by `0.00375` each tick. Entities within the cloud that are not the owner of the cloud will have the `example:dragon_cloud_debuff` power applied to them. It lasts for 100 ticks/5 seconds. This will spawn on the actor.