---
title: Bi-entity Action Types
date: 2022-07-29
---

# Bi-entity Action Types

Bi-entity Action Types operate on a `Pair<Entity, Entity>`; in simpler terms: an actor and a target. The actor and target is determined depending on the used power type, and can be swapped using Invert. These are available to power/action types that provides a `bientity_action` object field.

As a rule of thumb, the actor is usually the entity that "triggers" the action (e.g. uses or attacks another entity), while the target is the entity that is being targeted (e.g. the entity that is being used or attacked).

## Apugli
- [Change Hits on Target](change_hits_on_target)
- [Raycast Between](raycast_between)
- [Spawn Custom Effect Cloud](spawn_custom_effect_cloud)