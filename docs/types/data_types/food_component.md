---
title: Food Component (Data Type)
date: 2022-01-08
---
# Item Stack

[Data Type](../data_types.md).

An [Object](object.md) which defines a new food component.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`hunger` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | | The amount of hunger shanks the food component recovers upon consumption.
`saturation` | [Float](https://origins.readthedocs.io/en/latest/data_types/float/) | | The amount of saturation to give the player upon consumption.
`meat` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | `false` | Whether this food component counts as meat or not.
`always_edible` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | `false` | Whether this food component is edible at full hunger or not.
`snack` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | `false` | Whether this food component takes as long as dried kelp to eat (16 ticks) or not (32 ticks).
`effect` | [Status Effect Chance](status_effect_chance) | *optional* | A status effect and the chance of it triggering upon consuming something with this food component.
`effects` | [Array of Status Effect Chances](status_effect_chance) | *optional* | A status effect and the chance of it triggering upon consuming something with this food component.

### Examples:

```json
{
  	"food_component": {
		"hunger": 4,
        "saturation": 1.0
  	}
}
```

An food component that recovers 4 hunger and 1 saturation.