---
title: Undead (Origin)
date: 2021-07-13
---
# Undead

[Origin](../origins.md). ID: `toomanyorigins:undead`

A rare genetic mutation allows this race to keep their humanity despite suffering the effects of the Infection.

## Powers

Name | ID | Description (In-Game) | Description (Detailed)
-----|----|-----------------------|------------------------
*hidden* | `toomanyorigins:burn_timer` | *none* | When choosing this origin or respawning, you gain an ability cooldown that functions as a timer. When this timer is recharged it allows `toomanyorigins:no_helmet_burn` to activate as long as that ability's other conditions are met.
Deathly Bite | `toomanyorigins:deathly_bite` | Your melee attacks inflict a Zombifying effect on non undead mobs for a short time. Hitting any villager that has this effect zombifies them. | Your melee attacks inflict a zombifying effect on non Undead entities for 4.5 seconds.
Husk of a Former Self | `toomanyorigins:no_helmet_burn` | After 1 minute and 30 seconds of spawning in you burn in sunlight unless headwear is worn. | After `toomanyorigins:burn_timer` has ended its cooldown you start to burn in sunlight unless you wear something in your head slot that isn't part of the `toomanyorigins:ignore_head_slot` tag or use fire resistance.
Opposite Day | `toomanyorigins:opposite_day` | Instant Health and Instant Damage have the reverse effect. You are also immune to Regeneration, Hunger and Zombifying. | Sets your entity group to `player undead` swapping the effects of Instant Health and Instant Damage and making you take 60% of any extra damage from the Smite enchantment.
Cannibalism | `toomanyorigins:cannibalism` | Rotten Flesh is more nutritious for you. | Consuming Rotten Flesh gives you 5 more Hunger shanks and 10 more saturation.
Torn Lungs | `toomanyorigins:torn_lungs` | You exhaust much quicker than others, thus requiring you to eat more. | Everything you do exhausts you 60% more.
*hidden* | `toomanyorigins:zombify_hit` | *none* | If you hit a Villager with a melee attack while they are under the effect of the Zombifying status effect they will convert into a Zombie Villager.
*hidden* | `toomanyorigins:undead_immunities` | *none* | You are not effected by regeneration, hunger and zombifying effects.