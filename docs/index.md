---
title: Home
date: 2021-01-08
---

# Welcome to the Apugli Documentation
**This is also the TooManyOrigins documentation!**

Before reading this documentation, please have a decent understanding of Apoli/Origins datapacking as this has information that builds from there.
Read up on the [Origins Documentation](https://origins.readthedocs.io/en/latest/) before asking any questions.

You can visit [Apugli on CurseForge](https://www.curseforge.com/minecraft/mc-mods/apugli) or [Apugli on Modrinth](https://modrinth.com/mod/apugli) to download Apugli.

You can alternatively visit [TooManyOrigins on CurseForge](https://www.curseforge.com/minecraft/mc-mods/toomanyorigins) or [TooManyOrigins on Modrinth](https://modrinth.com/mod/toomanyorigins) to download TooManyOrigins which includes Apugli as a library.

## General Information
* If you would like to discuss anything on this wiki or discuss the mods, feel free to join the [Pug's Modzone Discord Server](https://discord.gg/UBfEjsANNz).
* Thank you to UltrusBot for allowing me to use `moborigins:nearby_entities` from Mob Origins. I've expanded on this condition to make it more in line with `apoli:block_in_radius` but this condition saved me a lot of time early on.
* Thank you to Mantarri for sparing me your wrath when I stole your code back in 1.16.5 CursedOrigins. Similar to what's stated above, I have since swapped out this code for my own code.
* You are able to use the `ope` namespace for any Apugli powers. This is also true for `toomanyorigins` if you have it installed.

## TooManyOrigins Tags
* Dragonborn gets which of the two active powers are used from the lightable tag. If you have any modded furnaces/campfires you are able to add them to the tag `(toomanyorigins/tags/blocks/lightable)`.
* If you would like to make an item not protect Undead when worn on their head you are able to add the item to the tag `(toomanyorigins/tags/items/ignore_head_slot)`. Nothing is in this tag by default.
* Hare gets what is considered a carrot from the tag `(toomanyorigins/tags/items/carrots)`. If you have a modded carrot item or just want to give the hare a boost from eating something else you can add the food item to this tag.
* Withered gets what is considered a regular seed through the `(toomanyorigins/tags/items/crop_seeds)` tag and gets what is considered a stem seed through the `(toomanyorigins/tags/items/stem_seeds)`.