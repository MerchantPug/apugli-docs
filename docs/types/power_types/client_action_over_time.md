---
title: Client Action Over Time (Power Type)
date: 2021-04-10
---

# Client Action Over Time

[Power Type](../power_types.md)

An [Action Over Time (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/action_over_time/) that runs on the client instead of the server.

Type ID: `apugli:client_action_over_time`


### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`interval` | [Integer](../data_types/integer.md) | `20` | Interval of ticks between subsequent executions of the specified actions. Must be a value of at least 1.
`entity_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | The action to execute on the entity that has the power each interval.
`rising_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | The action to execute on the first interval tick in which the condition became true.
`falling_action` | [Entity Action Type](../entity_action_types.md) | _optional_ | The action to execute on the first interval tick in which the condition became false.


### Examples

```json
{
  	"type": "apugli:client_action_over_time",
  	"entity_action": {
        "type": "apoli:add_velocity",
        "y": 2,
        "server": false
  	},
  	"interval": 20
}
```
This example will launch the entity upwards on the client every 20 ticks.
