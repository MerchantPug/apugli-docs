---
title: Entity Actions
date: 2022-01-08
---

# Entity Actions

Entity Action Types operate on an Entity. Some more specific actions only have an effect on more specific entity types (e.g. [Exhaust (Entity Action Type)](https://origins.readthedocs.io/en/latest/types/entity_action_types/exhaust/) only works on a `PlayerEntity`, as other entities do not have a hunger bar). These are available to power/action types that provides a `entity_action` object field.

## Apugli
- [Explode (Apugli)](explode)
- [Raycast](raycast)
- [Zombify Villager](zombify_villager)