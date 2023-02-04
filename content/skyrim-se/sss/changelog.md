---
title: "Changelog"
weight: 8
type: docs
description: >
  *I shall explain to you the mysteries of the outer realms.*
---

## Release 4.16.1 RC 1

> 2023-02-04

This update should really be called *Slidikins' Strenuous Skyrim Release 5.0 RC 4* as it's essentially a complete rebuild of the list based off of *The Phoenix Flavour 5.0 RC 4* (which is currently unavailable). The changes in 4.15.5 was the first step towards this goal. The jump to SSE 1.6.640 in 4.16 put me within spitting distance. So, while I know that it's only been a week since that jump, I've decided to go the rest of the way.

The core of the list hasn't changed. It's still a Simonrim-centered TPF modlist with *Survival Mode* and my other choices, but TPF 5.0 has decided to venture off into the previously labeled "TPF-X" realm of added content. This update follows TPF down that path... some of the way. You'll find your Vanilla+ experience peppered with **new enemies, new equipment, expanded quests, more crafting options, and more**. What you won't find are the new worldscapes (areas), followers, or any content that requires the [Anniversary Upgrade](https://store.steampowered.com/app/1746860/The_Elder_Scrolls_V_Skyrim_Anniversary_Upgrade). If you have that, keep an eye out for TPF's release as it will integrate most of it very well.

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