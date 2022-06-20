---
title: Light Up (Block Action Type)
date: 2021-08-19
---

# Light Up

[Block Action Type](../block_action_types.md).

A block action that lights up furnaces, campfires and brewing stands.

Type ID: `apugli:light_up`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`burn_time` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1600` | The number of ticks that a furnace is lit for.
`brew_time` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `20` | The amount of fuel given to a brewing stand upon use.
`light_campfire` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `true` | Whether this action should light up campfires.
`particle` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | ID of the particle type to use.
`particle_count` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | *optional* | The amount of particles to spawn when the block lights up.
`sound` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | *optional* | ID of the sound to play when the block lights up.


### Example
```json
{
    "block_action": {
        "type": "apugli:light_up_block",
        "burn_time": 2600,
        "brew_time": 20,
        "light_campfire": false,
        "particle": "minecraft:dragon_breath",
        "particle_count": 15,
        "sound": "minecraft:entity.ender_dragon.shoot"
    }
}
```
This block action lights up any furnace for 2600 ticks or fills a brewing stand. Successfully lighting a block releases 15 dragon breath particles from the block and will play an ender dragon shoot sound effect. This ignores campfires.