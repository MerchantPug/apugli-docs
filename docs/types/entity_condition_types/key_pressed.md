---
title: Key Pressed (Entity Condition Type)
date: 2022-03-29
---

# Key Pressed

[Entity Condition Type](../entity_condition_types.md).

Checks if the entity is actively using a keybind on their client.

Type ID: `apugli:key_pressed`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`key` | [Key](https://origins.readthedocs.io/en/latest/types/data_types/key/) |  | The key to check.


### Example
```json
"condition": {
  "key": {
    "key": "key.use",
    "continuous": true
  }
}
```
This example checks if the entity is continually holding the `key.use` keybind.