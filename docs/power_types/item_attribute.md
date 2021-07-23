---
title: Item Attribute (Power Type)
date: 2021-07-22
---

# Item Attribute

[Power Type](../power_types.md).

Adds an additional attribute modifier to item stacks. These attributes also show up in the description of the item.

Type ID: `apugli:item_attribute`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`modifier` | Attributed Attribute Modifier | *optional* | If specified, this modifier will be applied to its corresponding attribute.
`modifiers` | Array of Attributed Attribute Modifiers	|*optional* | If specified, these modifiers will be applied to their corresponding attributes.

### Example
```json
{
  "type": "apugli:entity_group",
  "group": "player_undead"
}
```
This power marks the player as Player Undead, meaning they will take 60% of the enchantment level's damage from Smite and will have the Instant Health and Instant Damage effects swapped.