---
title: Damage (Apugli) (Item Action Type)
date: 2021-10-02
---

# Damage (Apugli)

[Item Action Type](../item_action_types.md)

Damages the item stack with a specified amount.

Type ID: `apugli:damage`

!!! note

    If you do not need to display the break animation upon having this item break, please use Apoli's [Damage (Item Action Type)](https://origins.readthedocs.io/en/latest/types/item_action_types/damage/) instead.

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`amount` | [Integer](../data_types/integer.md) | `1` | The amount of damage it should do to the item stack.
`ignore_unbreaking` | [Boolean](../data_types/boolean.md) | `false` | Determines if this action should ignore the Unbreaking enchantment.



### Examples

```json
"item_action": {
    "type": "apugli:damage",
    "amount": 10,
    "ignore_unbreaking": true
}
```

This example will damage the item stack by 10, ignoring the Unbreaking enchantment.
