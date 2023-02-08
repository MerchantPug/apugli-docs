---
title: Entity Condition Types
date: 2022-01-08
---

# Entity Condition Types

Entity Condition Types operate on an Entity, which also allows access to the world. These are available to be used in most powers in the `condition` object field (or `entity_condition` in other power/condition types), which restricts when a power is active.

## Apugli
- [Attacker Condition](attacker_condition)
- [Attack Target Condition](attack_target_condition)
- [Can Have Effect](can_have_effect)
- [Compare Resource](compare_resource)
- [Entity In Radius](entity_in_radius)
- [Hostile](hostile)
- [Join Invulnerability Ticks](join_invulnerability_ticks)
- [Key Pressed](key_pressed)
- [Particle In Radius](particle_in_radius)
- [Player Model Type](player_model_type)
- [Structure](structure)
- [Velocity](velocity)

## Deprecated

!!! CAUTION
    These types are under potential removal in future versions as there's a better way of handling what these types can do in either Apoli or Apugli. Avoid using these unless you have to.

- [Max Health](max_health)
    - Succeeded by [Attribute (Entity Condition Type)](https://origins.readthedocs.io/en/latest/types/entity_condition_types/attribute/).
- [Raycast](raycast)
    - Succeeded by [Raycast (Entity Condition Type)](https://origins.readthedocs.io/en/latest/types/entity_condition_types/raycast/).
    - Only use this if you need to access the entity's reach.