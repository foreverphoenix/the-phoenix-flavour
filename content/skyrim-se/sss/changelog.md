---
title: "Changelog"
weight: 8
type: docs
description: >
  *I shall explain to you the mysteries of the outer realms.*
---

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
- Updated NVIDIA Reflex Support to 1.1.2 (73)
- Updated Dwemer Gates Don't Reset to 1.3.7 (78)
- Updated Papyrus Tweaks to 4.0 (100)
- Updated Rally's Nord War Horns to 1.3 (440)
- Updated Pilgrim - A Religion Overhaul to 1.1.2 (671)
- Updated Honed Metal Revoiced to 1.8 (720)
- Updated The Choice Is Yours to 2.7 (760)

#### Outputs
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
- Regenerated Nemesis
- Regenerated xLODGEN
- Regenerated TexGen
- Regenerated DynDOLOD (and Performance)
</details>



---
#### Previous changes dating back Release 4.3 can be found [here](https://github.com/Amigoliath/Slidikins-Strenuous-Skyrim/blob/main/Changelog.md)