---
title: Player Model Type (Entity Condition Type)
date: 2022-07-29
---

# Player Model Type

[Entity Condition Type](../entity_condition_types.md).

Check whether an `AbstractClientPlayerEntity` uses the `DEFAULT` or `SLIM` model type.

Type ID: `apugli:player_model_type`

!!! caution

    This condition is only effective client-side. That means any server-sided power types will not work as intended.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`model_type` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | The model type to check for. Can be either `"default"` OR `"slim`.

### Example
```json
"condition": {
    "type": "apugli:entity_in_radius",
    "model_type": "default"
}
```
This condition checks whether the `AbstractClientPlayerEntity` has a default (Steve) player model type.