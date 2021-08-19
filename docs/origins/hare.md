---
title: Hare (Origin)
date: 2021-08-19
---
# Hare

[Origin](../misc/origins.md). ID: `toomanyorigins:hare`

A race of nature-bound rabbits that had attained a level of awareness akin to humans. They inherited their proficient mobility.

## Powers

Name | ID | Description (In-Game) | Description (Detailed)
-----|----|-----------------------|------------------------
Bunny Hop | `toomanyorigins:bunny_hop` | You build up momentum while in the air which is added to your movement speed. You keep built up momentum momentarily while on the ground. You may also gain momentum with your active ability. | You gain 0.000375 velocity to your current movement direction every 10 ticks (capped at 0.015 extra velocity / 40 velocity updates) whenever you aren't on the ground, in water, in lava, in a vehicle (boat, horse, etc), fall flying or not moving at all. Upon meeting any of these conditions you keep your momentum for a maximum of 4 ticks before losing it if you continue to meet the condition. Your active power (default: G) adds 15 velocity updates (37.5% of max) to your current amount of velocity updates. This active power has a cooldown of 40 seconds and may not be used when your velocity is at its maximum value.
Photophobia | `toomanyorigins:photophobia` | You are unable to sleep in bright light. | You cannot sleep in a bed that is placed in a light level above 9.
Sugary Delicacy | `toomanyorigins:sugary_delicacy` | Carrots and Golden Carrots are more filling for you. They also give you Speed 1 for 8 seconds after consumption. | Consuming items in the `toomanyorigins:carrots` tag gives you 4 more hunger shanks and gives you a speed effect for 8 seconds.
Large Leap | `toomanyorigins:large_leap` | While standing still your jump height has increases. | While standing still you can jump about 2 blocks high.
Lightweight | `toomanyorigins:lightweight` | You have 2 less hearts of health than humans. | You have 8 hearts.
Vegetarian | `origins:vegetarian` | You can't digest any meat | You cannot eat food items defined in the tag origins:meat, unless they are also defined in the `origins:ignore_diet` tag.