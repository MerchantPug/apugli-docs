---
title: Entity Action Types
date: 2022-01-08
---

# Entity Action Types

Entity Action Types operate on an Entity. Some more specific actions only have an effect on more specific entity types (e.g. [Exhaust (Entity Action Type)](https://origins.readthedocs.io/en/latest/types/entity_action_types/exhaust/) only works on a `PlayerEntity`, as other entities do not have a hunger bar). These are available to power/action types that provides a `entity_action` object field.

## Apugli
- [Add Velocity (Apugli)](add_velocity)
- [Explode (Apugli)](explode)
- [Explosion Raycast](explosion_raycast)
- [Fire Projectile](fire_projectile)
- [Set No Gravity](set_no_gravity)
- [Spawn Particles](spawn_particles)
- [Zombify Villager](zombify_villager)

## Deprecated

!!! CAUTION
    These types are under potential removal in future versions as there's a better way of handling what these types can do in either Apoli or Apugli. Avoid using these unless you have to.

- [Raycast](raycast)
    - Succeeded by [Raycast (Entity Action Type)](https://origins.readthedocs.io/en/latest/types/entity_action_types/raycast/).
    - Only use this if you need to access the entity's reach, if you need to raycast in a specific direction, or if you need a piercing effect.
- [Resource Transfer](resource_transfer) 
    - Succeeded by [Modify Resource (Entity Action Type)](https://origins.readthedocs.io/en/latest/types/entity_action_types/modify_resource/).
- [Spawn Item](spawn_item)
    - Summon an item through commands for this one.