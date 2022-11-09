---
title: Hits on Target (Bi-entity Condition Type)
date: 2021-06-20
---

# Hits on Target

[Bi-entity Condition Type](../bientity_condition_types.md).

Checks the amount of times a target has been hit within a time interval.

Type ID: `apugli:hits_on_target`

!!! note
    The interval at which this bi-entity condition's hits reset depends on the Apugli config's resetTimerTicks value.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`comparison` | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/) | `">="` | How the amount of times the actor has hit the target should be compared to the specified value.
`compare_to` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | `1` | The value to compare the amount to.


### Example
```json
{
    "bientity_condition": {
        "type": "apugli:hits_on_target",
        "comparison": "==",
        "compare_to": 0
    }
}
```
This example checks if the actor has not hit the target.