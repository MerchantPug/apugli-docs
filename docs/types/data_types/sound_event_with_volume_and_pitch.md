---
title: Sound Event with Volume and Pitch (Data Type)
date: 2022-02-19
---
# Sound Event with Volume and Pitch

[Data Type](../data_types.md).

Either a [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) that defines the sound event or an [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) which defines a sound event with pitch and volume.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the sound to play.
`volume` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1` | The volume at which the sound will play.
`pitch` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1` | The pitch at which the sound will play.

### Examples:

```json
"sound": "minecraft:entity.pig.hurt"
```
A `minecraft:entity.pig.hurt` sound event.

```json
{
    "sound": "minecraft:entity.pig.death",
    "volume": 2,
    "pitch": 0.5
}
```

This will play the `minecraft:entity.pig.death` sound event at a volume of 2 and a pitch of 0.5 if selected.