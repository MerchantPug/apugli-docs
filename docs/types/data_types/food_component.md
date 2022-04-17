---
title: Food Component (Data Type)
date: 2022-01-08
---
# Item Stack

[Data Type](../data_types.md).

An [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) which defines a new food component.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`hunger` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The amount of hunger shanks the food component recovers upon consumption.
`saturation` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | | The amount of saturation to give the player upon consumption.
`meat` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether this food component counts as meat or not.
`always_edible` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether this food component is edible at full hunger or not.
`snack` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Whether this food component takes as long as dried kelp to eat (16 ticks) or not (32 ticks).
`effect` | [Status Effect Chance](status_effect_chance.md) | *optional* | A status effect and the chance of it triggering upon consuming something with this food component.
`effects` | [Array](https://origins.readthedocs.io/en/latest/types/data_types/array/) of [Status Effect Chances](status_effect_chance.md) | *optional* | A status effect and the chance of it triggering upon consuming something with this food component.

### Examples:

```json
{
  	"food_component": {
		"hunger": 4,
        "saturation": 1.0
  	}
}
```

A food component that recovers 4 hunger and 1 saturation.