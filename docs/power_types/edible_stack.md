---
title: Edible Stack (Power Type)
date: 2021-07-14
---

# Edible Stack

[Power Type](../power_types.md).

A power that makes any item that matches an item condition edible.

Type ID: `apugli:edible_stack`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/item_conditions/) |  | The item condition that items must satisfy to be affected by this power.
`hunger` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | | How much hunger an item gives upon eating it.
`saturation` | [Float](https://origins.readthedocs.io/en/latest/data_types/float/) | | How much saturation an item gives upon eating it.
`meat` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | `false` | Whether the item counts as meat.
`always_edible` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | `false` | Whether the item can be eaten when the player's hunger bar is full.
`snack` | [Boolean](https://origins.readthedocs.io/en/latest/data_types/boolean/) | `false` | Whether the item takes half the amount of time to eat when compared to regular food (see Dried Kelp)
`effect` | [Status Effect Instance](https://origins.readthedocs.io/en/latest/data_types/status_effect_instance/) |	*optional* | If set, this status effect will be applied by this power.
`effects` | [Array](https://origins.readthedocs.io/en/latest/data_types/array/) of [Status Effect Instances](https://origins.readthedocs.io/en/latest/data_types/status_effect_instance/) | *optional* |If set, these status effects will be applied by this power.
`tick_rate` | [Integer](https://origins.readthedocs.io/en/latest/data_types/integer/) | `10` | The frequency (in ticks) with which to set the items that satisfy the condition's foodcomponents. Lower values set the component quicker, but this comes at a potentially huge performance cost.

### Example
```json
{
  "type": "apugli:edible_stack",
  "item_condition": {
    "type": "apoli:ingredient",
    "ingredient": {
      "item": "minecraft:axolotl_bucket"
    }
  },
  "hunger": 4,
  "saturation": 1,
  "meat": true
}
```
This power allows for axolotl in buckets to be edible. Eating an axolotl in a bucket gives 4 hunger shanks and 1 saturation, it also counts as meat.