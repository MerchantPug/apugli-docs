---
title: Home
date: 2021-01-08
---

# Welcome to the Apugli / TooManyOrigins Documentation

Before reading this documentation, please have a decent understanding of Apoli powers/Origins datapacking as this has information that builds from there.
Read up on the [Origins Documentation](https://origins.readthedocs.io/en/latest/) before asking any questions.

You can visit [CurseForge](https://www.curseforge.com/minecraft/mc-mods/toomanyorigins) or [Modrinth](https://modrinth.com/mod/toomanyorigins) to download TooManyOrigins which includes Apugli as a library.

Likewise with TooManyOrigins you can visit [CurseForge](https://www.curseforge.com/minecraft/mc-mods/cursedorigins) or [Modrinth](https://modrinth.com/mod/cursedorigins) to download CursedOrigins.

## General Information
* This entire documentation is accurate to v1.2.1 of Apugli, v0.3.2 of TooManyOrigins and v2.0.0 of CursedOrigins.
* If you would like to discuss anything on this wiki or discuss the mods, feel free to join the [TooManyOrigins/CursedOrigins Discord Server](https://discord.gg/UBfEjsANNz)
* Thank you to Ultra for allowing me to use `moborigins:nearby_entities` from Mob Origins. I've expanded on this condition to make it more in line with `apoli:block_in_radius` but this condition saved me a lot of time.

## TooManyOrigins Tags
* Dragonborn gets which of the two abilities are used from the lightable tag. If you have any modded furnaces/campfires you are able to add them to the tag `(toomanyorigins/tags/blocks/lightable)`.
* If you would like to make an item not protect Undead when worn on their head you are able to add the item to the tag `(toomanyorigins/tags/items/ignore_head_slot)`. Nothing is in this tag by default.
* Hare gets what is considered a carrot from the tag `(toomanyorigins/tags/items/carrots)`. If you have a modded carrot item or just want to give the hare a boost from eating something else you can add the food item to this tag.
* Withered gets what is considered a regular seed through the `(toomanyorigins/tags/items/crop_seeds)` tag and gets what is considered a stem seed through the `(toomanyorigins/tags/items/stem_seeds)`.