---
title: Custom Hurt Sound (Power Types)
date: 2022-02-19
---

# Custom Hurt Sound

[Power Type](../power_types.md)

Modifies the sound being played if the entity that has the power is hurt.

Type ID: `apugli:custom_hurt_sound`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`muted` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines if the hurt sound should be muted.
`sound` | [Weighted Sound Events](../data_types/weighted_sound_event.md) | *optional* | If specified, this sound event will play instead of the original hurt sound of the entity that has the power.
`sounds` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Weighted Sound Events](../data_types/weighted_sound_event.md)  | *optional* | If specified, these sound events will play in a random fashion instead of the original hurt sound of the entity that has the power.
`volume` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | Determines the volume of the sound event(s) being played.
`pitch` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | Determines the pitch of the sound event(s) being played.


### Examples

```json
{
    "type": "apugli:custom_hurt_sound",
    "sound": "minecraft:entity.enderman.hurt"
}
```

This example will replace the hurt sound of the entity that has the power with the `minecraft:entity.enderman.hurt` sound event.
<br>

```json
{
    "type": "apugli:custom_hurt_sound",
    "sounds": [
        "minecraft:entity.enderman.hurt",
        {
            "sound": "minecraft:entity.axolotl.hurt",
            "weight": 4
        },
        "minecraft:entity.villager.hurt",
        "minecraft:entity.pillager.hurt"
    ]
}
```

This example will replace the hurt sound of the entity that has the power with the `minecraft:entity.enderman.hurt`, `minecraft:entity.axolotl.hurt`, `minecraft:entity.villager.hurt` and `minecraft:entity.pillager.hurt` sound events in a random fashion. The `minecraft:entity.axolotl.hurt` sound has a 4/7 chance to play whereas the others only have a 1/7 chance to play.
