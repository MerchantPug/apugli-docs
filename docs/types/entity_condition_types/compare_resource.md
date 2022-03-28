---
title: Compare Resource (Entity Condition)
date: 2022-03-29
---

# Compare Resource

[Entity Condition](../entity_condition_types.md).

Compares the value of two powers that use the [Resource (Power Type)](https://origins.readthedocs.io/en/latest/types/power_types/resource/) or a power type that has a built-in cooldown (using remaining ticks as the value).

Type ID: `apugli:compare_resource`

!!! note

    This condition requires the entity it's checking to have both powers. It will return false if this isn't met.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`resource` | The namespace and ID of a power that will be evaluated.
`compare_to` | The namespace and ID of a power that will be compared to the power in the `resource` field.
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)	| `">="` | How the `resource` power's value which are the specified should be compared to the `compare_to` power's value.

### Example
```json
"condition": {
  "type": "apugli:compare_resource",
  "resource": "apugli:test_resource_one",
  "compare_to": "apugli:test_resource_two",
  "comparison": "<="
}
```
This example checks if an entity's value of `apugli:test_resource_one` resource power is less than or equal to the value of its `apugli:test_resource_two` resource power.