---
title: "Changelog"
weight: 8
type: docs
description: >
  *I shall explain to you the mysteries of the outer realms.*
---

## Release 4.18.0.1

> 2023-07-03

Just a quick fix for a few issues I noticed personally. For starters, I've removed multiple Apothecary patches in lieu of a unified Anniversary Update patch. That should make the recipes more consistent and up to date. Then I noticed a lot of issues with the *New Armory Series - Lunar Weapons* integration. That's on me as I didn't properly check over it after reverting away from the TPF 5.0 beta. They should have the proper enchantments and tooltips now, and vanilla Silent Moons weapons should no longer appear.

Other than that, tiny quality of life changes. Stealing items undetected will give Sneak exp based on the value of what was stolen. Potions are no longer distractingly bright (but still emit some light). And [Photo Mode](https://www.nexusmods.com/skyrimspecialedition/mods/91701)! Access it from the System Menu or just hit `P`.

**This update is save-safe for 4.18 users.**

<details>

#### Changes
- **SKSE Plugins - Tweaks:** Added Skill of Sneaking
- **Interface:** Added Photo Mode
- **ElSopa's Potions Redone:** Added ElSopa Potions Redone - Less Emissive and Fixed Inventory Size
- **ElSopa's Potions Redone:** Added ElSopa Potions Redone - Less Emissive and Fixed Inventory Size - Xtudo ELIF Patch
- **Alchemy, Cooking, & Farming:** Removed Apothecary - Fishing Patch
- **Alchemy, Cooking, & Farming:** Removed Apothecary - Rare Curios Patch
- **Alchemy, Cooking, & Farming:** Removed Apothecary - Saints and Seducers Patch
- **Alchemy, Cooking, & Farming:** Removed Apothecary - Hearthfire Crispy Dumplings Patch
- **Alchemy, Cooking, & Farming:** Added Apothecary Anniversary Update
- **Alchemy, Cooking, & Farming:** Added Apothecary Anniversary Update - Food and Drink Addon
- **Survival & Fishing:** Removed Apothecary - Food and Drink Addon - Survival Mode Patch
- **Saints & Seducers:** Added Apothecary Anniversary Update - SECSS 
- **New Items:** Removed Ancient Nord Stalhrim - Ebony Assets
- **Final Patches:** Edited Enchantable Special Item Fix - TPF Patch to include Lunar Weapons, adjusted incorrect Silver Weapons stats
- **Conflict Resolution Patch:** Removed Cooked Boar Meat removal as it's properly handled by the Apothecary Anniversary Update
- **Conflict Resolution Patch:** Removed Poisoned Apple recipe edits to no longer require Solvency (Alchemy 60)
- **Conflict Resolution Patch:** Incorporated necessary Apothecary - Hearthfire Crispy Dumplings Patch changes
- **Conflict Resolution Patch:** Modified New Armory Series - Lunar Weapons effects to better match Thaumaturgy

#### Updates

- Updated MQ105SprintTriggerScript Fix to 1.0.1
- Updated Assorted Mesh Fixes to 0.83
- Updated Lux (main plugin) to 6.2
- Updated Lux Orbis (main plugin) to 3.3
- Updated Embers XD to 2.7.7
- Updated Adamant - A Perk Overhaul to 5.8.2 
- Updated Stormcrown - A Shout Overhaul to 1.1.7
- Updated Simplicity of Seeding to 0.4
- Updated Ancient Nord Stalhrim to 1.2.4.1
- Updated Tamrielic Distribution to 1.3.3.1

</details>

## Release 4.18.0

> 2023-06-29

This update has been simmering for a long time and I apologize to everyone who's had to wait patiently while its aroma drifted over them. But the wait is over: **4.18 is here!**

Let's start with the visuals. I've removed some more deviations I've made from Aurora such as *eFPS* and *Enhanced Landscapes* so that the visuals are more in line with Phoenix's amazing work. I've also switched back to *Realistic Water Two* which is Aurora's water mod of choice. We're still using RAID Weathers and The Vanilla ENB 2 since I want stealth mechanics to remain predictable in a game with no stealth meter. *Frozen Electrocuted Combustion* has also been removed. It's a good mod but there are some weird interactions and ultimately the effects take away some of the visual oomph of the late-game Destruction perks. (I still haven't sorted out the LOD unload bug in the winter, unfortunately. If you experience it, just save and reload where you are.)

Gameplay is where the meat of the update lies. *[Stormcrown](https://www.nexusmods.com/skyrimspecialedition/mods/90659)* has been added alongside the *Adamant - Bard Perks Addon* to move shouts into a perk tree everyone can benefit from and add more functionality to Speech tree respectively. As such, shouts as a whole have a different approach compared to *Forceful Tongue* and I've updated the Example Builds section to account for the changes. Enemy resistances have also changed slightly with a switch to *[Enemy Resistance Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/59394)*. Last but not least of the big gameplay changes is the removal of *Honed Metal*. It's been in the list a long time but it's been hard to balance it the way I've wanted *and* its features are quickly becoming redundant. Instead of removing it in a few months I've decided to rip the bandaid off now. The [gameplay guide](/skyrim-se/sss/gameplay-guide) has been updated to reflect this as well.

**THIS UPDATE IS NOT SAVE-SAFE.** Please start a new game. Please.

(Unless you've been using the 4.17.1 beta. Then you can install this after first Uninstalling Honed Metal via its MCM. *Stormcrown* also made some changes since 1.1.4 that might result in funkiness so a new game is *encouraged* but not required.)

<details>

#### Changes

- Applied changes from [Skyrim Modding Essentials 2.4.2](https://publish.obsidian.md/tpf/meta/changelogs/sme/sme-2-4-2), [2.4.3](https://thephoenixflavour.com/skyrim-se/sme/changelog/#release-243), and [Aurora 1.3](https://publish.obsidian.md/tpf/meta/changelogs/aur/aur-1-3)
- **Utilities & Frameworks:** Removed Constructible Object Custom Keyword System - Separate Weapon and Armor
- **Utilities & Frameworks:** Added Constructible Object Custom Keyword System - Light Usability Tweaks
- **Utilities & Frameworks:** Added Custom Skills Framework
- **General Fixes:** Added Self-targeting Staff Animation Fix
- **Script Fixes:** Added MQ105SprintTriggerScript Fix
- **Script Fixes:** Added DLC2AudioRepeaterActivator01Script Tweak
- **(Optional) Nordic UI:** Removed NORDIC UI - Compass Navigation Overhaul
- **Mesh Improvements:** Removed Better Windhelm Ground Meshes - Valunstrad
- **Mesh Improvements:** Removed Solitude Objects SMIMed - Solitude Well
- **Mesh Improvements:** Removed Solitude Objects SMIMed - Castle Dour Spire
- **Yuril's Mesh Edits:** Removed FYX - Eastern Empire Company Building - eFPS Patch
- **Graphics Baseline:** Removed eFPS - Exterior FPS Boost
- **Graphics Baseline:** Removed Unofficial eFPS Patches
- **Graphics Baseline:** Removed Revamped Assets Skyrim - Weapon Racks Patch
- **Landscape:** Removed Enhanced Landscapes (and relevant patches)
- **Snow & Ice:** Removed Snowy Landscapes in Snowy Regions
- **Seasons of Skyrim:** Moved section to match Aurora documentation
- **Seasons of Skyrim:** Removed Shrubs of Snow
- **Seasons of Skyrim:** Added Seasonal Landscapes
- **Seasons of Skyrim:** Added Sowables of Skyrim - Snowy Versions
- **Lux Lighting:** Removed Mesh Patches for Lux Orbis (redundant)
- **Visual FX:** Removed Frozen Electrocuted Combustion (and relevant patches)
- **Water & Splash FX:** Swapped out Water for ENB for Realistic Water Two (and all related patches)
- **Improved Trees:** Removed Seasonal Aspen Trees - Turn of the Seasons Patch
- **Improved Trees:** Removed 3D Junipers - Trees and Berries
- **Improved Trees:** Removed Dead Shrubs Resized
- **Plants & Mushrooms:** Removed Cathedral - 3D Sword Ferns
- **Plants & Mushrooms:** Removed Cathedral - 3D Clover Plant
- **Plants & Mushrooms:** Removed Drier Cathedral - 3D Clover Plant
- **Plants & Mushrooms:** Removed Cathedral - 3D Lavender
- **Plants & Mushrooms:** Removed Cathedral - 3D Dragons Tongue
- **Plants & Mushrooms:** Removed Cathedral - 3D Nightshade
- **Plants & Mushrooms:** Removed Cathedral - 3D Deathbell
- **Plants & Mushrooms:** Removed Improved Gourds
- **Magic & Perks:** Removed Adamant - Speech Exp Based on Words
- **Magic & Perks:** Removed Forceful Tongue - Shouts Overhaul
- **Magic & Perks:** Removed Forceful Tongue - SimonRim Patch
- **Magic & Perks:** Removed Dragon Aspect Overhaul
- **Magic & Perks:** Added Adamant - Bard Perks Addon
- **New Mechanics:** Added Stormcrown - A Shout Overhaul
- **Magic & Perks:** Added Aetherius - Starting Spells Addon
- **Magic & Perks:** Added Aetherius - NPC Spell Absorption Addon
- **Crafting:** Removed Honed Metal
- **Crafting:** Removed Honed Metal Revoiced
- **Alchemy, Cooking, & Farming:** Removed HearthFires - Customizable Fertile Soil
- **Alchemy, Cooking, & Farming:** Added Simplicity of Seeding
- **Combat & Encounter Zones:** Removed Blade and Blunt - Sneak Addon
- **NPC Dialogue & Behavior:** Removed Misc Dialogue Edits and More Dialogue Options - TPF Patch
- **NPC Dialogue & Behavior:** Added Brawl Lines Expansion
- **NPC Dialogue & Behavior:** Added NPCs React to Invisibility
- **Combat & Encounter Zones:** Separated part out into a new Enemy Overhauls section
- **Combat & Encounter Zones:** Added Dynamic Random Dragons
- **Enemy Overhauls:** Removed Resistances & Weaknesses
- **Enemy Overhauls:** Removed Resistances & Weaknesses - NPC Armaments
- **Enemy Overhauls:** Added Enemy Resistance Tweaks
- **Enemy Overhauls:** Added Lore Friendly Ghosts
- **Quest Start Adjustments:** Added Delayed Quest Starts - Blood on the Ice
- **Immersion:** Removed Open World Loot - C.O.I.N. Patch
- **Miscellaneous:** Removed Misc Tweaks - No Starting Spells
- **Miscellaneous:** Removed Forceful Tongue - Durnehviir Resurrected Patch
- **Miscellaneous:** Added Stormcrown - Durnehviir Resurrected Patch
- **Miscellaneous:** Added Stormcrown - Unique Dragon Aspect Patch
- **Sound FX:** Removed Forceful Tongue - Audio Overhaul for Skyrim Patch
- **Skeleton & Animations:** Removed Dynamic Animation Replacer
- **Skeleton & Animations:** Added Open Animation Replacer
- **Survival & Fishing:** Added Fish Plaque Fixes and Improvements
- **Survival & Fishing:** Added U Can't Touch Fish
- **Mandragorasprouts' Statues:** Renamed section from Daedric Shrines
- **Mandragorasprouts' Statues:** Added Daedric Shrines - All in One - Azura Loading Screen
- **Mandragorasprouts' Statues:** Added Daedric Shrines - Hircine Skull Mask Version
- **Mandragorasprouts' Statues:** Added Statue of Kynareth
- **Mandragorasprouts' Statues:** Added Kynareth Replaces Talos - Civil War Consequence
- **New & Expanded Quests:** Added Caught Red Handed - NGCDT Patch
- **New Mechanics:** Removed Pilgrim - TPF Patch
- **New Mechanics:** Added Adamant - Bard Perks Addon - Pilgrim Integration
- **New Items:** Removed Royal Armory - TPF Patch
- **New Items:** Added Royal Armory - Plugin Replacer - Adjustments and Rebalancing for Thaumaturgy
- **New Animations:** Added Leviathan Animations II - Greatsword Sprint Attacks
- **New Animations:** Added Leviathan Animations II - Greatsword Power Attacks
- **Conflict Resolution:** Removed overwrite to `000C3691` as its no longer needed
- **Conflict Resolution:** Moved PlacedObject `000A9539` changes to CRP to remove Lux - TPF Patch
- **Conflict Resolution:** Moved DerkeethusCell `0002C993` changes to CRP to remove Lux - TPF Patch
- **Conflict Resolution:** Moved MAG_PoisonRuneFFLocation `0401D74C` changes to CRP to remove SimonRim - TPF Patch
- **Conflict Resolution:** Removed edits to MAG_VoiceUnrelentingForceEffect03 `0007F82F` to let Stormcrown do its thing
- **Conflict Resolution:** Swapped Forceful Tongue's WOOP edits for Stormcrown's
- **Conflict Resolution:** Added new shouts to Pilgrim's MAG_ShoutList `xx335269` for Talos' blessing
- **Conflict Resolution:** Forwarded necessary Aetherius changes
- **Conflict Resolution:** Resolved MAGShockImpact02 `00059ED8` in a different way
- **Conflict Resolution:** Cleaned up files that were no longer needed (hopefully!)

#### Updates

- Updated Fluency Themes to 1.4
- Updated Root Builder to 4.4.3
- Updated DynDOLOD to 3.00 Alpha-128
- Updated Payload Interpreter to 1.1
- Updated Versatile Item and Group Re-Assignment to 1.0.1.1
- Updated NPCs Names Distributor to 2.1.3
- Updated Weapons Armor Clothing and Clutter Fixes to 2.9.3
- Updated ConsolePlusPlus to 1.3
- Updated Keyboard Shortcuts Fix to 1.0.0.4
- Updated Dragonactorscript Infinite Loop Fix to 1.3.2
- Updated Assorted Mesh Fixes to 0.82
- Reverted Skyrim Skill Uncapper to vadfromnu's 0.1.7
- Updated Delphine's Map Reveals Dragon Mounds to 1.2
- Updated Compass Navigation Overhaul to 2.1.1
- Updated Spinning Load Screens to 1.1
- Updated NORDIC UI - Compass Markers Restored to 1.4.2
- Updated DynDOLOD Resources to 3.00 Alpha-37
- Updated xLODGen Resource - SSE Terrain Tamriel to 2.0
- Updated ENBSeries to 0.494
- Updated Lux to 6.2
- Updated Lux Ortbis to 3.3
- Updated Embers XD to 2.7.6
- Updated Rudy HQ - More Dramatic Red Mountain Plume to 1.2
- Updated Skyrim Remastered - Glaciers and Ice to 1.3
- Updated Icy Caves to 2.1.5
- Updated Icy Mesh Remaster to 2.20
- Updated Happy Little Logs to 1.7
- Updated HQ Vanilla Tiny Rocks to 2.4
- Updated Stony AF Markarth and Dwemer Ruins to 2.2
- Updated Imperial Armors and Weapons Retexture to 1.2
- Updated Elven Armors and Weapons Retexture to 1.01
- Updated Orcish Armors and Weapons Retexture to 1.1
- Updated Ebony Armors and Weapons Retexture to 1.21
- Updated Daedric Armors and Weapons Retexture to 1.2
- Updated Adamant - A Perk Overhaul to 5.8.1
- Updated Mundus - A Standing Stone Overhaul to 1.10.2
- Updated Mundus - A Standing Stone Overhaul - USSEP Patch to 1.0.1
- Updated Aetherius - A Race Overhaul to 2.11.7
- Updated Cooking Categories Improvement to 2.0.1
- Updated Misc Dialogue Edits to 1.9.2
- Updated Hunters Not Bandits to 4.1
- Updated Narrative Gameplay Consistent Dialogue Tweaks to 1.5.2
- Updated More Dialogue Options to 1.5
- Updated Immersive Rejections to 1.11
- Updated Ashlander Nomads Names to 1.1
- Updated Daedric Names to 1.2
- Updated Dovah Names to 1.1
- Updated Reachmen Tribes Names 1.2
- Updated Tamrielic Names to 1.1
- Updated Arena - An Encounter Overhaul
- Updated Blade and Blunt - A Combat Overhaul to 3.0.6
- Updated Blade and Blunt - Health Regeneration Addon to 1.1
- Updated Enemies Respect Encounter Zones to 1.4
- Updated Dragon War - A Dragon Overhaul to 3.0.6
- Updated Dragon War - Deadly Spell Impacts Patch to 3.0.6
- Updated Dragon War - Deiform Alduin Particle Lights Patch to 3.0.6
- Updated The Dragon Cult - A Draugr Overhaul to 1.3.5
- Updated At Your Own Pace - College of Winterhold to 2.1MG
- Updated The Choice is Yours (no version change)
- Updated Misc Dialogue Edits - Save the Icerunner Patch to 1.9.2
- Updated More Dialogue Options - Thieves Guild Reformation Patch to 1.5
- Updated Headhunter - Bounties Redone to 1.50
- Updated Destination Weddings to 1.5
- Updated Destination Weddings - Compatibility Patches to 1.5
- Updated Dragon War - Durnehviir Resurrected Patch to 3.0.6
- Updated Dragon War - Audio Overhaul for Skyrim Patch to 3.0.6
- Updated Dynamic Animation Casting to 3.2.4
- Updated Survival Mode Improved to 1.2
- Updated Turn of the Seasons to 1.0.7.1
- Updated Hand to Hand - An Adamant Addon to 1.5.4
- Updated New Armory Series - Lunar Weapons - A Silent Moons Overhaul to 1.6
- Updated Civil War Deserters to 2.0.1.1
- Updated GRAHL - Apothecary Patch to 15
- Updated Conditional Armor Type Animations to 1.3c
- Updated Vanargand Animations - Sprint to 1.3c
- Updated Vanargand Animations - Female Idle Walk and Run to 1.3.1c
- Updated Vanargand Animations - Male Idle Walk and Run to 1.3.1c
- Updated Leviathan Animations II - Sprint to 2.4c
- Updated Leviathan Animations II - Female Idle Walk And Run to 2.3c
- Updated Leviathan Animations II - Male Idle Walk And Run to 2.3c
- Updated Goetia Animations - Sprint to 1.0c
- Updated Goetia Animations - Female Idle Walk And Run to 1.2c
- Updated Goetia Animations - Male Idle Walk And Run to 1.3c
- Updated Take A Seat to 1.01
- Updated lilebonymace's Patches to 2.32

</details>

## Release 4.17.0.2

> 2023-05-18

This update was left on the backburner for a few reasons but I've decided to push it out today assuming the next update will require a new game. Why will the next update require a new game, you ask? Because [Stormcrown](https://www.nexusmods.com/skyrimspecialedition/mods/90659) released and some of you might have talked to Paarthurnax already. There are a few other mods that I'm thinking of switching out as well, so I'm considering this a good staging point for figuring out the next steps.

Another reason the update was stalled was because I wanted to update the Example Builds section a bit more. I haven't gotten around to all the changes I wanted to implement so the builds are slightly out of date with Simonrim. I plan on giving them all some polishing with the Stormcrown update as the shouts sections will obviously need adjusting.

The changelog looks lengthy but there aren't too many big changes. Just some gameplay updates to be aware of, such as the Blade and Blunt - Health Regeneration Addon. With this, you will regenerate Health back to 50% regardless of Survival mechanics, but you'll still need other means of recovery if you want to get back to full Health.

There's also a known LOD bug that's most noticeable in the Winter season. If you notice weird flickering or floating snow in your travels, just save and reload in place and it should fix itself. Hopefully this is fully fixed in newer versions of DynDOLOD, but for now it's something we have to live with.

<details>

#### Changes

- Cleaned up archives list, should lower the download size a fair amount
- Applied changes from [Skyrim Modding Essentials 2.3.3](https://publish.obsidian.md/tpf/meta/changelogs/sme/sme-2-3-3), [2.4](https://publish.obsidian.md/tpf/meta/changelogs/sme/sme-2-4), and [2.4.1](https://publish.obsidian.md/tpf/meta/changelogs/sme/sme-2-4-1) and [Aurora 1.1](https://publish.obsidian.md/tpf/meta/changelogs/aur/aur-1-1) and [1.2](https://publish.obsidian.md/tpf/meta/changelogs/aur/aur-1-2)
- **TPF 5.0 Fixes:** Removed Small Environmental Fixes (AO and Transition)
- **TPF 5.0 Fixes:** Removed Small Environmental Fixes - Fixes
- **Interface:** Temporarily disabled Compass Navigation Overhaul
- **Graphics Baseline:** Removed Skyland AIO - Parallax
- **Lux Lighting:** Removed Lux Via - Morthal Crash Fix
- **Lux Lighting:** Switched to Even Brighter Templates
- **Improved Trees:** Removed Happy Little Trees - Ivy on Trees
- **Magic & Perks:** Moved Adamant - Weapons Armor Clothing and Clutter Fixes Patch into lilebonymace's Patches
- **Alchemy, Cooking, & Farming:** Removed Book Covers Skyrim - Apothecary Patch
- **Alchemy, Cooking, & Farming:** Added Apothecary - Book Covers Skyrim Patch
- **Alchemy, Cooking, & Farming:** Moved Apothecary - Weapons Armor Clothing and Clutter Fixes Patch into lilebonymace's Patches
- **NPC Dialogue & Behavior:** Moved Thugs Not Assassins - Timing Is Everything Patch Fix into lilebonymace's Patches
- **Combat & Encounter Zones:** Added Blade and Blunt - Health Regeneration Addon
- **Quest Start Adjustments:** Moved The Choice Is Yours - DLC2 March of the Dead Fix Patch into lilebonymace's Patches
- **Quest Start Adjustments:** Moved The Choice Is Yours - Lod Dialogue Tweak into lilebonymace's Patches
- **Miscellaneous:** Moved Contraband Confiscated - USSEP Patch into lilebonymace's Patches
- **New & Expanded Quests:** Moved House of Horrors - No More Logrolf Houdini Patch into lilebonymace's Patches
- **New & Expanded Quests:** Moved House of Horrors - The Choice Is Yours Patch into lilebonymace's Patches
- **New Items:** Added aMidianBorn Armor Variants Lite - Modular Armory and Wolf Armors and Weapons Retextured Patch
- **New Items:** Added PrivateEye's Royal Armory - Loadscreen Models Update as a separate mod
- **New Creatures and Enemies:** Removed Skinshifters - Forsworn Doppelgangers
- **Conflict Resolution:** Resolved Leveled List conflict between Apothecary and Ish's Respec Mod `0009CD41`
- **Conflict Resolution:** Disabled EVG Conditional Idles' shield cover animations by default

#### Updates

- Updated Spell Perk Item Distributor to 6.6.1
- Updated MergeMapper to 1.5
- Updated Beautifully Overhauled and Objectively Better Icons Enriched for SkyUI to 1.4
- Updated Universal Cured Serana Eye Fix to 0.4
- Updated Assorted Mesh Fixes to 0.79
- Updated Skyrim Landscape and Water Fixes to 7.9
- Updated Don't Stay in the Water to 5.1
- Updated CoMAP - Common Marker Addon Project to 4.0
- Updated Whose Quest Is It Anyway (no version change)
- Updated ENBSeries to 0.493
- Updated Lux Via to 1.7
- Rolled Embers XD back to 2.7.3
- Updated Icy Mesh Remaster to 2.14
- Updated Cathedral - 3D Mountain Flowers - Base Object Swapperto 0.1.20
- Updated Unique Red Wave to 1.1
- Updated Mysticism - A Magic Overhaul to 2.2.4
- Updated Adamant - A Perk Overhaul to 5.7.8
- Updated Thaumaturgy - An Enchanting Overhaul to 1.3.3
- Updated Apothecary - An Alchemy Overhaul to 1.3.4
- Updated Lawless - A Bandit Overhaul to 2.0
- Updated Lawless - SimonRim Patch to 2.0
- Updated Lawless - Expanded Enemy Coverage Addon to 2.0
- Updated Lawless - Patch Collection to 2.0
- Updated Dragon War - A Dragon Overhaul to 3.0.3
- Updated Dragon War - Deadly Spell Impacts Patch to 3.0.3
- Updated Dragon War - Deiform Alduin Particle Lights Patch to 3.0.3
- Updated The Dragon Cult - A Draugr Overhaul to 1.3.3
- Updated At Your Own Pace - College of Winterhold to 2.0.1MG
- Updated Paarthurnax - Quest Expansion to 1.12
- Updated Immersive Display Overhaul to 1.3
- Updated Survival Mode Improved to 1.1.3
- Updated Destination Weddings to 1.4.1
- Updated Dragon War - Durnehviir Resurrected Patch to 3.0.3
- Updated Audio Overhaul for Skyrim to 4.1.3
- Updated Dragon War - Audio Overhaul for Skyrim Patch to 3.0.3
- Updated Caught Red Handed - Quest Expansion to 1.04
- Updated Hand to Hand - An Adamant Addon to 1.4.7
- Updated Gesture Animation Remix to 2.0

#### Outputs

- Reuploaded Nemesis (previous upload flagged for some reason)
- Regenerated Synthesis Patches
- Regenerated TexGen
- Regenerated DynDOLOD (and Performance)

</details>

## Release 4.17.0.1

> 2023-04-23

There were a few issues with the release of 4.17. Thank you SAEL in particular for catching the bulk of them and bringing them to my attention. The root cause of some was the Embers XD 2.7.4 beta, rather, the existing patches that did not account for it. Since I went through the trouble of fixing those, the beta stays in this version despite it being temporarily "retired" by mindflux on the Nexus. If that causes issues, I'll revert back to 2.7.3 and undo the fixes.

More importantly, *NPCs Learn Skills and Spells* has been removed. It was a fun experiment but now that Lawless and The Dragon Cult exist, we have a lot more intention with the enemy overhauling. We don't need SPID buffing up the enemies even more, and it turns out it was buffing them much more than intended. Sorry to everyone who ran into Lv1 bandits summoning atronachs, that should be fixed now.

Otherwise, it's a small update that follows its base list, [Aurora](https://www.nexusmods.com/skyrimspecialedition/mods/898050), in its official 1.0 release! Congrats to Phoenix for delivering another solid modlist to the community.

**This update is save-safe.**

<details>

#### Changes

- Applied changes from [Skyrim Modding Essentials 2.3.2](https://thephoenixflavour.com/skyrim-se/sme/changelog/#release-232) and [Aurora 1.0](https://publish.obsidian.md/tpf/meta/changelogs/aurora/aur-1-0)
- **Utilities & Frameworks:** Added Beautifully Overhauled and Objectively Better Icons Enriched for SkyUI
- **ElSopa's Potions Redone:** Added ElSopa - Potions Redone - Apothecary Patch
- **Magic & Perks:** Removed NPCs Learn Skills and Spells (as it's incorrectly processing NPCs)
- **Conflict Resolution:** Resolved differences between Embers XD and Frozen Electrocuted Combustion for FireFXShader `0001B212`
- **Conflict Resolution:** Resolved differences between Embers XD and No Edge Glow for DarkElfAncestorWrathFXShader `0010F56C`

#### Updates

- Updated Keyword Item Distributor to 3.0.2
- Updated Mesh Patches for Lux Orbis to 1.5.2
- Updated Embers XD to 2.7.4 Beta (No Version Change)
- Updated Stones of Solitude - Majestic Mountains Rocks to 1.2.1
- Updated Icy Mesh Remaster to 2.12
- Updated Immersive Rejections to 1.1
- Updated Lawless - SimonRim Patch to 1.6.2
- Updated The Dragon Cult - A Draugr Overhaul to 1.3.2

</details>

## Release 4.17.0

> 2023-04-17

There's no changelog here. There was one, once. It was massive and I lost it in the ether. After that there were hundreds of other changes made. I should do better. Another time, perhaps.

But this is a **huge** update, make no mistake. If you're coming from 4.16.0.*x*, just **make a new save file**. It's not save-safe. If you're coming from 4.16.1.*x* **you probably should also make a new save** but it's possibly salvageable. So what's changed?

As I mentioned in the last release candidate, Phoenix is back and they've changed their approach to TPF 5.0. It will be built on **Aurora** which is built on **Skyrim Modding Essentials**. This makes it very streamlined for Phoenix, building each list right on top of the other. So I've gone ahead and tossed out pretty much everything visual and also made this list based off of Aurora's release candidate (RC5 currently). It looks fantastic and the textures were selected with a lot more care than I'm capable of. I still kept RAID Weathers (and RAID), Water for ENB, and The Vanilla ENB Two, so it's not exactly the same as Aurora, but it's close.

The gameplay sections have moved around in anticipation for TPF 5.0. Phoenix has been posting their documentation and I can see how things are formatted for the future. I don't know which mods will be in TPF 5.0 so I've more or less smashed the current gameplay mod sections into their new separators and called it a day. When TPF comes out I will take notes on what direction Phoenix went in and adjust, but this list may just continue being an Aurora fork.

- Could I have been more discerning and gone through every mod to see if I still liked it? Sure.
- Will I do that at a later date? Probably.
- What's this then? I suppose technically it's still a SSS 5.0 beta, but the official WJ download has been neglected for awhile so I thought to bring everyone up to speed with this release.
- Does this need more polish? On the back end, sure. The game should play great and look great. I just need to clean things up from an organization perspective.

No, seriously, at some point I'll get around to cleaning up the load order and sorting out the CR patches to look less work-in-progress. But since the list is based off of two of Phoenix's release candidates, perhaps work-in-progress is how it's supposed to look.

Overall, I've taken Phoenix's visual overhaul from Aurora, trimmed down the added equipment from TPF 5.0, but otherwise kept its bug fixes and changes to quests/NPCs until TPF 5.0 is officially released. At which point I'll decide if I'm going to be a fork off Aurora or a fork off TPF and tweak accordingly.

tl;dr changes from 4.16.2 RC 1:  
- Visuals overhauled to match Aurora RC5
- Phoenix's Weapons & Armor Overhaul removed in lieu for a restored Weapons, Armor, Clothing, and Clutter Fixes
- Some of the added weapons and armor (e.g. Stalhrim Extra Crafting) was removed until balance can be better achieved
- Optional difficulty modules removed, Aurora optionals maintained

Thanks for listening to my TED Talk.

Seriously though, **start a new save file.**


## Release 4.16.2 RC 1

> 2023-03-05

It's been a few weeks since the last release candidate and we've found some issues that have been ironed out. The Uncapper should work as intended now with its latest update, Hulking Draugr shouldn't lower your attack speed into oblivion, and Simon has released a handful of fixes and updates before taking a well-deserved break. I'm still not entirely comfortable calling it a full release but we're close. Provided there's no huge issues with this update, it will go live on Wabbajack.

In other news, Phoenix has returned from their break! Alongside that news are changes to how they're approaching TPF 5.0 and their other lists and those changes will eventually trickle down into SSS. For instance, there will be a visuals-only list that will essentially replace the visuals here once it's released. I've recently taken visuals into my own hands with this release candidate but honestly I regret it and will love to put that back into Phoenix's hands. On that note, I've added the new xavbio armor and weapons textures where they've been patched for *Modular Armory*.

Other major additions for this release include a number of quality of life mods in the crafting world such as *Recipe Auto-Learn* and *Cooking Categories Improvement.* Crafting menus all around should be nicely sorted and discovering new alchemical effects should be a smidge less trial and error.

**This update is safe-save.** Just save in an interior cell before updating due to the change in DynDOLOD outputs.

Also, full disclosure, Lux updated everything in the final moments before pushing this update so I haven't had time to properly test out the changes (which haven't even been posted at this time) or re-run the LODs. There might be minor issues. This is precisely the type of thing I want to avoid by letting Phoenix handle the visuals.

<details>

#### Changes

- **SKSE Plugins:** Added Inventory Interface Information Injector
- **SKSE Plugins:** Added Recipe Auto-Learn
- **Interface:** Added Versatile Item and Group Re-Assignment
- **Interface:** Added Cooking Categories Improvement
- **Weather & Lighting:** Removed Enhanced Volumetric Lighting and Shadows
- **Landscape:** Removed Majestic Mountains - More Accurate Collision - AME Patch
- **Landscape:** Added Enhanced Rocks and Mountains - Majestic Mountains Patch
- **Trees, Grass, & Plants:** Added Cathedral - 3D Nightshade
- **Trees, Grass, & Plants:** Added Cathedral - 3D Dragons Tongue
- **Trees, Grass, & Plants:** Merged ENB Light Patch with Caveworm Plate Retexture
- **Apparel & Weapons:** Removed Modular Armory - Male Horns for Female Iron Helmet
- **Apparel & Weapons:** Added Iron Armors and Weapons Retexture
- **Apparel & Weapons:** Added Modular Armory - Iron Armors and Weapons Retexture Patch
- **Apparel & Weapons:** Added Steel Armors and Weapons Retexture
- **Apparel & Weapons:** Added Modular Armory - Steel Armors and Weapons Retexture Patch
- **Apparel & Weapons:** Added Orcish Armors and Weapons Retexture
- **Apparel & Weapons:** Added Modular Armory - Orcish Armors and Weapons Retexture Patch
- **Balance & Crafting:** Added Alchemy Recipe Expansion
- **Balance & Crafting:** Added Alchemy Recipe Expansion - Book Covers Skyrim Patch
- **Balance & Crafting:** Added Alchemy Recipe Expansion - Apothecary Patch
- **Non-Player Characters:** Added Vampire Lines Expansion
- **Non-Player Characters:** Added Vampire Lines Expansion - Orc Addon
- **Combat & Encounters:** Added Locational Encounter Zones
- **Conflict Resolution:** Hid 'Combat End Reset'spell from Seeking Out Sneaks from the effects menu

#### Updates

- Updated DynDOLOD to 3.00 Alpha-118
- Updated ENBSeries to 0.488
- Updated Root Builder to 4.4.2
- Updated Papyrus Tweaks to 4.1.0
- Updated Skyrim Landscape and Water Fixes to 7.6
- Updated powerofthree's Tweaks to 1.8
- Updated Bash Bug Fix to 3.0.0
- Updated Skyrim Skill Uncapper to 2.1.5
- Updated DynDOLOD Resources to 3.00 Alpha-31
- Updated Embers XD to 2.7.2
- Updated Parallax Spell Impacts 1.5
- Updated Majestic Mountains - Simplicity of Snow Patch to 1.1
- Updated Water for ENB to 1.76
- Updated Skyland - Happy Little Trees Bark to 1.2
- Updated Modular Armory to 1.3.1
- Updated Mysticism - A Magic Overhaul to 2.2.2
- Updated Aetherius - A Race Overhaul to 2.10.4
- Updated Canis Hysteria - The Werewolf Disease to 1.0.5
- Updated Forceful Tongue - Shouts Overhaul to 3.0.9.1
- Updated C.O.I.N. - Coins of Interesting Natures to 2.1.1.2
- Updated More Craftable Equipment to 1.4
- Updated AI Overhaul to 1.8.3
- Updated Bandit Lines Expansion to 1.07
- Updated Civil War Lines Expansion to 1.06
- Updated NPCs Wear Amulets of Mara to 2.03
- Updated The Dragon Cult - A Draugr Overhaul to 1.2.1
- Updated Headhunter - Bounties Redone to 1.43
- Updated Survival Mode Improved to 1.0.10
- Updated Skyrim Extended Cut - Saints and Seducers to 1.0.0.5
- Updated Saints & Seducers - Mysticism Rebalance to 2.2
- Updated Extended Cut Saints and Seducers - Mysticism Rebalance to 2.2
- Updated Mysticism - Survival Spells Addon to 1.0.2
- Updated Hand to Hand - An Adamant Addon to 1.4.4
- Updated East Empire Company Armor to 2.0.0.3
- Updated NPC Animation Remix to 1.3
- Updated Tamrielic Distribution to 1.3
- Updated Lux to 6.0
- Updated Lux Via to 1.6
- Updated Lux Orbis to 3.2

#### Outputs

- Regenerated Left Hand Weapon Meshes
- Regenerated LODGen
- Regenerated TexGen
- Regenerated DynDOLOD (and Performance)

</details>

## Release 4.16.1 RC 3

> 2023-02-13

It's been a little over a week and I've a short trip coming up so I wanted to put out an update before then. Thank you everyone that's been helping me test so far (and big thanks to Berna for finding some bugs to squash!) but I don't think it's quite ready for a full release just yet. This update is mostly just updates to existing mods, however one of those mods is *The Vanilla ENB Two* which had a huge update since RC 2 came out. Overall it's an amazing step forward and I love how it looks but it does come with a bit of a performance hit. I'm not sure if I tweaked the Performance Profile enough to compensate, but let me know if the hit's too much compared to the last release (and 4.16.0, even) so I can see what I can do about dialing it back.

**This update is save safe.** Nothing new has been generated. Have fun!

<details>

#### Changes

- **Weather & Lighting:** Removed Pouring Rain
- **Interiors:** Added Skyland Common and Upper Furniture
- **Clutter:** Removed upperclass meshes and furniture from Rudy HQ - Miscellaneous
- **New Animations:** Added Improved Table Transition Animations
- **Lux, Lux Orbis, & Lux Via:** Added Lux - Pilgrim - Daedric Shrines Patch (from Ro)
- **Conflict Resolution:** Add "No Grass in Cabin" changes (thanks to Berna)
- **Conflict Resolution:** Fixed Lunar Armory loadscreen (also thanks to Berna)
- **Conflict Resolution:** Removed `textures/landscape/grass/columbine.dds` from the ENB Complex Grass collection (hat trick for Berna)

#### Updates

- Updated powerofthree's Papyrus Extender to 5.5
- Updated Bash Bug Fix to 2.1.1
- Updated Skyrim Skill Uncapper to 2.1.3
- Updated Unique Map Weather to 1.1.1
- Updated Water for ENB to 1.74
- Updated Happy Little Trees - Ivy on Trees to 1.1.4
- Updated Animated Forge Water to 0.7
- Updated The Cost of a Mistake - Increased Guild Fines to 3.1
- Updated Misc Dialogue Edits to 1.8.5
- Updated Zim's Trainers Expansion to 1.1
- Updated Misc Dialogue Edits - Save the Icerunner Patch to 1.8.5
- Updated Blade and Blunt - A Combat Overhaul to 2.1.1
- Updated Unequip Quiver to 2.2
- Updated Snowy Surfaces Sound Collision and Aesthetics to 1.6.2
- Updated Headhunter - Bounties Redone to 1.42
- Updated Hand to Hand - An Adamant Addon to 1.4.3
- Updated Icy Mesh Remaster to 2.0
- Updated The Vanilla ENB Two to 2.0

</details>

## Release 4.16.1 RC 2

> 2023-02-05

Whoops, that was a quick update. This one's short but impactful. If your character plans on doing a lot of sneaking around I'd advise restarting. You don't have to but the values won't be the intended. If not, you probably won't notice too much difference other than the lighting.

*EVLaS* is gone for now. Will it come back? Possibly, but it would require a workable adjustment for *The Vanilla ENB Two* in order to prevent some of the intense outdoor shadows you may have encountered. Even with that fix, the shaodws the mod produces don't actually affect your current light level, so hiding in them won't make you stealthier. It's misleading and in a game with no other indicators, not good design. So I had to drop it.

I also updated *DWTD* values so that *R.A.I.D.*'s settings properly pass through. Since *RAID Weathers* was designed with stealth in mind, some of DWTD's features were doubling down on what NPCs were already experiencing. I've turned off some of those features and left others, such as NPCs hearing less in the rain or searching a small radius in bad weathers.

R.A.S.S. was removed because it was on the fence to begin with, half of the mod was turned off and the other half wasn't looking great in action. *S.W.I.F.T.* was removed because it trivialized some of the established methods of fast traveling (carriage, ferry, spells) that existed through other mods. The mod itself is great but it doesn't fit the list.

All in all, an update centered around mods with initializations.

<details>

#### Changes

- **Weather & Lighting:** Removed Enhanced Volumetric Lighting and Shadows (EVLaS)
- **Fire & Visual FX:** Removed R.A.S.S. - Rain Ash And Snow Shaders
- **Fire & Visual FX:** R.A.S.S. - Rain Ash And Snow Shaders - Settings Loader
- **Architecture:** Fixed Windhelm Bridge Stairs... again
- **Combat & Encounters:** Edited Dynamic Weather and Time Based Detection to properly detect RAID 3 plugins and set the correct settings
- **Skeletons & Animations:** Restored Missile's Immersive Equipment Display Presets
- **New Mechanics:** Removed Skyrim Wayshrines - Immersive Fast Travel
- **ENB:** Increased *AmbientLightingIntensityInteriorDay* and *AmbientLightingIntensityInteriorNight* to `1.00`

#### Outputs

- Regenerated DynDOLOD (and Performance)

</details>

## Release 4.16.1 RC 1

> 2023-02-04

This update should really be called *Slidikins' Strenuous Skyrim Release 5.0 RC 4* as it's essentially a complete rebuild of the list based off of *The Phoenix Flavour 5.0 RC 4* (which is currently unavailable). The changes in 4.15.5 was the first step towards this goal. The jump to SSE 1.6.640 in 4.16 put me within spitting distance. So, while I know that it's only been a week since that jump, I've decided to go the rest of the way.

The core of the list hasn't changed. It's still a Simonrim-centered TPF modlist with *Survival Mode* and my other choices, but TPF 5.0 has decided to venture off into the previously labeled "TPF-X" realm of added content. This update follows TPF down that path... some of the way. You'll find your Vanilla+ experience peppered with **new enemies, new equipment, expanded quests, more crafting options, and more**. What you won't find are the new worldspaces (areas), followers, or any content that requires the [Anniversary Upgrade](https://store.steampowered.com/app/1746860/The_Elder_Scrolls_V_Skyrim_Anniversary_Upgrade). If you have that, keep an eye out for TPF's release as it will integrate most of it very well.

There's a lot of changes here. Seriously. The folder count went from ~800 to ~1400. The plugin count is through the roof. Part of that is due to the conflict resolution patches being separated out by section instead of being altogether. This might not be the case in the final release, however there's no reason not to leave it as is with the way ESL plugins work.

Anyway, a not-so-shortlist of sectional changes can be found below. Please, *please* let me know if you run into any issues. I almost guarantee that you will. I want to fix them.

> **This update is absolutely not save-safe.** It is likely that future release candidates will be but not guaranteed. If you want to safely continue your character on v4.16.0.1, my advice would be to manually update SimonMagus' mods so long as they're labeled save-safe and you'll be in good shape.

<details>

#### Changes

This changelog is structured differently because of how much has changed. Instead of an itemized list, I'll go through section by section and list some key differences from each, compared to [TPF 5.0 RC 4](https://loadorderlibrary.com/lists/the-phoenix-flavour-50-wip).

- **Utilities:** No big changes here. This section consists of pre-requisites for other mods, most of which were already in the list. I did not carry over *Optional Quick Start* from TPF 5.0 as I'm not a fan of the implementation.

- **Essential Mods:** Phoenix created her own *Weapons & Armor Overhaul* that supercedes *WACCF* here, otherwise this section is mostly untouched. Numerous mods from this section have been moved to sections below.

- **SKSE Plugins:** The section has been moved higher. There are a number of new plugins, almost all of which are small quality of life fixes such as *Stagger Direction Fix* or *Alchemy Plus*.

- **Fixes & Tweaks:** Can you believe there are so many things to fix after USSEP? And it's all in here. Again, not going to get into the weeds over things that are small bug fixes. "It just works."

- **Controls & Camera:** This section also moved upwards. *Sprint Swimming* is the newest addition here, otherwise it's the same as before. I've switched away from the *EasyEase Preset* to [SmoothCam Vanilla Enhanced 2](https://www.nexusmods.com/skyrimspecialedition/mods/82481) with very minor changes.

- **Interface:** I kept *Toggle Compass Hotkey* over *Ultimate Immersion Toggle*. I've also reverted back to regular *SkyUI* as the default interface. This allows for more consistency with *CoMAP* and *Constructible Object Custom Keyword System*, both new additions in this update. There is an optional *Nordic UI* section for those who still want the old look but it's not at the same level of consistency. Widescreen support is still present for 21x9 monitors (*SkyUI* only; for other ratios or *Nordic UI* support you have to install it on your own). I've tried my best to make sure both UI looks work with the same configuration file.

- **Graphic Baseline:** Not much to say here. The Performance Profile does not utilize *High Poly Project* otherwise it's not an exciting section to talk about. To look at is a different story.

- **Mesh Improvements:** Likewise, TPF 5.0 just makes things look prettier here and I saw no reason to change these choices.

- **Weather & Lighting:** This is the first major departure from TPF 5.0. I've switched *Obsidian Weathers* out for *RAID Weathers* but left everything else the same. Previous versions of the list did not have reliable stealth mechanics which was a sore spot given the reduced HUD. By switching back to *RAID* and *RAID Weathers* sneaking around is tough but fair, the way I intended.

- **Fire & Visual FX:** I've added *R.A.S.S. - Rain Ash and Snow Shaders* on top of TPF 5.0. I've also kept all of my previous additions such as *Frozen Electrocuted Combusion*. I'm borderline on R.A.S.S. so please let me know what you think.

- **Landscape:** I kept pretty much everything here, the most noticeable of which was *Enhanced Landscapes* to make exploring a bit more memorable. Then I added a bunch of MystiriousDawn's new HD Parallax textures.

- **Trees, Grass, & Plants:** Essentially the same as TPF 5.0, which is the same as TPF 4.0 with the addition of *Happy Little Trees* and some of the *Cathedral - 3D* plants.

- **Appearance:** Unchanged as this section was adopted by SSS in earlier versions.

- **Architecture:** No real changes from TPF 5.0 aside from *Rally's Market Stalls*. Things look good here.

- **Misc Structures:** Again, no real changes. For the most part I've always agree with Phoenix's visuals and that hasn't changed.*Daedric Shrines* was put here as the only addition from a later section of the list.

- **Interiors:** Nothing to say here that hasn't already been said.

- **Dungeons:** The retexture section of the changelog is quite boring, isn't it?

- **Clutter:** I should note that TPF 5.0 switched from the desaturated version of *Book Covers Skyrim* to the saturated version. All the books in the game will be brighter than before.

- **Valuables:** For some reason *Security Overhaul SKSE* was moved here. Otherwise, nothing interesting to note.

- **Food & Ingredients:** I've added *Garlic - A Garlic Mod* to the section. It came out after the last release candidate but I feel that Phoenix would've loved it.

- **Apparel & Weapons:** Unchanged from TPF 5.0 as it was already incorporated into SSS awhile back.

- **Creatures:** Unchanged from TPF 5.0.

- **Gameplay Overhauls:** The SimonRim core of TPF remains untouched.

- **Balance & Crafting:** TPF 5.0 expands the crafting a good amount and SSS followed it all the way down that road. The biggest thing to note here is that TPF 5.0 modifies the Smithing tree along with its other changes. *Honed Metal* has not been adjusted to compensate so there may be some weirdness with the blacksmith services.

- **Non-Player Characters:** Children get more clothes with *Prince and the Pauper* returning to the list. Vigilants as well. Otherwise, this is a mostly unchanged section that introduces a few small tweaks to the list.

- **Improved Vanilla Quests:** TPF 5.0 fleshes this section out even more with a lot of minor tweaks. *At Your Own Pace* has been added for the main quest and the College of Winterhold. The other factions have gotten some attention as well to improve their quest pacing.

- **Combat & Encounters:** Nothing really changed here. Like Gameplay Overhauls, the core of the list hasn't changed.

- **Miscellaneous:** Phoenix added a number of small mods to this section such as *Jarrin Root for Babette*. *Left Hand Rings* is included so that the Bond of Matrimony can be worn without taking up a valuable enchantment slot. One that I didn't take was *Another Redbelly Mine Mod* because, put frankly, I don't care all too much about the dialogue conflict here. It's an easy mine to enter, let's leave it as an iron mine like all the other easy mines to enter.

- **Skeleton & Animations:** I left this mostly unchanged which is a departure from TPF 5.0 because it added *Movement Behavior Overhaul* and *Animated Armoury*. The former was glitchy for me and I didn't think the latter fit the current vision of the list and there are no added weapon types here, so I dropped them. *Precision* returns, however, as it was not the true source of the previous issue.

- **Sound FX:** I know less about sound than I do visuals. This section was left as is.

- **Creation Club:** This list only uses the 4 free Creations that came with Anniversary Edition so the others have been removed, drastically slimming down the next few sections.

- **Creation Club Base:** I did my best to preserve what could be used here with the above limitation which wasn't much. In addition, previous enhancements to *Saints and Seducers*, *Survival Mode*, and *Fishing* were moved here.

- **Creation Club Assets:** Unchanged from TPF 5.0 aside from the aforementioend trim.

- **Creation Club Patches:** Included everything necessary for the utilized Creations.

- **Creation Club Integreation:** This has been reduced to Phoenix's patches and *Mysticism - Survival Spells Addon*.

- **Beyond Skyrim Bruma, Wyrmstooth, City Overhauls, Other Locations, Interior Overhauls, and New Player Homes:** Not included in SSS.

- **New & Expanded Quests:** Some of these were introduced in the last update. Most, actually. I did not add *Cheesemod for EVERYONE* and *New Treasure Hunt*, however.

- **New Mechanics:** *Hand to Hand* and *Pilgrim*, among others, were already in the list. I've added *Skyrim Wayshrines* and *BA Bard Songs*. *Wayshrines* provides another alternative to fast traveling but you'll incur fatigue in exchange for the transmission. Left out were some CC-dependent mechanics, *Take A Peek*, *Skyrim's Got Talent*, and *Skyrim's Paraglider*.

- **New Items:** A lot. I mean, there's a lot of new, lore friendly gear to outfit yourself with here. Before it was just *Royal Armory* and *Ancient Nord Stahlrim*. Now it's a proper section.

- **New Creatures:** This was called "New NPCs & Creatures" in TPF 5.0 but I didn't carry over a single NPC so just ignore that first part. You still get plenty of new monsters to fight and a handful more alchemical ingredients to play around with from this section.

- **New Animations:** In addition to the previous animations I've added to the list, TPF 5.0 adds almost all of Verolevi's animations (with *Conditional Armor Type Animations*) to the game. In action all of these new animations looked nice and made sense, so I left them in.

- **New Music:** Nothing has changed here.

- **Content Integration:** Without certain CC mods the *Crossbow Integration* part of this section got neutered but I kept what I could. You should also see more Bonemold and Chitin and merchants will have more gear from across Tamriel even if you can't go there yourself.

- **Lux, Lux Orbis, & Lux Via:** These mods are so big they need their own section. I've included everything that was necessary given the other choices in the modlist.

#### Updates

- Updated Crash Logger to 1.8
- Updated Spell Perk Item Distributor to 6.4
- Updated Cathedral Weathers and Seasons - Unofficial Update to 2.40
- Updated Particle Patch for ENB to 1.2.3
- Updated Assorted Mesh Fixes to 0.78
- Updated Aetherius - A Race Overhaul to 2.10.3
- Updated Mundus - A Standing Stone Overhaul to 1.9.1
- Updated Snowy Surfaces Sound Collision and Aesthetics to 1.6.1
- Updated Hand to Hand - An Adamant Addon to 1.4.2
- Updated NPC Animation Remix to 1.2.1

#### Outputs
- Regenerated everything

</details>


## Release 4.16.0.1

> 2023-01-27

This is mostly a hotfix to deal with some bugs that have been reported. One in particular was considered a critical bug which meant this update goes out sooner rather than later. Below is a list of the issues addressed:

- Adjusted Scrambled Bugs settings so that all of Simonrim's perks and effects should act as the author intended.
- Dragons no longer magically obtain a smaller hitbox vs. projectiles, allowing archers and mages to actually kill them again.
- Innkeepers should properly give you a bounty letter when asked. If you decline the quest it won't be offered again immediately.
- The Windhelm bridge should have its proper textures.
- Unique weaponry should have all of their correct meshes/textures and a few stats have been tweaked to match Phoenix's intent.

A new save is not required. You will receive a warning about `Precision.esp` that can be ignored.

<details>

#### Changes

- **Architecture:** Added Windhelm Fence 3D
- **Gameplay Overhauls:** Removed Precision
- **Gameplay Overhauls:** Removed Precision Creatures
- **Improved Vanilla Quests:** Moved Headhunter - Bounties Redone to Miscellaneous
- **Skeleton & Animations:** Removed Nemesis Creature Behaviour Compatibility
- **Configuration:** Lowered SkillFormulaCaps to 100 (this won't change much of anything as Simonrim bonuses tend not to give raw skill boosts, I'm just cleaning up the file)
- **Configuration:** Adjusted Scrambled Bugs settings to match Simon's suggestions for his gameplay suite

#### Updates

- Updated NVIDIA Reflex Support to 1.1.2
- Updated Dwemer Gates Don't Reset to 1.3.7
- Updated Papyrus Tweaks to 4.0
- Updated Rally's Nord War Horns to 1.3
- Updated Pilgrim - A Religion Overhaul to 1.1.2
- Updated Honed Metal Revoiced to 1.8
- Updated The Choice Is Yours to 2.7

#### Outputs

- Regenerated Left Hand Meshes
- Regenerated Nemesis

</details>

## Release 4.16.0

> 2023-01-23

I'll be clear: **this is a new chapter for Slidikins' Strenuous Skyrim.** I've decided to rip off the proverbial band-aid and bring the list up to date to Skyrim SE 1.6.640. With that comes a handful of changes and a lot of new opportunities. Since a new game would've been required anyway, I also took the liberty of cramming in a ton of mods that also would've meant starting fresh. The end result is this monster of a changelog that I promise is totally the same SSS you've come to enjoy. Let's get into it!

#### Mod Substitutions

Not every SKSE plugin made the jump to 1.6.640. Most of them have been replaced with something comparable, such as *PlayerPayCrimeGold Tweak* filling in for *No Crime Teleport*. In two cases a substitute didn't exist (such as *SSE Gameplay Tweaks*). It's unfortunate but the features lost weren't vital to the list.

Outside of SKSE plugins there were a few more changes. wSkeever's *Simplicity of Snow* and *Shaders of Solstheim* took over for *Better Dynamic Snow/Ash*. *The Dragon Cult* replaced *Haugbui* which was a fine mod but not the best fit in comparison. You'll see a few others like these in the details below, such as the Lux series that's taken over the lighting.

#### Visual Changes

Since building the list off of TPF the philosophy has mostly been "focus on gameplay mods, let TPF handle the visuals." That has changed... slightly. I've been stepping out of that box a bit to include things such as MystiriousDawn's parallax landscape textures, *Seasons of Skyrim*, and borrowing from TPF 5.0's unreleased modlist. (Yes, that means ENB Complex Parallax is enabled in the regular profile.)

Even so, I don't like focusing on visuals and don't think this will lead to drastic changes in how the game looks. Expect to find more nuggets of visual changes here and there in future updates. *Lux* (and *Lux Via* and *Lux Orbis*) are the latest mods grabbed from TPF 5.0. Lighting will be noticeably different and stealth mechanics have changed slightly because of it. It'll probably be too easy still, but it's a work in progress.

#### Quest Expansions

JaySerpa's mods have always been on the cusp of making it into the list. I love pretty much all of their ideas but I have to ask myself, "Does this fit Vanilla+?" at every release. Well, the needle has moved to "Yes" for a lot of them, specifically the quest expansions. Alongside those you'll find other mods that enhance the existing quests of the game such as *Headhunter*, *Destination Weddings*, and *Extended Cut - Saints & Seducers*. That's right, *Saints & Seducers* is now part of the list!

#### Branching Further

With these and other changes, SSS has distanced itself from TPF that much more. It's still a TPF fork at its core but it's become impossible to convert TPF 4.16 to SSS 4.16 without a digital scalpel and a ton of time. As such, SSS' manual guide has been retired and installation is available only through Wabbajack. This will allow me to pile in some smaller mods (such as wSkeever's various fixes) without making installation more tedious, so expect to see these branches diverge even further as TPF 5.0 develops.

I haven't done justice to all of the changes in 4.16. Take a peek at the details below for a full list. There are some real gems in there.

<details>

Updated for [TPF 4.16.0](https://github.com/Codygits/TPF-Updates/releases/tag/4.16.0)
#### Changes
- **Creation Club Content:** Added Saints and Seducers
- **Essential Mods:** Removed .NET Script Framework
- **Essential Mods:** Added Crash Logger
- **Fixes:** Removed Dlizzio's Mesh Fixes - Assorted Mesh Fixes Patch
- **Fixes:** Removed Skyrim Particle Patch for ENB - Assorted Mesh Fixes - Solitude Mesh Fixes Patch
- **Fixes:** Added Animation Queue Fix
- **Fixes:** Added Beard Mask Fix
- **Fixes:** Added Enchantable Special Item Fix
- **Fixes:** Added Sound Fix for Large Sector Drives
- **Tweaks:** Removed SSE Gameplay Tweaks
- **Tweaks:** Removed No Crime Teleport
- **Tweaks:** Added PlayerPayCrimeGold Tweak
- **Tweaks:** Added Whiterun Watchtower Doesn't Start Broken
- **Tweaks:** Added Wade in Water
- **Tweaks:** Added Wade in Water Redone
- **Interface:** Added HD Local Map
- **Interface:** Added Show Player in Menus
- **Interface:** Adjusted positioning of Ammo Widget and Oxygen Meter
- **Graphics Baseline:** Removed SMIM - Assorted Mesh Fixes Patch
- **Graphics Baseline:** Added Far Object LOD Improvement Project
- **Seasons of Skyrim:** Added EC Vanilla Tweaks - Winter Unending
- **Weather:** Added Cathedral Weathers and Seasons - Unofficial Update
- **Weather:** Added Rain Extinguishes Fires
- **Lighting:** Removed Lanterns of Skyrim II
- **Lighting:** Removed Luminosity Lighting Overhaul
- **Lighting:** Added Lux
- **Lighting:** Added Lux Orbis
- **Landscape:** Removed Better Dynamic Snow
- **Landscape:** Removed Better Dynamic Ash
- **Landscape:** Removed Point the Way
- **Landscape:** Removed MystiriousDawn's HD Skyrim Overhaul - Landscape Textures 2K
- **Landscape:** Added Simplicity of Snow
- **Landscape:** Added Shaders of Solstheim - Ash and Moss
- **Landscape:** Added Lux Via
- **Landscape:** Added eFPS - Lux Via Patch
- **Landscape:** Added Tundra - HD Texture Replacer with Parallax
- **Landscape:** Added Dirt - HD Texture Replacer with Parallax
- **Landscape:** Added River Stone - HD Texture Replacer with Parallax
- **Landscape:** Added Snow - HD Texture Replacer with Parallax
- **Landscape:** Added Pine Forest - HD Texture Replacer with Parallax
- **Landscape:** Added Coast and Marsh - HD Texture Replacer with Parallax
- **Landscape:** Added Fall Forest - HD Texture Replacer with Parallax
- **Landscape:** Added Field Grass - HD Texture Replacer with Parallax
- **Landscape:** Added Volcanic Tundra - HD Texture Replacer with Parallax
- **Landscape:** Added Reach - HD Texture Replacer with Parallax
- **Architecture:** Added Skyrim Objects SMIMed - Warmaiden's Holes
- **Architecture:** Added Whiterun Cobblestone - HD Texture Replacer
- **Architecture:** Added Windhelm Bridge Stairs
- **Architecture:** Added Simplicity of Settlements - Dragon Bridge
- **Clutter:** Removed Yee Haaaa Horse Saddle Retexture
- **Clutter:** Removed Imperial Saddle Retexture
- **Clutter:** Removed Shadowmere Saddle Retexture
- **Food & Ingredients:** Added Garlic - A Garlic Mod
- **Apparel & Weapons:** Added Dynamic Armor Variants
- **Apparel & Weapons:** Added Dynamic Lowered Hoods
- **Creatures:** Removed Dawnguard Rewritten - Arvak
- **Creatures:** Added zzjay's Horse Overhaul
- **Creatures:** Added Slightly Better - Arvak
- **Creatures:** Added Arvak Burning Hooves Restored 
- **Gameplay Overhauls:** Removed Simple Werewolf Favourite Howls Menu
- **Gameplay Overhauls:** Removed More Expensive Transmute for Mysticism
- **Gameplay Overhauls:** Added Mysticism - Survival Spells Addon
- **Gameplay Overhauls:** Added Aetherius - Starting Spells Addon
- **Gameplay Overhauls:** Added Saints and Seducers - Mysticism Rebalance
- **Gameplay Overhauls:** Added Extended Cut Saints and Seducers - Mysticism Rebalance
- **Gameplay Overhauls:** Added Precision Creatures
- **Gameplay Overhauls:** Added Zim's Trainers Expansion
- **Loot & Crafting:** Removed Bounties Are Worthwhile - Leveled Bounty Rewards
- **Loot & Crafting:** Added Oblivion - An Atronach Forge Overhaul
- **Loot & Crafting:** Added Oblivion - Book Covers Skyrim Patch
- **Non Player Characters:** Added Forsworn and Thalmor Lines Expansion
- **Non Player Characters:** Added Carriages and Stables Dialogue Bundle
- **Non Player Characters:** Added Carriages and Stables Dialogue Bundle - CFTO Patch
- **Assorted Plugins:** Removed Sales Overflow Solved for real this time
- **Improved Vanilla Quests:** Removed The Paarthurnax Resolution
- **Improved Vanilla Quests:** Removed Reasonable Quest Rewards - Bounties Are Worthwhile Patch
- **Improved Vanilla Quests:** Added Paarthurnax - Quest Expansion
- **Improved Vanilla Quests:** Added Improved College Entry - Questline Tweaks
- **Improved Vanilla Quests:** Added Nilheim - Misc Quest Expansion
- **Improved Vanilla Quests:** Added Caught Red Handed - Quest Expansion
- **Improved Vanilla Quests:** Added House of Horrors - Quest Expansion
- **Improved Vanilla Quests:** Added The Only Cure - Quest Expansion
- **Improved Vanilla Quests:** Added The Whispering Door - Quest Expansion
- **Improved Vanilla Quests:** Added Skyrim Extended Cut - Saints and Seducers
- **Improved Vanilla Quests:** Added Missives are in Skyrim
- **Improved Vanilla Quests:** Added Headhunter - Bounties Redone
- **Improved Vanilla Quests:** Added Destination Weddings
- **Improved Vanilla Quests:** Added Destination Weddings - Compatibility Patches
- **Improved Vanilla Quests:** Added Fishing - Reduced Cut
- **Improved Vanilla Quests:** Added Streamlined Fishing
- **Combat & Encounters:** Removed Haugbui - A Draugr Overhaul
- **Combat & Encounters:** Removed Haugbui - Better-Shaped Weapons Patch
- **Combat & Encounters:** Removed Haugbui - SimonRim Patch
- **Combat & Encounters:** Removed Haugbui - CC Fishing Patch
- **Combat & Encounters:** Removed Haugbui - WACCF Patch
- **Combat & Encounters:** Added Blade and Blunt - Sneak Addon
- **Combat & Encounters:** Added Cannibal Draugr on Solstheim
- **Combat & Encounters:** Added The Dragon Cult - A Draugr Overhaul
- **Combat & Encounters:** Added Resistances and Weaknesses - NPC Armaments
- **Combat & Encounters:** Added Dragon War - Variants
- **Combat & Encounters:** Added Seeking Out Sneaks
- **Miscellaneou:** Removed Miscellaneous Tweaks Collection - No Starting Spells
- **Miscellaneous:** Removed Iron Dusk's Laboratory - Saddlebags
- **Miscellaneous:** Added Simplest Horses
- **Assorted Plugins:** Removed Better Stealing
- **Assorted Plugins:** Removed Uninterrupted Invisibility
- **Assorted Plugins:** Removed Uninterrupted Ethereal Form
- **Assorted Plugins:** Removed Crafting Skill Leveling Overhaul
- **Assorted Plugins:** Removed Fish Anywhere With Water
- **Assorted Plugins:** Added Mum's the Word
- **Assorted Plugins:** Added Enhanced Invisibility
- **Assorted Plugins:** Added Missile's Immersive Equipment Display Presets
- **Assorted Plugins:** Added Missile's Immersive Equipment Display Presets - Better Head Hunter Displays While Mounted
- **Sound FX:** Added Acoustic Space Improvement Fixes
- **Skeletons & Animations:** Removed Read the Room
- **Skeletons & Animations:** Added Nemesis Creature Behaviour Compatibility
- **Skeleton & Animations:** Added Faster Horse Dismount
- **Skeleton & Animations:** Added Take a Seat
- **Controls & Camera:** Removed Alternate Conversation Camera Plus
- **Controls & Camera:** Added Improved Alternate Conversation Camera
- **Utilities:** Added ENB Helper Plus
- **Conflict Resolution:** Added weights to currency added by C.O.I.N. to match Septim weights
- **Conflict Resolution:** Added FallowstoneCaveWorldEnd `000204C7` overwrite for Shadows of Sunlight.
- **Conflict Resolution:** Removed a ton of old records that have been changed by either Mysticism, AOS, or both.
- **Conflict Resolution:** Updated FVS_VelehkHeart values to match earlier Apothecary update
- **Conflict Resolution:** Adjusted values in Zim's Trainers Expansion to prevent exploits
- **Conflict Resolution:** Adjusted Sneak gamesettings in a number of ways
- **Conflict Resolution (Creation Club):** Removed MAG_flameCloak `0003AE9F` as it's covered in Mysticism - Survival Spells Addon
- **Conflict Resolution (Creation Club):** Removed DLC2FoodHorkerAshYamStew `0403CD5B` to let the new Survival Mode Improved patch do its job
- **Conflict Resolution (Creation Club):** Patched two SECSS ingredients with Apothecary 
- **Conflict Resolution (Creation Club):** Removed edits to the Steed Stone and Extra Pockets
- **FaceGen:** Removed extraneous data from TPF's FaceGen data (it's much smaller now!)

#### Updates
- Updated xLODGEN to 97
- Updated DynDOLOD to 3.00 Alpha-111
- Updated Synthesis to 0.25.3
- Updated SSE NIF Optimizer to 3.2.0
- Updated numerous SKSE Plugins to the respective AE version
  - Disabled Keyboard Shortcuts Fix until it's compatible
  - Disabled NVIDIA Reflex Support until it's compatible
  - Disabled Don't Stay in the Water until it's compatible
  - Disabled Wash That Blood Off 2 until it's compatible
- Updated Address Library for SKSE Plugins to 8.0
- Updated SSE Engine Fixes to 6.1.1
- Updated Weapons Armor Clothing and Clutter Fixes to 2.9.2
- Updated Particle Patch for ENB to 1.2.2
- Updated Skyrim Landscape and Water Fixes to 7.4
- Updated Assorted Mesh Fixes to 0.77.1
- Updated Bug Fixes SSE to 8
- Updated Actor Limit Fix to 7
- Updated Equip Enchantment Fix to 1.3.6
- Updated Mfg Fix to 1.6.1
- Updated ENB Light Inventory Fix to 1.1.1
- Updated Shadow Boost to 1.3
- Updated Shadow Diffusion (now Soft Shadows) to 1.1
- Updated Papyrus Tweaks to 3.3
- Updated Reading is Good to 1.1.2
- Updated Fix Note Icon for SkyUI to 1.2.6
- Updated moreHUD to 5.2.2.0
- Updated Nordic UI - Miscellaneous Patches to 1.8.1
- Updated Contextual Crosshair to 1.3
- Updated A Clear Map of Skyrim and Other Worlds to 4.0
- Updated Forget Spell to 1.2.5
- Updated DynDOLOD Resources to 3.00 Alpha-30
- Updated Simple Activate SKSE to 1.4.1
- Updated Far Object LOD Improvement Project to 1.1
- Updated Frozen Electrocuted Combustion to 5.1
- Updated Realistic Water Two to 5.6
- Updated FYX - Water Splash to 1.0.1.1
- Updated Skyrim Flora Overhaul - Plant Textures to 2.73b
- Updated Iconic Statues 4K to 1.2.1
- Updated Mysticism - A Magic Overhaul to 2.2.1
- Updated Adamant - A Perk Overhaul to 5.7.4
- Updated Adamant - Hand to Hand Addon to 1.3.6
- Updated Aetherius - A Race Overhaul to 2.9.1
- Updated Scion - A Vampire Overhaul to 2.1.2
- Updated Manbeast - A Werewofl Overhaul to 2.0
- Updated Forceful Tongue - Shouts Overhaul to 3.0.8
- Updated Pilgrim - A Religion Overhaul to 1.1.1
- Updated Survival Mode Improved to 1.0.7
- Updated Precision to 2.0.4
- Updated Armor and Clothing Extension to 1.5.1
- Updated Ancient Nord Stalhrim to 1.2.3
- Updated Trade and Barter - Adamant Patch with a hotfix
- Updated Armor and Clothing Extension - Spell Perk Item Distributor Patch to 1.4
- Updated Simple Degradation - NPC Tempering to 1.4.1
- Updated C.O.I.N. - Coins of Interesting Natures to 2.1.0.2
- Updated Bandit Lines Expansion to 1.06
- Updated NPCs Wear Amulets of Mara to 2.02
- Updated Civil War Lines Expansion to 1.05
- Updated The Choice is Yours to 2.6
- Updated Encounter Zones Unlocked to 1.5.4
- Updated Resistances and Weaknesses to 1.0
- Updated Enchantments and Potions Work for NPCs to 1.0.2
- Updated NPCs Learn Skills and Spells to 1.2
- Updated Blade and Blunt - A Combat Overhaul to 2.1
- Updated Archery Rebalance (formerly Quintessential Quivers) to 1.7
- Updated Horse Stamina HUD to 1.0.4
- Updated Unequip Quiver to 2.1.1
- Updated Audio Overhaul for Skyrim to 4.0.1
- Updated Regional Sounds Expansion to 2.0
- Updated Reverb Interior Sounds Expansion to 1.4
- Updated Simple Dual Sheath to 1.5.4
- Updated Sleeping Expanded to 1.22
- Updated Dynamic Animation Replacer to 1.1.3
- Updated Auto Input Switch to 1.2
- Updated Classic Sprinting Redone to 2.3
- Updated Better Jumping to 1.8.6
- Updated Better Third Person Selection to 0.5.8
- Updated JContainers to 4.2.3
- Updated powerofthree's Papyrus Extender to 5.4.1
- Updated FileAccess Interface for Skyrim SE to 1.4.1b
- Updated ConsoleUtils to 1.4
- Updated ENB Helper to 2.2
- Updated Spell Perk Item Distributor to 6.3
- Updated Console Commands Extender to 1.11
- Updated Keyword Item Distributor to 2.2
- Updated Base Object Swapper to 2.5.1
- Updated Sound Record Distributor to 1.3
- Updated ENBSeries to v0.384
- Updated Blade and Blunt - Vanilla Difficulty Modifiers to 2.0

#### Outputs
- Regenerated Left Hand Meshes
- Regenerated Nemesis
- Regenerated xLODGEN
- Regenerated TexGen
- Regenerated DynDOLOD (and Performance)
</details>



---
#### Previous changes dating back Release 4.3 can be found [here](https://github.com/Amigoliath/Slidikins-Strenuous-Skyrim/blob/main/Changelog.md)