---
title: "Changelog"
weight: 7
type: docs
description: >
  Update notes for all non-Beta versions.
---

## Release 2.6.1

> 16/08/2022

All I wanted to do was fix WJ installations failing due to the xLODGen archives, but then DoubleYou went and published more LOD improvements, so I had to regenerate terrain and object LODs, and things kind of escalated from there. Anyway, this is a semi-minor update that is of course safe save and makes (distant) trees look better, especially on Far Harbor.

**KNOWN ISSUE:** Currently there is an empty category in the Crafting (chem) Bench. If you click it YOU CAN'T BACK OUT so, uhh, don't click it. I have no idea what is causing it but I'll investigate further.

#### Mod Changes

- Added BSArchPro (irrelevant for users)
- Added Fall UI No 3D in Barter Menu
- Added Better Landscape Grass
- Added NukaWorld HiRez FakeRocks
- Added Drinkable Water Retexture
- Added Wasteland Workshop Snappable Posters
- Added Five Wall Corners
- Added Optimised Vanilla Tree LODs
- Added Far Harbor 3D Tree LODs
- Re-added Fixed Gobo Effects
- Updated Workshop Framework to 2.2.3
- Updated Fixed Alpha Maps to 6.1
- Updated Targeted Textures to 1.2
- Updated Perk Up to 1.2
- Removed Retextured Water - By Ben Ephla
- Removed xLODGen archives that was causing installs to fail (sorry)
- Repacked the Texture Pack - Clutter BA2s
- Slightly modified the Upgradable Vault Suit crafting station category for consistency
- Regenerated terrain and object LOD

#### Website Changes

- **Documentation:** Minor updates for newly added mods
- **Known Issues:** Added empty Crafting Bench category issue

## Release 2.6

> 12/08/2022

**This update requires a new save.**

