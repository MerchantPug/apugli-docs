---
title: Custom Entity Id (Entity Condition Type)
date: 2022-10-30
---

# Custom Entity Id

[Entity Condition Type](../entity_condition_types.md).

Checks for the Entity ID associated with a Custom Projectile or Custom Area of Effect Cloud.

Type ID: `apugli:custom_entity_id`

!!! note

    This condition will always return false if used outside of a Custom Projectile or Custom Area of Effect Cloud.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_id` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The entity id to cehck 

### Example
```json
"condition": {
    "type": "apugli:custom_entity_id",
    "entity_id": "example:fireball"
}
```
This example checks if a custom entity has an entity id of `example:fireball`.