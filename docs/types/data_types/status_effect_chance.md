---
title: Status Effect Chance (Data Type)
date: 2022-01-08
---
# Status Effect Chance

[Data Type](../data_types.md).

An [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) which defines a status effect with a chance.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Status Effect Instance](https://origins.readthedocs.io/en/latest/types/data_types/status_effect_instance/) | | The status effect instance which is used when the chance is successful.
`chance` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The chance for the status effect to trigger.

### Examples:

```json
{
  	"effect": {
		"effect": "minecraft:slowness",
		"amplifier": 1,
		"duration": 80
	},
	"chance": 0.8
}
```

This is a Slowness II effect that lasts for 80 ticks with a chance that has an 80% chance of triggering.