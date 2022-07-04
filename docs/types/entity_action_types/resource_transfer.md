---
title: Resource Transfer (Entity Action Type)
date: 2022-06-01
---

# Resource Transfer

[Entity Action Type](../entity_action_types.md).

Transfers a value from a "provider" resource into a resource.

Type ID: `apugli:resource_transfer`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`resource` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the power that uses the [Resource (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/resource/) or has a built-in cooldown to transfer the value from `provider` into.
`provider` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | | The namespace and ID of the power that uses the [Resource (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/resource/) or has a built-in cooldown to use for the value transfer.


### Example
```json
"entity_action": {
    "type": "apugli:resource_transfer",
    "resource": "test:inactive_resource",
    "provider": "test:active_resource"
}
```
This action transfers the value from `test:active_resource` to `test:inactive_resource`