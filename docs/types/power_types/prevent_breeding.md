---
title: Prevent Breeding (Power Type)
date: 2022-03-25
---

# Prevent Breeding

[Power Type](../power_types.md).

Prevents the power holder from breeding `AnimalEntity`s that meet the bi-entity condition.

Type ID: `apugli:prevent_breeding`

### Fields
Field  | Type | Default | Description
-------|------|---------|-------------
`bientity_condition` |	[Bi-entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | *optional* | The bi-entity condition type to check for with the power holder as the actor and the entity the actor is attempting to breed as the target.
`bientity_action` |	[Bi-entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/) | *optional* | The bi-entity action type to execute upon failing to breed an entity with the power holder as the actor and the entity the actor is attempting to breed as the target.
`prevent_follow` |	[Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | *optional* | Whether this power type prevents entities from following the power holder when a breeding item is held.

### Example
```json
{
  "type": "apugli:prevent_breeding",
  "bientity_condition": {
    "type": "origins:target_condition",
    "condition": {
       "type": "origins:tamed",
       "inverted": true
    }
}
```
This example prevents the entity from breeding any animals that aren't tamed.