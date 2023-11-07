---
title: Power Types
date: 2022-03-05
---

# Power Types

Power Types are what grants functionality to your origins! Each power has a type, specified with a `type` field in the JSON. Which type a power is defines which other fields it requires and supports.

Unless stated otherwise, each power type supports a condition field that can check for [Entity Condition Types](entity_condition_types.md). See [Power JSON](https://origins.readthedocs.io/en/latest/json/power/) for more details.

## Apugli

#### Regular Types
- [Allow Anvil Enchant](allow_anvil_enchant)
- [Bunny Hop](bunny_hop)
- [Custom Death Sound](custom_death_sound)
- [Custom Footstep](custom_footstep)
- [Custom Hurt Sound](custom_hurt_sound)
- [Custom Projectile](custom_projectile)
- [Edible Item](edible_item)
- [Energy Swirl](energy_swirl)
- [Entity Texture Overlay](entity_texture_overlay)
- [Force Particle Render](force_particle_render)
- [Hover](hover)
- [Instant Effect Immunity](instant_effect_immunity)
- [Invert Instant Effects](invert_instant_effects)
- [Mobs Ignore](mobs_ignore)
- [Redirect Lightning](redirect_lightning)
- [Step Height](step_height)

#### Action-related
- [Action On Attacker Hurt](action_on_attacker_hurt)
- [Action On Block Placed](action_on_block_placed)
- [Action On Bonemeal](action_on_bonemeal)
- [Action On Durability Change](action_on_durability_change)
- [Action On Equip](action_on_equip)
- [Action On Projectile Hit](action_on_projectile_hit)
- [Action On Target Death](action_on_target_death)
- [Action On Target Hurt](action_on_target_hurt)
- [Action On Tame Hit](action_on_tame_hit)
- [Action When Projectile Hit](action_when_projectile_hit)
- [Action When Tame Hit](action_when_tame_hit)
- [Client Action Over Time](client_action_over_time)
- [Projectile Action Over Time](projectile_action_over_time)

#### Modifying types
- [Modify Block Placed](modify_block_placed)
- [Modify Breeding Cooldown](modify_breeding_cooldown)
- [Modify Durability Change](modify_durability_change)
- [Modify Enchantment Damage Dealt](modify_enchantment_damage_dealt)
- [Modify Enchantment Damage Taken](modify_enchantment_damage_taken)
- [Modify Enchantment Level](modify_enchantment_level)
- [Modify Equipped Item Render](modify_equipped_item_render)
- [Modify Soul Speed](modify_soul_speed)

#### Preventing types
- [Prevent Bee Anger](prevent_bee_anger)
- [Prevent Breeding](prevent_breeding)
- [Prevent Label Render](prevent_label_render)
- [Prevent Sound](prevent_sound)

## Deprecated

!!! CAUTION
    These types are under potential removal in future versions as there's a better way of handling what these types can do in either Apoli or Apugli. Avoid using these unless you have to.

- [Aerial Affinity](aerial_affinity)
    - Succeeded by [Modify Break Speed (Apoli)](https://origins.readthedocs.io/en/latest/types/power_types/modify_break_speed/).
- [Set Texture](set_texture)
    - Succeeded by [Entity Texture Overlay](entity_texture_overlay).
- [Rocket Jump](rocket_jump)
    - Succeeded by a specific configuration of [Active Self (Apoli)](https://origins.readthedocs.io/en/latest/types/power_types/active_self/). See the [toomanyorigins:overheat](https://github.com/MerchantPug/toomanyorigins/blob/1.19.4/Common/src/main/resources/data/toomanyorigins/powers/overheat.json) power JSON for more information. 
<br>

## TooManyOrigins

#### Modifying types
- [Modify Dragon Fireball](modify_dragon_fireball)