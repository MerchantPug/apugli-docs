---
title: Damage (Apugli) (Item Action Type)
date: 2021-10-02
---

# Cooldown

[Item Action Type](../item_action_types.md)

Sets the cooldown of the stack's associated item.

Type ID: `apugli:cooldown`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`ticks` | [Integer](../data_types/integer.md) | `20` | The amount of ticks that the cooldown should be active for.

### Examples

```json
"item_action": {
    "type": "apugli:cooldown",
    "ticks": 200
}
```

This example will set the stack's item to 200 ticks/10 seconds. This will affect all items of this type.