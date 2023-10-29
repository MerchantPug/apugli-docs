---
title: Custom Projectile (Entity Action Type)
date: 2023-10-29
---

# Custom Projectile

[Power Type](../power_types.md)

Fires a projectile that is customisable by the fields in the power type.

Type ID: `apugli:custom_projectile`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_id` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | An identifier for use with projectiles spawned through this entity action. For use with [Custom Entity Id (Entity Condition Type)](../entity_condition_types/custom_entity_id).
`texture_location` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, the texture used for the custom projectile.
`texture_url` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | If specified, the url to a .png file imported into the game as a texture for this power's use. This will be used as a fallback if `texture_location` is not specified or if a texture is not present.
`count` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The amount of projectiles to fire each use.
`speed` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.5` | The speed applied to the fired projectile.
`divergence` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | How much each projectile fired is affected by random spread.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If set, the sound with this ID will be played when the power is used.
`tag` | [NBT](https://origins.readthedocs.io/en/latest/types/data_types/nbt/) | *optional* | NBT data of the entity.
`entity_action_before_firing` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, the entity action to execute on the entity firing the projectile just prior to the projectile being created.
`bientity_action_after_firing` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | If specified, the bi-entity action to execute with the projectile owner the actor, and the projectile as the target as soon as the projectile is created.
`block_action_on_hit` | [Block Action Type](../block_action_types.md) | *optional* | If specified, the block action to execute on the block the projectile lands on upon having it land on it.
`bientity_action_on_miss` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, the bi-entity action to execute with the projectile owner as the actor, and the projectile as the target upon missing.
`bientity_action_on_hit` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, the bi-entity action to execute with the projectile as the actor, and the hit entity as the target upon hitting an entity.
`owner_target_bientity_action_on_hit` | [Entity Action Type](../entity_action_types.md) | *optional* | If specified, the bi-entity action to execute with the projectile owner as the actor, and the hit entity as the target upon hitting an entity.
`block_action_cancels_miss_action` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines if the `block_action_on_hit` action will cancel the `bientity_action_on_miss` action.
`block_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the block condition that the block targeted by the `block_action_on_hit` field must meet in order for that to run.
`bientity_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the bi-entity condition with the projectile as the actor and the target as the target for the projectile to actually hit the target instead of pass through.
`owner_bientity_condition` | [Block Condition Type](../block_condition_types.md) | *optional* | If specified, the bi-entity condition with the projectile owner as the actor and the target as the target for the projectile to actually hit the target instead of pass through.
`tick_bientity_action` | [Bi-entity Action Type](../bientity_action_types.md) | *optional* | If specified, the bi-entity action with the projectile owner as the actor, and the projectile as the target that is run each tick of the projectile's lifespan.
`key` | [Key](https://origins.readthedocs.io/en/latest/types/data_types/key/) |  | Which active key this power should respond to.


### Examples

```json
{
    "type": "apugli:custom_projectile",
    "entity_id": "example:realistic_brick",
    "texture_url": "https://freepngimg.com/thumb/bricks/8-2-bricks-png.png",
    "bientity_action_on_miss": {
      "type": "apoli:target_action",
      "action": {
        "type": "apoli:and",
        "actions": [
          {
            "type": "apoli:execute_command",
            "command": "playsound minecraft:block.stone.break player @a ~ ~ ~ 1 0.7"
          },
          {
            "type": "apoli:spawn_particles",
            "particle": {
              "type": "minecraft:item",
              "params": "minecraft:brick"
            },
            "count": 8,
            "speed": 0.1,
            "spread": {
              "x": 2.0,
              "y": 0.0,
              "z": 2.0
            }
          }
        ]
      }
    },
    "owner_target_bientity_action_on_hit": {
      "type": "apoli:and",
      "actions": [
        {
          "type": "apoli:damage",
          "source": {
            "name": "brick.player"
          },
          "amount": 8
        }
      ]
    },
    "count": 8,
    "divergence": 2.0,
    "speed": 0.8
}
```
This example action will let an entity fire a custom projectile with the use key, the projectile has the id `example:realistic_brick` and is textured like a high resolution brick. this spawns particles and plays a sound upon missing, and damages entities upon being hit by the brick. The brick flies at a speed of 2.0.