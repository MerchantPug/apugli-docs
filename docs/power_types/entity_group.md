---
title: Apugli Entity Group (Power Type)
date: 2021-06-20
---

# Apugli Entity Group

[Power Type](../power_types.md).

Defines the entity group of the player, mostly used for determining enchantment bonus damage towards the player. A player should only have one of this or `origins:entity_group`.

If you'd like to use the vanilla entity groups use `origins:entity_group` instead.

Type ID: `apugli:entity_group`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`group` | [String](https://origins.readthedocs.io/en/latest/data_types/string/) |  | The group to associate with the player. One of `smiteable` or `player_undead`

### Example
```json
{
  "type": "apugli:entity_group",
  "group": "player_undead"
}
```
This power marks the player as Player Undead, meaning they will take 60% of the enchantment level's damage from Smite and will have the Instant Health and Instant Damage effects swapped.