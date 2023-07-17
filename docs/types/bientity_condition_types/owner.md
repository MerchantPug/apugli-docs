---
title: Owner (Bi-entity Condition Type)
date: 2021-06-20
---

# Owner

[Bi-entity Condition Type](../bientity_condition_types.md).

Checks if the target entity has the actor entity as its owner.

Type ID: `apugli:hits_on_target`

!!! note
    Unlike Apoli's `owner` bi-entity condition. This is additionally able to pick up the owner for projectiles and area effect clouds. If you're just using a Tameable entity, you can use that.

### Fields

*None.*

### Example
```json
{
    "type": "apugli:owner"
}
```
This example checks if the target entity has the actor entity as the owner.