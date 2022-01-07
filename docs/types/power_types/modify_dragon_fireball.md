---
title: Modify Dragon Fireball (Power Type)
date: 2021-06-20
---

# Modify Dragon Fireball

[Power Type](../power_types.md).

Can modify certain values of any dragon fireball the player uses, whether this be through the item form or the Dragonborn origin.

Type ID: `toomanyorigins:modify_dragon_fireball`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`damage_modifier` | [Attribute Modifier](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, this modifier will apply to the damage amount.
`damage_modifiers` | [Array of Attribute Modifiers](https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier/) | *optional* | If set, these modifiers will apply to the damage amount.
`min_radius` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | Sets the radius to the amount of blocks specified at the start of the AoE's life.
`max_radius` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | *optional* | Sets the radius to the amount of blocks specified at the end of the AoE's life.
`duration` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |  | Specifies the duration that the AoE Entity is out for.

### Example
```json
{
  "type": "toomanyorigins:modify_dragon_fireball",
  "modifier": {
    "name": "Extra damage for dragon fireball",
    "operation": "addition",
    "value": 3.0
  },
  "min_radius": 4.0,
  "max_radius": 2.0,
  "duration": 20
}
```
This power makes dragon fireballs last for 1 second, start with an 8 block diameter, end with a 4 block diameter and deal 1.5 more hearts of damage.