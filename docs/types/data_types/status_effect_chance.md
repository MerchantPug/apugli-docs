---
title: Status Effect Chance (Data Type)
date: 2022-01-08
---
# Item Stack

[Data Type](../data_types.md).

An [Object](https://origins.readthedocs.io/en/latest/types/data_types/object/) which defines a status effect with a chance.

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`effect` | [Status Effect Instance](https://origins.readthedocs.io/en/latest/types/data_types/status_effect_instance/) | | The status effect instance which is used when the chance is successful.
`chance` | 

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