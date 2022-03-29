---
title: Modify Equipped Item Render (Power Type)
date: 2022-03-05
---

# Modify Equipped Item Render

[Power Type](../power_types.md).

Renders an item on an entity as if it were worn by them.

Type ID: `apugli:modify_equipped_item_render`

!!! note

    This power type only works if said entity can visibly carry an item in that slot. For example villagers are only allowed head slot powers whereas players can use any slot with this power.

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`slot` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | | Which equipment slot to render the item at. One of: `"mainhand"`, `"offhand"`, `"head"`, `"chest"`, `"legs"`, `"feet"`.
`stack` | [Item Stack](https://origins.readthedocs.io/en/latest/types/data_types/item_stack/) |  | The item stack to render on the entity's head.
`scale` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | The scale to render the item stack if this is rendering on the player's head. (This does not effect helmets)
`override` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | Determines whether the power overrides existing equipment from rendering.
`merge_with_held` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | `false` | If the equipment slot is set to the mainhand or offhand, this determines whether the power merges with the held item in the third person view.

### Example
```json
{
  "type": "apugli:modify_equipped_item_render",
  "equipment_slot": "HEAD",
  "stack": {
    "item": "minecraft:brown_carpet",
    "tag": "{CustomModelData:1}"
  },
  "scale": 1.5
}
```
This example would render brown carpet with a CustomModelData of 1 at 1.5 scale on the entity's head.

```json
{
  "type": "apugli:modify_equipped_item_render",
  "equipment_slot": "MAINHAND",
  "stack": {
    "item": "minecraft:diamond_sword"
  },
  "override": true
}
```
This example would render a diamond sword in the entity's hand overriding any existing item in the entity's hand.