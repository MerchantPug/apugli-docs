---
title: Prevent Label Render (Power Type)
date: 2022-02-18
---

# Prevent Label Render

[Power Type](../power_types.md)

Prevents the name tag label of the entity that has the power from rendering.

Type ID: `apugli:prevent_label_render`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_condition` | [Entity Condition Type](https://origins.readthedocs.io/en/latest/types/entity_condition_types) | *optional* | If specified, only entities that fulfills this entity condition type will **not** see the name tag label of the entity that has the power.
`bientity_condition` | [Bi-entity Condition Type](https://origins.readthedocs.io/en/latest/types/bientity_condition_types) | *optional* | If specified, only entities which fulfills this bi-entity condition type in relation to the entity that has the power will **not** see the name tag label of the entity that has the power.


### Examples

```json
{
    "type": "apugli:prevent_label_render",
    "entity_condition": {
        "type": "apoli:in_block_anywhere",
        "block_condition": {
            "type": "apoli:fluid",
            "fluid_condition": {
                "type": "apoli:in_tag",
                "tag": "minecraft:water"
            }
        },
        "comparison": ">=",
        "compare_to": 1
    }
}
```

This example will prevent the name tag label of the entity that has the power from rendering to entities that has their eyes or feet in water.
