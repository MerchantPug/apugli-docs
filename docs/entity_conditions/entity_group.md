---
title: Apugli Entity Group (Entity Condition)
date: 2021-06-20
---

# Apugli Entity Group

[Entity Condition](../entity_conditions.md).

Checks whether the entity is of a specific entity group.

If you'd like to use the vanilla entity groups use `origins:entity_group` instead.

Type ID: `apugli:entity_group`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`group` | [String](https://origins.readthedocs.io/en/latest/data_types/string/) |  | Entity group required for the entity to pass the check. One of `smiteable` or `player_undead`

### Example
```json
"condition": {
  "type": "apugli:entity_group",
  "group": "smiteable"
}
```
This example checks if the entity is included in the `smiteable entity group`.