WTP now features [Perk Up - Lightweight Perk Overhaul](https://www.nexusmods.com/fallout4/mods/62843), one of a collection of mods by SpringHeelJon for his new Wabbajack list, [FUSION](https://www.nexusmods.com/fallout4/mods/62880), which you should definitely check out!

I also added [Kezyma's Root Builder](https://www.nexusmods.com/skyrimspecialedition/mods/31720) which means moving the Game Folder Files is no longer required. Instead, all files that need to be inside the root folder will be moved there by the plugin when you launch the game, and removed again when you close it. Existing WTP users should clear out existing GFF files from their root folder.

Also I finally got around to generating custom terrain and object LOD for this update.

#### Mod Changes

- Added FO4LODGen
- Added Kezyma's Root Builder (MO2 plugin)
- Added Kezyma's Profile Sync (MO2 plugin)
- Added Targeted Textures - Vanilla Textures Upscaled Fixed and Sized
- Added Perk Up - Lightweight Perk Overhaul
- Added No Empty Med Cabinets (custom plugin)
- Added Perk Up - Restore Power Armor Frames Patch (custom plugin)
- Added FO4LODGen Resources
- Added HD LOD Textures
- Added Modern House LOD
- Added Far Object LOD Improvement Project
- Added custom terrain and object LOD
- Updated Fixed Alpha Maps to 6.0
- Updated Lightweight Lighting to 2.3
- Updated Upgradeable Vault Suit to 1.1
- Updated Previsibines Repair Pack to 0.59.10
- Removed deorder's plugins
- Removed Starlight Drive In LOD Fix
- Removed Nuka-World - Transit Center LOD Fix
- Removed Fixed Gobo Textures (included with Targeted Textures)
- Removed Far Harbor Pine Branches 4K (included with Targeted Textures)
- Removed Fix for Forsythia (included with Targeted Textures)
- Removed Easy Lockpicking and Hacking (replaced by Perk Up)
- Removed Fortune Finder 4 Fix (included in Perk Up)
- Removed Neura LOD (replaced by custom LODs)

#### Modifications

- Forwarded various UFO4P edits
- Added the [Raw] sorting tag to the Nukalurk Egg added by the UFO4P
- Added new {Neck} tag with appropriate icon
- Fixed missing tags on Yao-guai Finger Necklace and Pack Feather Necklace
- Renamed some custom plugins
- ESL-flagged Some Assembly Required - WTP Patch

#### Website Changes

- **Installation:** Removed Game Folder Files instructions (no longer necessary with Root Builder)
- **Installation:** Removed Easy Lockpicking and Hacking section (mod removed in favour of Perk Up)
- **Documentation:** Removed Game Folder Files section (no longer necessary with Root Builder)
- **Known Issues:** Updated instructions on how to disable ENB in case of performance issues

## Release 2.5

> 30/07/2022

This update is coming with some site restructuring: The entire WTP documentation was moved to the new Fallout 4 Lists section and as a result, all links are broken. I fixed those I could find, let me know if you find any that are still leading into the void. I also took the opportunity to restructure the pages somewhat, particularly the Documentation.

I also removed the mod Facials for Everyone because of persistent performance issues. Fallout 4 has an issue where long levelled lists for NPC templates considerably degrade performance, so Facials offered a "lite" version with a shorter LList for that reason and WTP was using that. But I still got plenty of reports for stutters that were fixed by disabling facials and decided to boot the mod.

Also puddles were re-enable and should no longer flicker. Yay!

#### Mod Changes

- Added Simple Puddle Reflection Flicker Fix
- Added Gloomy Glass - All Transparent Materials Revised
- Added Blasted Billboards - A Weathered Billboard Overhaul
- Added Peeling Posters - Weathered Paper Based Signs
- Added Frame Job - A Power Armor Frame Retexture
- Added The Eyes of Beauty - SHJ Edit
- Added Dog Furniture Pack
- Added Previsibines Repair Pack - Hotfix 0.59.7
- Updated the Fallout 4 Script Extender to 0.6.23
- Updated Spectrum ENB to 1.2
- Updated the Unofficial Fallout 4 Patch to 2.1.4
- Updated High FPS Physics Fix to 0.8.6
- Updated Workshop Framework to 2.2.2
- Updated Wetness Shader Fix to 3.6.1
- Updated Lightweight Lighting to 2.2
- Updated Ultimate Window Overhaul Redone to 4.0
- Updated Curated Companions to Final
- Updated Classic Holstered Weapons System to 1.06b
- Updated Whisper's Extra Pieces and Snaps to 2
- Updated Useful Posts to 1.1
- Updated LOST Audio Tweaks to 3
- Removed Overboss Colter Fix (now obsolete)
- Removed Clarity - A Visual Overhaul - Material Edits
- Removed ADs 2X Rez HDTP
- Removed Power Armor Frame 4K UHD
- Removed The Eyes of Beauty
- Removed Facials for Everyone - Less Than Fresh Faces
- Removed WTP - Curated Companions Patch (no longer necessary)
- Repacked Texture Pack - Power Armor
- Fixed load order for SyringerAmmoSimplerIngredientsAlternate.esp
- Re-enabled puddles which should now be flicker-free at last

#### Website Changes

- **Installation:** Moved Requirements here and added MO2 Prerequisites sub section
- **Installation:** Instructions for the CC Modular Military Backpack were rewritten and moved here
- **Documentation:** Merged several separate sites together into one longer documentation
- **Known Issues:** Added "brown faces" problem and solution

## Release 2.4

> 17/06/2022

It was recently brought to my attention that some DLC weapons have completely broken names which turned out to have been due to a very silly oversight on my part. This update fixes that, but unfortunately it will not work retroactively. If you already went to Far Harbor and / or Nuka World, any weapons that already generated will have the incorrect names. Sorry about that.

In other news, I added a few recent releases, mostly adding new snap points to meshes to make settlement building a smoother experience. Syringer ammo is now easier to craft (requiring base ingredients rather than Antifreeze Bottles etc) and will be sorted in their own roll-up (sub) menu in the Aid tab. You can quit accidentally poisoning yourself now.

If you don't want to start a new game for this, you need to manually restart the quest for Diamond City Radio Extended ingame. Open the console and run the following two commands:

```
stopquest radiodiamondcity 
startquest radiodiamondcity
```

#### Mod Changes

- Added Atom Cats Drag Race Start Fix
- Added CC's UHD APC 4K (packed into a BA2)
- Added Companion Thoughts Overhaul
- Added Syringer Ammo Simpler Ingredients
- Added Proctor Teagan Sells BOS Clothing
- Added Garden Plot Snap
- Added Useful Posts
- Added Warehouse Corner Wall Snap
- Added Warehouse to Wall Snap
- Added Snappy Half Walls
- Updated BethINI to 3.6.1
- Updated Cathedral Assets Optimizer to 5.3.13
- Updated Buffout 4 to 1.26.2
- Updated Wetness Shader Fix to 3.6
- Updated Workshop Framework to 2.2.1a
- Updated MCM Settings Manager to 1.1
- Updated Phoenix - Sorting Overhaul (see below)
- Updated FallUI - Interface to 2.1.1
- Updated FallUI - HUD to 1.6b
- Updated FallUI - Confirm Boxes to 2.2.1
- Updated FallUI - Workbench to 1.4
- Updated Diamond City Radio Extended to 3.0.0
- Updated LOST Audio Tweaks - DCRE RAO Patch to 3.0.0
- Updated WTP MCM Presets (both regular and 21:9 versions)
- Regenerated both sets of INI files with the new version of BethINI
- Removed tbbmalloc.dll from Game Folder Files

> The tbbmalloc.dll is no longer required for Buffout. You can delete it from your root folder.

#### Sorting Overhaul

- Added some Nuka World melee weapon paint job options missing in the main INNR record
- Fixed broken names on Far Harbor / Nuka World weapons
- Fixed some insanely difficult to see errors in the scrap tags for three different Lit Cigar records

#### Website Changes

- [MCM Settings](/fo4/wtp/documentation/mcm-settings/): Updated for the new changes (specifically in the FallUI mod MCMs)

## Release 2.3.3

> 30/04/2022

Small update. Yes, it's save-safe.

#### Mod Changes

- Added DiamondTheWall Retexture (packed into a BA2)
- Added CC's UHD UFO 4K (packed into a BA2)
- Added Cathedral Asset Optimizer (irrelevant for users)
- Updated Cola Cars Overboss Fix to 1.2
- Updated Laser Weapons 1st Person Reposition to 1.5.2
- Updated Wetness Shader Fix to 3.5
- Updated Workshop Framework to 2.2.0
- Updated Fallout 4 Ultimate Window Overhaul to 3.2
- Updated Configurable Hotkeys to 6
- Updated Previsibines Repair Pack to 0.59.5

## Release 2.3.2

> 03/04/2022

Another minor update, mostly to address performance concerns and to fix ambient occlusion being enabled in the INIs.

#### Mod Changes

- Added Overboss Colter Fix (used to be part or PRP)
- Updated Workshop Framework to 2.0.22
- Updated Previsibines Repair Pack to 0.57.4.2
- Disabled ambient occlusion in the default INIs (it was accidentally left enabled in the previous update, sorry about that)
- Added a set of performance INIs that should yield a better framerate on lower end PCs

#### Website Changes

- **Introduction:** Moved the requirements here from the Installation page
- **Installation:** Added the Performance INI section
- **INI Files:** Moved notes on INI settings to their own page
- **Known Issues:** Added "Performance Issues" section

## Release 2.3.1

> 28/03/2022

This is a quick maintenance update for WTP because I'm a dummy and deleted the enbseries zip from the CDN. I did take the opportunity to add a new, high-res map retexture which required me to adjust the MCM settings for FallUI Map a bit. While I was at it, I changed the Wait hotkey to CTRL + T so it doesn't accidentally trigger while renaming a weapon. Finally, I also regenerated INIs with the new version of BethINI, hope I didn't forget about any custom tweaks. I may add performance INIs in the future if people find this set to be too demanding.

#### Mod Changes

- Added Glass Roofs Stop Rain and Snow - Vanilla Green House Roof
- Added Collection Improved Maps
- Added NPC Accuracy Revised
- Updated WTP - MCM Settings Preset
- Updated Workshop Framework to 2.0.21
- Updated Natural Landscapes to 0.5
- Updated Tune The Radios to 2.1.3
- Updated Previsibines Repair Pack to 1.57.4.1
- Updated BethINI to 3.6
- Fixed enbseries link which took down 2.3 (very sorry about that)
- Regenerated INI files

#### Website Changes

- **GFF & INI Settings:** Now documenting my INI tweaks on this page.
- **MCM Settings:** Updated Baka Wait Anywhere settings and added FallUI Map settings.

## Release 2.3

> 27/02/2022

**New save required.** Please also overwrite the Game Folder Files!

This update adds a few cool new mods as well as some relevant updates.

- The assorted radio mods were replaced with the combined [Diamond City Radio Extended](https://www.nexusmods.com/fallout4/mods/56898).
- Visuals are now largely affected by [Spectrum ENB](https://www.nexusmods.com/fallout4/mods/58028) and [Lightweight Lighting](https://www.nexusmods.com/fallout4/mods/57680).
- You can now [upgrade your vault suit](https://www.nexusmods.com/fallout4/mods/57891) as you progress through the main quest!
- [Facials for Everyone](https://www.nexusmods.com/fallout4/mods/37180) expands the face preset lists without affecting performance.

Please note that I have not tested this update extensively. That being said, I do not anticipate any major issues.

#### Mod Changes

- Added Spectrum ENB
- Added Lightweight Lighting - A Weather and Interior Lighting Overhaul
- Added Imposing Gunner Skulls
- Added Facials For Everyone - Less Than Fresh Faces
- Added Curated Companions
- Added WTP - Curated Companions Patch
- Added Upgradable Vault Suit
- Added WTP - Upgradable Vault Suit Patch
- Added Diamond City Radio Extended
- Added Radio AT - DCE RAO Patch
- Updated ENB Series to 0.468
- Updated Workshop Framework to 2.0.20
- Updated What's Your Name to 1.13.1
- Updated Previsibines Repair Pack to 0.57.2/0.57.3
- Removed FallOpt ENB
- Removed Flicker Fixer (incorporated in PRP)
- Removed Improved Map with Visible Roads
- Removed SeriouslySarcastic's Immersive Companions
- Removed Better Settlers
- Removed BS Defence
- Removed More Where That Came From - Diamond City Radio Edition
- Removed LOST Audio Tweaks - MWTCF DC Patch
- Removed Elvani's Track Pack - Diamond City Radio
- Removed Previs Repair Pack - Clarity Patch
- Heavily edited Clarity.esp, it now only removes puddles and iron sight DOF
- Disabled InputSwitch in Buffout (could cause some issues)
- Easy Lockpicking and Hacking is now disabled by default
- Place Everywhere mode is now on by default

#### Website Changes

With this update, I gave the website a much-needed once over. Most improvements are relatively minor and were not documented.

- **Introduction:** Slightly restructured the page and updated the feature list.
- **Installation:** Consolidated all sub-pages to a single long one. Attempted to shorten it a little and fixed a few broken links.
- **Installation:** Added instructions on how to enable Easy Lockpicking and Hacking.
- **Mod Config:** Removed step about applying FallUI HUD preset. Turns out the MCM preset already does it!
- **WTP Visuals:** Slightly updated the documentation. The screenshots are a tad outdated and will be replaced asap.
- **WTP Gameplay:** Slightly updated the documentation.

## Release 2.2

> 13/01/2022

With this update I am removing This Is Trash, WTP's scrapping mod which should some performance issues and flickering. Neither This Is Trash nor Previs Repair Pack are causing this issue, but using both at the same time would require me to regenerate previs/precombines for places where they overlap if I wanted to avoid issues. To tell you the truth, the whole process is time-consuming and annoying, and I do not care enough about Fallout 4 modding to dive any deeper into this. Hence, the removal of This Is Trash.

In other news, I re-added Ultrawide (21:9) support. Folks with 2560x1080 or 3440x1440 monitor resolutions will now be able to play with a properly adjusted UI.

**This update is NOT save-safe.**

Remember to copy over Game Folder Files again to update the ENB preset.

#### Mod Changes

- Added ENB Helper for Fallout 4
- Added MCM Booster
- Added TruBy9 UltraWide Fallout 4
- Added Welcome to Paradise - MCM Settings (21-9)
- Added Minimalistic Main Menu
- Updated Mod Organizer to 2.4.4
- Updated FallOpt ENB to 2.3
- Updated Natural Rocks to 0.3
- Removed Another Sanctuary Bridge (can't be bothered to redo precombines)
- Removed This Is Trash (can't be bothered to redo precombines)
- Fixed Place Everywhere INI (keybinds were F2, F3 instead of F1, F2 - thanks, Dargor!)
- Minor edits to the Conflict Resolution Patch

#### Website Changes

- [Finalisation](/fo4/wtp/installation/finalisation/): Added section with instructions for ultrawide compatibility.
- [Mod Config](/fo4/wtp/mod-config/): Updated the MCM preset instructions to account for the new 21:9 preset.

![Widescreen Main Menu](/Pictures/wtp/installation/widescreen-main-menu.jpg)

## Release 2.1

> 25/12/2021

This is a small maintenance update, largely to bring you the recent FallOpt ENB improvements.

This update is **save-safe**. Please copy over game folder files once again as the ENB files updated.

#### Mod Changes

- Updated Workshop Framework to 2.0.18a
- Updated MCM Settings Manager to 1.0.3
- Updated LOST - Audio Tweaks to 2.1
- Updated Previsibines Repair Pack to 0.53.12012021
- Updated FallOpt ENB to 2.2
- Removed Hush Dogmeat (integrated in LOST - Audio Tweaks)
- Enabled HBAO in fallout4prefs.ini (ambient occlusion)
- Changed MO2 separator colours again
- New Wabbajack cover image

## Release 2.0

> 01/12/2021

**A new save is required.**

Welcome to Paradise 2.0 goes back to the roots. The list was refocused to vanilla improvements with a great deal of sorely needed back-end changes, including a full rebuild with detailed documentation of all edits in Mod Organizer 2. Lingering issues and annoyances from previous versions (that I know of) were eliminated with the result being an overall more consistent, polished experience.

- New lighting and ENB combination for more consistent visuals as well as brighter nights and interiors.
- Better shadow INI settings to reduce pop-in and blurry shadows (thanks SpringHeelJon!).
- Replaced Boston FPS Fix with Previs Pack to eliminate some crashes and improve performance in even more areas.
- Replaced Workshop Re-arranged with smaller, more managable workshop additions.
- New retextures, most of which were added to the WTP texture packs for better performance.
- MCM settings can now be applied automatically via a universal WTP preset thanks to MCM Settings Manager.
- Finally some documentation in the form of the new [WTP Visuals](/fo4/wtp/documentation/wtp-visuals/) and [WTP Gameplay](/fo4/wtp/documentation/wtp-gameplay/) pages.

**ENB and lighting changes:**

In WTP 2.0, I removed [True Storms](https://www.nexusmods.com/fallout4/mods/4472), [True Nights](https://www.nexusmods.com/fallout4/mods/9253), and [Subtle ENB](https://www.nexusmods.com/fallout4/mods/5885). The decision was not easy as I have never really played Fallout 4 *without* True Storms, and I really love the murky nights with this combination of mods. Unfortunately, True Storms makes the game's lackluster occlusion effect (intended to prevent rain and fogs in interiors) even more noticable. I also had a ton of people complain about dark nights.

With this update, WTP is switching to [Clarity](https://www.nexusmods.com/fallout4/mods/31991) for some fantastic all around improvements to visuals as well as the lightweight [FallOpt ENB](https://www.nexusmods.com/fallout4/mods/55662) preset. This combination also mostly replaced [Interiors Enhanced](https://www.nexusmods.com/fallout4/mods/8768) which means that interiors are a little brighter now.

**Removal of CBBE and EVB:**

I ended up removing the body replacers in this update. There is simply nothing I really need CBBE for and EVB male bodies do not have dismemberment support.

**Removal of Workshop Re-arranged:**

Workshop Re-arranged is a pretty great workshop overhaul. Unfortunately, it's also extremely difficult to work with on account of its rebalancing edits which change many of the building requirements as well as junk scrap yields. I finally decided to ditch the mod and return to smaller, individual workshop additions.

**BOS Power Armor Paint Jobs:**

I realised that without the stat changes, there is no need to have separate Knight/Paladin/Sentinel paint jobs for the power armor as they are visually identical. The exception is the Left Arm piece which displays the rank insignia. I rectified this by adding a single "Brotherhood of Steel" paint job that can be applied to any piece of power armor, then limiting the rank-specific paint job to Left Arm pieces. Problem solved!

#### Mod Changes

**New Additions**

- Added FallOpt ENB
- Added MCM Settings Manager
- Added Fallout Priority - F4SE Plugin (may be placebo)
- Added NPC Drinking Fix
- Added Fixed Textures for Mirelurk Egg Omelette
- Added Institute Floor Fix
- Added Automatron Load Screen Fix
- Added No Negative Affinity
- Added No Negative Affinity DLC Patch
- Added No Crafting Experience
- Added No Holotape Tease - Texture Replacement
- Added Base Scrap Is Not Junk Jet Ammo (custom)
- Added NPC Protection Tweaks (custom)
- Added Atmospheric Animated Menu Replacer (Night Version)
- Added Clarity - A Visual Overhaul
- Added NMC's Texture Bundle
- Added Redder Red Rocket
- Added Subway Transit Sign HD Texture
- Added CC's Vertibirds
- Added The Nuka Project
- Added Scrap Metal and Makeshift Welds - A Pipe Gun Retexture
- Added Duffle Bag Retexture
- Added U.S. Covert Operations Manual Revised - Magazine Retexture
- Added Pipboy UHD - Holotape
- Added Vault Suits UHD
- Added CC's UHD Bloatflies - Reimagined
- Added Immersive Mouth and Teeth
- Added Valkyr Female Body Textures
- Added Baka Wait Anywhere
- Added Easy Lockpicking and Hacking
- Added Consume Without Pickup
- Added Moonracer's Armor Overhaul
- Added Some Assembly Required - Atom Cats CPAO Patch
- Added Locked Vault Tec Paint Job
- Added Locked Abraxo and Sugar Bombs Power Armor Paints
- Added No PA Battery Pathing
- Added Power Grid Tools
- Added Improved Workshop Lights
- Added Better Workshop Street Oil Lamps
- Added DLC Light Radius Redux
- Added Wasteland Workshop Street Lamp and Ceiling Light Fix
- Added Better Generators (x2)
- Added Tune the Radios
- Added Shackin' Up - A Prefab Shack Mod
- Added Whisper's Extra Pieces and Snaps
- Added Snappable Junk Fences
- Added No More Gaps Under Junk Fences
- Added Graf's Security Fences
- Added Craftable Turret Stands
- Added Wall Oil Lamps
- Added Better Workshop Street Oil Lamps - Wall Oil Lamps Patch
- Added Pip-Boy Retextured
- Added LOST Audio Tweaks - MWTCF DC Patch
- Added Previs Repair Pack

**Updated Mods**

- Updated ENBSeries binaries (no version number change)
- Updated xSE Plugin Preloader F4 to 0.2.5.1
- Updated Buffout to 1.24.5
- Updated Buffout TBB Redistributables to 2021.3
- Updated High FPS Physics Fix to 0.8.4-5
- Updated Laser Weapons 1st Person Reposition to 1.5
- Updated WET - Water Enhancement Textures to 2.0.4
- Updated Retro Radio Replacer to 0.2
- Updated Visible Idle Markers to 3
- Updated BS Defence to 2.3
- Updated LOST Audio Tweaks to 2
- Updated FO4Edit to 4.0.4

**Removed Mods**

- Removed Subtle ENB
- Removed Jamaica Plain Navmesh Fix (fix included in UFO4P)
- Removed Corpse Collision
- Removed No More Glowing Water Coolers (replaced by Clarity)
- Removed Fixed Flickering Puddles (Clarity removes the puddles)
- Removed No Lockpick Activate (F4SE)
- Removed Depth of Field (DOF) Removal
- Removed Valdacil's Item Sorting - Perks
- Removed Main Menu Music Replacer - Wandering The Foothills
- Removed True Storms - Wasteland Edition
- Removed True Nights
- Removed Interiors Enhanced
- Removed Vehicle Overhaul
- Removed Really Red Rocket
- Removed Authentic Hand-Made Weapons (removed from the Nexus)
- Removed U.S. Covert Operations Manual - Magazine Retexture
- Removed Proto Vault Suit
- Removed Better Recon Scope
- Removed Spiffy's Workshop - Forged in Nuclear Fire - HQ Liberty Prime Retexture
- Removed CC's UHD Bloatflies
- Removed Distinct Teeth for FO4
- Removed Caliente's Beautiful Bodies Enhancer
- Removed Kellogg's Gloves for CBBE Clipping Fix
- Removed Skeletal Adjustments for CBBE - Knee Fix
- Removed CBBE Ida Body Texture
- Removed Enhanced Vanilla Bodies
- Removed Auto Hack
- Removed Auto Lockpicking
- Removed Better Explosives Redux (too overpowered)
- Removed Unique X-01
- Removed No Quest Autostart - BOS Fire Support
- Removed Main Quest Choices Extended
- Removed Nuka World Collectable Quest Markers
- Removed Corrunda's Red Rocket - Light and Curb Fix
- Removed Fixed and Cleaned Homeplate
- Removed Vault 88 Template - Optimised
- Removed Obedient Concord Group (toggleable with Visible Idle Markers)
- Removed Workshop Re-arranged
- Removed Grab The Damn Mag (not adding custom weapons)
- Removed RAO - True Storms Patch
- Removed Game Configuration Menu (replaced with individual tweaks)
- Removed Boston FPS Fix
- Removed Boston FPS Fix - Hotfix for UFO4P 2.1.1a
- Removed River Fix

**Other Edits**

- Rebuilt all custom texture pack BA2s
- Some retextures were increased from 2K to 4K
- Packed up ADs 2X Rez HDTP in a BA2
- Switched to the merged legendary patch version of Some Assembly Required
- Heavily edited the CRP (many patches are now separate)
- Disabled ambient occlusion in the Fallout4Prefs.ini (in favour of ENB AO)
- Increased fBlendSplitDirShadow from 48 to 96 in Fallout4Prefs.ini
- Increased iDirShadowSplits from 2 to 3 in Fallout4Prefs.ini
- Now using the HighFPSPhysicsFix_custom.ini feature
- My BAT files for testing are no longer included
- Changed interface color to a muted green matching the Pip-Boy
- New separator colours in MO2
- Added MO2 Loot Preventifier (plugin by LostDragonist)
- Sort button above the load order in MO2 was removed
- Installed NifSkope as an additional tool

#### Website Changes

- [Finalisation](/fo4/wtp/installation/finalisation/): Removed the LUTs section
- [Finalisation](/fo4/wtp/installation/finalisation/): Removed VSYNC section (it is now always enabled as it should be)
- [Finalisation](/fo4/wtp/installation/finalisation/): Updated the FPS Cap section including the screenshot
- [Mod Config](/fo4/wtp/mod-config/): Completely overhauled this page to account for automatic MCM settings loading and the new mods
- Removed the Resources section
- Added the Documentation section
- [Game Folder Files](/fo4/wtp/documentation/game-folder-files/): Updated the page with the latest additions and changes
- [WTP Visuals](/fo4/wtp/documentation/wtp-visuals/): Added page to discuss WTP's graphics mods, including a list of textures in the five WTP repacks
- [WTP Gameplay](/fo4/wtp/documentation/wtp-gameplay/): Added page to discuss WTP's gameplay changes, including custom hotkeys and unique item locations
- Renamed the "Troubleshooting" page to "Known Issues"
- [Known Issues](/fo4/wtp/known-issues/): Added "Invisible Spouse" bug
- [Known Issues](/fo4/wtp/known-issues/): Updated the "Flickering Puddles" bug, eliminated in WTP 2.0
- [Known Issues](/fo4/wtp/known-issues/): Removed the "Nights are too dark" section (they are no longer as dark in WTP 2.0)
- [Known Issues](/fo4/wtp/known-issues/): Added the "Load screens appear frozen" issue (which is not actually an bug)

---

## Release 1.6.3

> 14/08/2021

This update finally brings back WTP after an extended downtime due to Nexit. I was extremely unhappy to remove the Stormy Nights main menu replacer and Full Dialogue Interface (for which the string patch was taken down), but there is nothing to be done. I apologise that it took me so long to bring WTP back, it remains more of a smaller side project for me and sadly I have not felt the Fallout 4 itch in quite some time. Nevertheless, the list has always been doing surprisingly well, much better than I had expected, so I will definitely continue to maintain it.

This is update is **not save-safe**. Please copy over the Game Folder Files into your root folder once again as the ENB binaries were updated.

#### Mod Changes

- Disabled frame limit in enblocal.ini (oversight from when I reinstalled ENBSeries in 1.6.2)
- Enabled VSYNC in High FPS Physics Fix (should always be on)
- Removed the main menu replacer as it was deleted from the Nexus (damn shame, it's been my favourite for years)
- Removed More Attackers - Get Off My Buildzone as a master from the CRP
- Removed More Attackers - Get Off My Buildzone (removed from the Nexus)
- Removed Full Dialogue Interface
- Removed String Patches for Full Dialogue Interface (removed from the Nexus)
- Removed F4 Creation Kit Fixes from Game Folder Files
- Updated ENBSeries binaries to 0.461
- Updated Workshop Framework to 2.0.16
- Updated Synthkind Redefined HD to 1.01
- Updated What's Your Name to 1.12.1
- Updated Vault 88 Essentials to 1.1
- Added Extended Dialogue Interface

## Release 1.6.2

> 27/06/2021

This is just a quick update to fix two minor issues and update a couple of mods. Since Wabbajack updated to 2.5.0.0, I had to recompile anyway.

Update your **Game Folder Files** to get the new ENBSeries binaries. The update is **save safe**.

#### Mod Changes

- Updated ENBSeries to 0.458
- Updated the Unofficial Fallout 4 Patch to 2.1.3
- Updated Buffout to 1.23.1
- Updated Workshop Framework to 2.0.15a
- Updated FallUI - Inventory to 1.13.3
- Updated FallUI - HUD to 1.4
- Updated Console Commands Extender to 1.2.0
- Maybe fixed UI elements sometimes being misaligned
- Fixed a few minor issues in Home Plate (thanks C19i)

## Release 1.6.1

> 04/06/2021

As it turns out, I got sloppy last night. I'd already recompiled once when [Bullet Counted Reload System](https://www.nexusmods.com/fallout4/mods/41178) updated and part of the update was support for [Tactical Reload](https://www.nexusmods.com/fallout4/mods/49444). I dropped in both, did a cursory check in xEdit, fixed some conflicts, and called it a day. Evidently I shouldn't have done that as something about the combination has caused frequent crashes in WTP 1.6 that was reported twice so far and I was able to reproduce it on my end. Dropping Tactical Reload fixed it so at least there was an easy solution. I haven't investigated further why exactly the crashes happen because I frankly don't care about the mod that much and don't have time today either.

This update is **save safe**. It's a crash fix. You'll be asked about missing plugins when loading your save, click Yes.

#### Mod Changes

- Removed Tactical Reload
- Replaced the TR version of BCR Lever Action Rifle with the regular one
- Removed Tactical Reload as a master from the CRP

## Release 1.6

> 03/06/2021

**Starting a new game is required.**

For this update I checked out the new **FallUI** suite of interface replacers and took the opportunity to review WTP's existing interface mods. I came to the decision to once again remove [Extended Dialogue Interface](https://www.nexusmods.com/fallout4/mods/27216) and revert to [Full Dialogue Interface](https://www.nexusmods.com/fallout4/mods/1235) which I like far better. After careful consideration, I decided *against* including [FallUI - HUD](https://www.nexusmods.com/fallout4/mods/51813) because even with my DEF_UI HUD preset, it would make item pickup prompts look [weird](https://i.imgur.com/Bd9w9VZ.jpg) with a huge gap between the item name and the button prompts. I also removed FallUI - Map because I didn't like it. However, FallUI - HUD and FallUI - Map are still going to be installed in case someone wants them (but are disabled by default).

I also removed **Widescreen** support. I can't test it, it's additional headache, I'd have to write extra instructions for changing the aspect ratio in the various FallUI MCMs. Sorry to everyone on ultrawide monitors, it's just not worth the effort to me.

When updating, please also move the Game Folder Files into your root folder and overwrite (ENB binaries updated).

#### Mod Changes

- Added zEdit (I needed it for one merge)
- Added deorder's MO2 Plugins (only useful for me)
- Added F4 Creation Kit Fixes (only useful for me)
- Added DEF_HUD - My Preset (smaller vanilla, crosshair to dot)
- Added Tactical Reload
- Added Jamaica Plain Navmesh Fix
- Added Weston Water LOD Fix
- Added Assaultron Left Hand Hydraulic Frame Arm Mesh Bug Fix
- Added Perception Bug Fix
- Added Carlisle Typewriter Mesh Fix
- Added Car Physics Death Bug Fix
- Added 1 Rad Bugfix
- Added Far Harbor Marine Armor Boots Fix
- Added Cryo Fix
- Added Cryolator Cryo-Cell Fix
- Added Pool Rack Fix (finally the game is playable)
- Added X-01 Power Armor Neck and Minor Light FX Fix
- Added FallUI - HUD (disabled by default)
- Added Full Dialogue Interface
- Added String Patches for Full Dialogue Interface
- Added UNLIMITED POWER - Tesla Rifle Projectiles Create Visual Effect on Impact
- Added Fix for Forsythia
- Added Far Harbor Pine Branches
- Added The Natural Bundle - Masonry Set
- Added The Natural Bundle - Submarine Set
- Added Defined Hightech Floor Tiles
- Added Fix for Tiles02
- Added ADs 2X Rez
- Added Wall Worldmap
- Added Globes (retexture)
- Added Library and Subway Tokens HD Remastered
- Added Deathclaws HD Retexture
- Added The Flamer Project
- Added Leafblower Junk Jet
- Added Synthkind Redefined
- Added Auto Lockpick
- Added Auto Hack
- Added Better Explosives Redux
- Added Fortune Finder 4 Fix
- Added Vault 88 Template - Optimised
- Added Workshop Power Pack
- Added Vault 88 Essentials
- Added Vault 88 Essentials - WTP Tweaks
- Added Whose Quest Is It Anyway
- Added River Fix
- Updated Mod Organizer 2 to 2.4.2
- Updated ENBSeries to 0.455
- Updated Buffout to 1.23.0
- Updated Bullet Counted Reload System to 2.0
- Updated Workshop Framework to 2.0.14a
- Updated Wetness Shader Fix to 3.41
- Updated Companion Stealth Distance Fix to 7.0
- Updated FallUI Confirm Boxes to 2.1
- Updated FallUI Workbench to 1.2.4
- Updated Fallout 4 Ultimate Window Overhaul to 3.1
- Updated Visible Idle Markers to 1.6
- Updated LOST Audio Tweaks to 1.7a
- Updated the LOST Audio Tweaks - True Storms and RAO Patch to 1.1
- Removed Extended Dialogue Interface
- Removed Scrolling Doesn't Change PoV
- Removed Valentine Jaw Sync (part of Synthkind Redefined)
- Removed Weapon Rack Fixes (largely covered by UFO4P)
- Removed Detailed Deathclaws
- Removed Fallout 3 NV Feral Ghouls Replacer
- Removed Simple Crafting Station - K-9 Harness Patch
- Removed Sprint Engine Limitations
- Reinstalled Fixed Flickering Puddles (was missing one file, may fix lingering issues)
- FallUI - Map is now disabled by default
- Rebuilt the Weapons BA2s
- Rebuilt the Creatures BA2s
- Deleted the broken IMAD record in True Nights to be on the safe side (I tweaked it before but can't remember how)
- Regenerated precombines for the area around the new Sanctuary bridge (thanks for talking me through that, Lively!)
- Removed Fortune Finder tweaks from Loot Logic Scrounger Fortune Finder Rebalance
- Reverted UNLIMITED POWER changes to Tesla Rifle damage, capacity, and reload speed
- Added new 'Backpack' tag to DEV_INV_TAGS.xml
- Merged the three music plugins together and removed the separate plugins
- Replaced the now redundant music patch with the merged plugin
- Extracted the Fallout Suite BA2 since there is no longer a plugin to load it
- Fixed some conflicts between Better Explosives Redux and other mods
- Regenerated INI files from scratch

**K-9 Harness**

Until now fadingsignal's K-9 Harness for Dogmeat could be crafted at the crafting station which was the original implementation. I have never been happy with this and in this update I finally did something about it. You can now find exactly *one* K-9 Harness in the world. The location happens to be a police station for obvious reasons - if you want to know where exactly you can find it, double-click the new K-9 Integration Patch in Mod Organizer 2 and check the **Notes** tab.

**Creation Club**

WTP 1.6 adds *optional* support for some "creations" (only the Modular Military Backpack so far). You can find details and instructions [here](/fallout-4/wtp/wtp-resources/creation-club).

#### Website Changes

- Updated a bunch of pages. Added stuff on the **Finalisation** page. Don't remember everything.
- Added a link for LostDragonist's Steam Library Setup Tool on the **Fallout 4** page.
- Removed Widescreen support stuff from the **Finalisation** page (sorry).
- Added new **Creation Club** page under Resources for Modular Military Backpack support.
- Removed the Custom Files page. All relevant documentation was moved into Mod Organizer 2 (check the Notes for each mod).
- Linked to True Nights for instructions on how to change night brightness on **Troubleshooting**.

## Release 1.5.2

> 06/04/2021

This update is safe-save. Copy over the GFF into your root folder and overwrite (ENB binaries updated).

#### Mod Changes

- Updated Mod Organizer 2 to 2.4.1
- Re-arranged and re-coloured MO2 separators
- WTP changelogs are no longer available through MO2
- Updated ENBSeries (no version change)
- Updated Buffout 4 to 1.22.0
- Updated PrivateProfileRedirector to 0.5.2
- Updated High FPS Physics Fix to 0.8.3
- Updated What's Your Name to 1.12.0
- Added Less Annoying Water Foam Circles
- Added No Quest Autostart - BoS Fire Support
- Added No Quest Autostart - Automatron
- Added No Quest Autostart - Vault-Tec
- Added No Quest Autostart - Far Harbor
- Added No Quest Autostart - Nuka World
- Removed some unnecessary stuff from the Phoenix Tweaks plugin

#### Website Changes

- **Finalisation:** Shortened the Resolution section and moved Ultrawide tweaks to this page.
- **Ultrawide:** Removed this page.

*Turns out that Wabbajack auto-sets the resolution in the INI files.*

## Release 1.5.1

> 08/03/2021

I fixed some errors in `Power Armor Lore-Friendly Distribution.esp` by reverting the levelled lists for Atom Cats power armor to vanilla. That means they'll be wearing T-60 armor again (instead of T-51). I know I had Atom Cats T-51 armor *somewhere* but it seems to have gotten lost, resulting in these errors. I fully admit that this is a lazy solution but it works and that was always enough for Todd anyway.

While recompiling for WJ, I also updated the links to the website (see below).

## Global Site Update

> 08/03/2021

I finally did some spring cleaning. For the longest time it annoyed me that in my original folder structure I had categorised pages by games, for example the TPF part of the website was called "Skyrim SE" in the top menu. But what if I want to start another SE project? And you don't want to know the chaos in my pictures folder either.

The reason I hesitated for so long to change the folder names is because it breaks every, single, link. And while fixing the internal links and file paths was merely a minor annoyance, fixing all external links is more difficult - especially considering that other people may link to TPF as well and those links are now broken. Of course I also need to recompile both TPF and WTP for Wabbajack to update the links that open automatically upon installing a Wabbajack list.

Well, I finally updated now and I'm very happy with the changes. It likely will take some time for all external links to get fix plus I suspect I may have missing some internal links and file paths.

#### Changes

- Removed the Bioware section (see below).
- Renamed "Skyrim SE" to "The Phoenix Flavour" (link changed from skyrim-se to tpf).
- Renamed "Fallout 4" to "Welcome to Paradise" (link changed from fallout to wtp).
- Updated all internal links and file paths - hopefully.
- Cleaned up my pictures folder to remove any pictures that are no longer in the guide.
- Updated the home page, it has two buttons now and a combination of the TPF and WTP pics.

#### Bioware

The current state of things is that I have published a guide for ME1 with a draft for an ME2 version waiting for revision. But here's the thing: Modding Bioware games is quite different from modding Bethesda games. I've only really dipped my toes in it and wouldn't call myself an expert by any stretch of the imagination. Something I often criticise about various smaller Skyrim modding "guides" is that their authors barely know what they're doing. It occured to me that my Mass Effect "guides" are in essence the same thing ~~with better formatting~~.

To keep a longer story short, I have developed a strong sense of imposter syndrome over those excursions into Bioware land that is causing me a fair amount of stress. Something I've learned over the past couple years is that if you have too many things putting pressure on you at once, cut out everything that's non-essential. Well, this time the scissors are for the Bioware section of the TPF website.

## Release 1.5

> 06/03/2021

#### Mod Changes

- Updated Mod Organizer 2 to 2.4.0
- Tweaked Pipboy INI settings (increased resolution, disabled fx)
- Added Mator's xEdit Patching Framework
- FO4Edit cache is now saved into the Tools\FO4Edit folder
- Updated xSE Plugin Preloader to 0.2.4
- Changed xSE Plugin Preloader load method to OnThreadAttach
- Updated Buffout to 1.20.3
- Updated the Unofficial Fallout 4 Patch to 2.1.2b
- Updated High FPS Physics Fix to 0.8.0
- Removed additional High FPS Physics Fix INIs
- Default settings for WTP are now 60FPS and no VSYNC
- Documentation includes instructions to change the settings
- Reinstalled DEF_UI and only chose DEF_HUD
- Reverted to vanilla DEF_UI profile
- Added FallUI
- Added FallUI Workbench
- Added FallUI Map
- Re-added LooksMenu
- Added Better Confirm Boxes for PC
- Added TRUBY9 ULTRAWIDE DEF_UI Fix
- Added Better Confirm Boxes for PC - Widescreen Patch
- Added Neutral Look Up Tables LUT
- Added Fallout 4 Enhanced Color Correction
- Added Retro Radio Replacer
- Added Classic Wasteland Survival Guide - Magazine Retexture
- Added U.S. Covert Operations Manual - Magazine Retexture
- Added Total Hack - Magazine Retexture
- Added The Hunting Rifle Set
- Added The Ballistic Series
- Added Fixed Creature Death Drops
- Added FO4 Photo Mode
- Updated Workshop Framework to 2.0.10
- Updated Simple Sorting Overhaul to 2.0
- Updated Wetness Shader Fix to 3.3
- Updated Sprint Stuttering Fix to 1.2
- Updated Hazmat Suit Redux to 0.1
- Updated Skeletal Adjustments for CBBE to 2.0
- Updated What's Your Name to 1.11.1
- Updated Fixed and Cleaned Homeplate to 2.1
- Updated LOST Audio Tweaks to 1.6.2
- Updated LOST Audio Tweaks - True Storms and RAO Patch to Beta
- Removed Pip-Boy Dual Color section
- Removed Small Map Markers
- Removed The Humble Hunting Rifle
- Removed ScratchMade - New Combat Shotgun and Rifle Textures 
- Removed The Top-Notch Tommy Gun
- Removed Assault Rifle Retexture 2K
- Removed HUD Customisation stuff
- Repacked the Clutter BA2s
- Repacked the Weapon BA2s
- Changed ENB hotkeys to mirror TPF's

#### Simple Sorting Overhaul

As we have now switched to FallUI from DEF_INV, I updated my INNRs (naming rules) to have the same format as Ruddy's sorting patcher that FallUI was intended for. That means mods for armors and weapons will be displayed in smaller font below the item name.

I did take a look at the [Complex Sorter](https://www.nexusmods.com/fallout4/mods/48826) for FallUI which would be very convenient for me but ultimately I prefer my own icons and INNRs. Plus they already cover my power armor changes and include my preferred power armor naming scheme.

#### Website Changes

I went over all pages and fixed what I thought needed fixing. Screenshots were updated, sentences were rephrased, and instructions were clarified.

- **Finalisation:** Added instructions for the optional LUTs.
- **Finalisation:** Added Controller Fix instructions (required because of an issue with FallUI).
- **Finalisation:** Expanded FPS and VSYNCs instructions (they are DIY now).
- **New Game:** Removed Hotkey instructions. No longer necessary with TPF ENB hotkeys.
- **Mod Configuration:** Added instructions for Photo Mode.
- Renamed the "Documentation" section to "Resources".
- **Ultrawide:** Moved this page to the Resources section.
- **Customisation:** Removed this section. Use the FallUI MCM to customise your UI.
- **Troubleshooting:** Added a note about flickering puddles.

## Release 1.4.1

> 26/11/2020

#### Mod Changes

- Re-enabled Authentic Handmade Weaponry (accidentally disabled the plugin in 1.4)

## Release 1.4

> 23/11/2020

#### Mod Changes

- Added Weapon Debris Crash Fix
- Added Sprint Stuttering Fix
- Added Less Ugly Intercom
- Added The Laser Series
- Added The Plasma Project
- Removed The Lavish Laser Musket
- Removed The Lavish Laser Collection
- Rebuilt the Weapons BA2
- Updated Buffout to 1.17.1
- Updated Wetness Shader Fix to 3.2
- Updated Handmade Turrets to 1.3.2
- Updated Workshop Framework to 2.0.6
- Updated Indubitably Ivy to 0.2
- Updated What's Your Name to 1.10.0
- Updated Skeletal Adjustments for CBBE - Knee Fix to 1.1
- Updated LOST Audio Tweaks to 1.5.1
- Updated custom Sound Slider Tweaks plugin
- Slightly tweaked High FPS Physics Fix presets
- Unhid message box and tutorial messages in my DEF_UI preset

## Release 1.3.1

> 24/10/2020

Just a minor fix and clean-up for yesterday's update.

#### Mod Changes

- Updated Bullet Counted Reload System to 1.05b
- Updated Workshop Framework to 2.0.3
- Added missing ALWAYS INCLUDE flags to High FPS Physics Fix profiles

## Release 1.3

> 23/10/2020

This update fixes a number of issues reported by users (thanks, guys!). I am also officially changing the list name to **Welcome to Paradise**. The website, Discord channels, and Mod Organizer 2 profile have all been edited accordingly.

#### Mod Changes

- Hopefully fixed radio songs not playing for good
- Updated xSE Plugin Preloader to 0.2.3 (XML unchanged, let me know if there are issues)
- Updated Buffout 4 to 1.16.1
- Fixed some untranslated UI bits (missing strings)
- Removed Auto Gamepad Switch (caused some issues)
- Fixed scrap tag for Stogie
- Added High FPS Physics Fix plus pre-configured INIs
- Removed the separate DEF_UI preset, now editing the one packaged with the main mod
- Re-enabled compass markers for locations / Dogmeat / PA in DEF_UI
- Turns out Archive2 is unreliable so I repacked a bunch of BA2s with CAO
- Unpacked custom BA2 for Bleak Beauty, Musical Lore, More Where That Came From, and Elvani's Track Pack
- Fixed some purple cars by reverting them to vanilla, it's a band-aid fix but the best I could do

#### Website Changes

- **Finalisation:** Removed instructions for NVIDIA Inspector.
- **Finalisation:** Added instructions for the newly-added High FPS Physics Fix and my pre-configured INIs.

## Release 1.2.1

> 01/10/2020

#### Mod Changes

- Actually fixed radio tracks not playing
- Updated xSE Plugin Preloader to 0.2

Please delete **xSE PluginPreloader.ini** from your **root** folder. Move the new **xSE PluginPreloader.xml** and updated **IpHlpAPI.dll** into your **root** folder and overwrite when prompted.

## Release 1.2

> 30/09/2020

#### Mod Changes

- Updated Buffout to 1.12.1
- Placed the new Buffout TBB Redist plugin in the Game Folder Files folder
- Removed Achievements (this is now a feature in Buffout)
- Actually fixed the problematic True Nights record instead of bruteforce deleting it
- Updated Classic Hostered Weapons System to 1.04c
- Added Start Me Up - Basic Version
- Added Lively's Start Me Up Tweak
- Resolved a conflict between Start Me Up and the UFO4P
- Inlined Lively's PPPL INI file
- Updated Sweet Roll 5000 and rebuilt Clutter BA2s
- Fixed Diamond City Radio tracks not playing (thanks Archie!)

#### Website Changes

- [Finalisation](/fo4/wtp/installation/finalisation/): Added this new page and moved the game resolution instructions here.
- [Finalisation](/fo4/wtp/installation/finalisation/): Added instructions on how to force VSYNC and cap the framerate.
- [New Game](/fo4/wtp/installation/new-game/): Removed LooksMenu related instructions as that mod was removed.
- [New Game](/fo4/wtp/installation/new-game/): Added *seriously* detailed instructions for Start Me Up.

## Release 1.1

> 27/09/2020

#### Mod Changes

- Now using Lively's pppl.ini file
- Updated Buffout to 1.11.0
- Removed one record from True Nights which can cause memory corruption according to Buffout
- Removed LooksMenu (don't really need it anyway)
- Enabled the Classic Holstered Weapons Systems patch in Buffout
- Adjusted loot / interact prompt and window position in my DEF_UI preset
- Switched to the Alternative Version of Fixed Flickering Puddles (hopefully fixing black pre-war Codsworth)
- Removed Skip raiding your own settlements (no time to troubleshoot the compilation error it causes)

#### Website Changes

- [Wabbajack](/fo4/wtp/installation/wabbajack/): Added new section on how change the game resolution.
- [Troubleshooting](/fo4/wtp/appendix/troubleshooting/): Added this page with a few known issues.

## Release 1.0.1

> 26/09/2020

- Rolled back to **Buffout 4** 1.7.0 as the latest version is causing crashes.

## Release 1.0

> 26/09/2020

Initial release. For more info check the [Patreon post](https://www.patreon.com/posts/phoenix-flavour-42049352).