---
title: Change Hits on Target (Bi-entity Action Type)
date: 2021-06-20
---

# Change Hits on Target

[Bi-entity Action Type](../bientity_action_types.md).

Changes the value which the [Hits On Target](../bientity_condition_types/hits_on_target.md) bi-entity condition checks for.

Type ID: `apugli:change_hits_on_target`

!!! note
    This only effects the [Hits On Target](../bientity_condition_types/hits_on_target.md) condition, this does not mess with any base Minecraft stuff involving damage source tracking.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`change` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | *optional* | This value will be either added to or set as the hits on target check.
`operation` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"add"` | Determines if the action should add or set the value of the hits on target check. Accepts `"add"` or `"set"`.
`timer_change` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | *optional* | This value will be either added to or set as the hits on target check's timer. This will be reset to 0 if it goes above the Apugli config's `resetTimerTicks` value (default 100).
`timer_operation` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"add"` | Determines if the action should add or set the value of the timer relating to hits on target. Accepts `"add"` or `"set"`.

### Example
```json
"bientity_action": {
    "type": "apugli:change_hits_on_target",
    "change": 0,
    "operation": "set"
}
```
This example sets the amount of times that the actor has hit the target to 0.