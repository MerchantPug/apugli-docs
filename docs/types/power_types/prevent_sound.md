---
title: Prevent Sound (Power Types)
date: 2022-02-19
---

# Prevent Sound

[Power Type](../power_types.md)

Prevents sound events from being heard by the entity that has the power.

Type ID: `apugli:prevent_sound`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`category` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | If specified, all sound events from this category will be prevented from being heard by the entity that has the power. Can accept `"ambient"`, `"blocks"`, `"hostile"`, `"master"`, `"music"`, `"neutral"`, `"players"`, `"records"`, `"voice"` and `"weather"`.
`categories` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Strings](https://origins.readthedocs.io/en/latest/types/data_types/string/) | *optional* | If specified, all sound events from these categories will be prevented from being heard by the entity that has the power. Can accept `"ambient"`, `"blocks"`, `"hostile"`, `"master"`, `"music"`, `"neutral"`, `"players"`, `"records"`, `"voice"` and `"weather"`.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, this sound event will be prevented from being heard by the entity that has the power.
`sounds` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, these sound events will be prevented from being heard by the entity that has the power.
`whitelist` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | If specified, these sound events will be exempt from being prevented.


### Examples

```json
{
    "type": "apugli:prevent_sound",
    "categories": [
        "BLOCKS"
    ],
    "whitelist": [
        "minecraft:block.glass.break"
    ]
}
```

This example will prevent sound events from the `BLOCKS` sound category from being heard by the entity that has the power except for the `minecraft:block.glass.break` sound event.
