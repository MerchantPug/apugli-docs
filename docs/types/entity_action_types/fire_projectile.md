---
title: Fire Projectile (Entity Action Type)
date: 2022-06-01
---

# Fire Projectile

[Entity Action Type](../entity_action_types.md).

Fires a projectile.

Type ID: `apugli:fire_projectile`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`count` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1 `| The amount of projectiles to fire each use.
`speed` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.5` | The speed applied to the fired projectile.
`divergence` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | How much each projectile fired is affected by random spread.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If set, the sound with this ID will be played when the power is used.
`tag` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | NBT data of the entity.
`bientity_action` | [Bi-entity Action](../bientity_action_types.md) | *optional* | A bi-entity action to execute with the user as the actor and the projectile as the target upon creating the projectile.


### Example
```json
"entity_action": {
    "type": "apugli:fire_projectile",
    "speed": 2.0,
    "entity_type": "minecraft:arrow",
    "tag": "{pickup:0}"
}
```
This action fires an arrow at a speed of 2 that cannot be picked up. 