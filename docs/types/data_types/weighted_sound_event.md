---
title: Weighted Sound Event (Data Type)
date: 2022-02-19
---
# Weighted Sound Event

[Data Type](../data_types.md).

Either a [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) that defines the sound event or an [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) which defines a sound event with volume and pitch alongside weight.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`sound` | [Sound Event With Volume and Pitch](sound_event_with_volume_and_pitch.md) | | The namespace and ID of the sound to play along with pitch and volume.
`sounds` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Sound Event With Volume and Pitch](sound_event_with_volume_and_pitch.md) | | The namespace and ID of the sounds to play along with pitch and volume.
`weight` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The weight for the sound effect to play in a randomiser. The higher this is, the more likely it'll be selected.

### Examples:

```json
"sound": "minecraft:entity.pig.hurt"
```
A `minecraft:entity.pig.hurt` sound event.

```json
{
    "sound": "minecraft:entity.pig.death",
    "weight": 5
}
```

This weighted sound event has a weight of 5 and will play the `minecraft:entity.pig.death` sound event if selected.