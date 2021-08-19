---
title: Food Component (Data Type)
date: 2021-08-19
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
<br>

```json
{
  	"food_component": {
		"hunger": 5,
        "saturation": 12.4,
        "always_edible": true,
        "snack": true
  	}
}
```

A food component that recovers 5 hunger and 12.4 saturation. It is always edible and counts as a snack.