---
title: Custom Footstep
date: 2022-02-18
---

# Custom Footstep

[Power Type](../power_types.md)

Modifies the footstep sound of the entity that has the power.

Type ID: `apugli:custom_footstep`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`muted` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether the footstep should be muted.
`sound` | [Weighted Sound Event](../data_types/weighted_sound_event.md) | *optional* | If specified, this sound event is played.
`sounds` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Weighted Sound Events](../data_types/weighted_sound_event.md) | *optional* | If specified, these sound events are played in a random fashion.
`volume` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float) | `1.0` | Determines the volume of the sound event(s) being played.
`pitch` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float) | `1.0` | Determines the pitch of the sound event(s) being played.


### Examples

```json
{
    "type": "apugli:custom_footstep",
    "sound": "minecraft:block.amethyst_block.break"
}
```

This example will replace the footstep of the entity that has the power with the `minecraft:block.amethyst_block.break` sound event.
<br>

```json
{
    "type": "apugli:custom_footstep",
    "muted": true,
    "condition": {
        "type": "apoli:on_block",
        "block_condition": {
            "type": "apoli:in_tag",
            "tag": "minecraft:wool"
        }
    }
}
```

This example will mute the footstep of the entity that has the power if the said entity is standing on any kind of Wool block.
