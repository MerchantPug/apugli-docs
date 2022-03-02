---
title: Custom Death Sound (Power Types)
date: 2022-02-19
---

# Custom Death Sound

[Power Type](../power_types.md)

Modifies the sound being played if the entity that has the power dies.

Type ID: `apugli:custom_death_sound`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`muted` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether the death sound should be muted.
`sound` | [Weighted Sound Event](../data_types/weighted_sound_event.md) | *optional* | If specified, this sound event will play instead of the original death sound of the entity that has the power.
`sounds` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Weighted Sound Events](../data_types/weighted_sound_event.md) | *optional* | If specified, these sound events will play instead of the original death sound of the entity that has the power in a random fashion.
`volume` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | Determines the volume of the sound event(s) being played.
`pitch` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | Determines the pitch of the sound event(s) being played.


### Examples

```json
{
    "type": "apugli:custom_death_sound",
    "muted": true
}
```

This example will mute the death sound of the entity that has the power.
<br>

```json
{
    "type": "apugli:custom_death_sound",
    "sound": "minecraft:entity.axolotl.death"
}
```

This example will replace the death sound of the entity that has the power with the `minecraft:entity.axolotl.death` sound event.
