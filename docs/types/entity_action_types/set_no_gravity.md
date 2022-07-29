---
title: Set No Gravity (Entity Action Type)
date: 2022-07-29
---

# Set No Gravity

[Entity Action Type](../entity_action_types.md).

Sets whether the entity is affected by gravity or not.

Type ID: `apugli:set_no_gravity`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`value` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | *optional* | The value to set the `NoGravity` flag to. If not set it'll change the value to the opposite of what it currently is.


### Example
```json
"entity_action": {
    "type": "apugli:set_no_gravity",
    "value": true
}
```
This action makes the entity unaffected by gravity.