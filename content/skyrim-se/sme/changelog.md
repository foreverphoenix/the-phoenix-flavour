---
title: "Changelog"
weight: 8
type: docs
description: >
  Update notes for Skyrim Modding Essentials.
---

## Release 1.7

> TBD

After a semi-long hiatus, here's all the recent updates. The next *major* update (i.e. 1.8) will likely **update** to **SSE 1.6.640** and **SKSE 2.2.3**. This version is still using **SSE 1.6.353** and **SKSE 2.1.5**.

I may not have caught all updates as it is getting kinda tricky to manage the different Skyrim/SKSE versions across multiple mod lists.

#### Mod Changes

- Added CK Fixes Update
- Added FormList Manipulator
- Added Payload Interpreter
- Added Papyrus Tweaks NG
- Added ConsolePlusPlus
- Added Animation Queue Fix
- Added Magic Student (WIChangeLocation04) Quest Fix
- Added Rock Traps Trigger Fixes*
- Updated Crash Logger SSE AE VR to 1.6.0
- Updated Spell Perk Item Distributor (SPID) to 6.3.0
- Updated Keyword Item Distributor to 2.2.0
- Updated Sound Record Distributor to 1.3.0
- Updated Base Object Swapper to 2.5.1
- Updated QUI to 0.3.2
- Updated Assorted Mesh Fixes to 0.77
- Updated Particle Patch for ENB to 1.2.0
- Updated DynDOLOD Resources to 3 Alpha 30
- Updated SSE NIF Optimizer to 3.2.0
- Updated Synthesis to 0.25.2
- Updated zEdit to 0.6.7
- Updated ENB Binaries to 0.484

*Note that this mod requires a new game (which should not be an issue as SME is intended to only be installed for a new installation and not subsequently updated).

## Release 1.6

> 03/11/2022

Another round of mod and tool updates.

Note on Crash Logger: The latest version (1.2.0) does not currently work with SSE 1.6.353.0 so SME is using 1.1.0.

#### Mod Changes

- Added Sound Record Distributor
- Added Recursion Monitor
- Added MergeMapper
- Added Barter Limit Fix
- Added Aurora Fix
- Updated DynDOLOD to 3 Alpha 105
- Updated Synthesis to 0.24.1
- Updated zEdit to 0.6.6.2
- Updated Crash Logger SSE AE VR to 1.1.0
- Updated Base Object Swapper to 2.0
- Updated Keyword Item Distributor to 2.1.1
- Updated Particle Patch for ENB to 1.1.1
- Updated AnimObject Swapper to 1.1
- Updated DynDOLOD Resources to 3 Alpha 29
- Where In Special Edition Am I is now disabled by default

## Release 1.5.3

> 16/10/2022

- Restored accidentally deleted custom presets for Cathedral Assets Optimizer

## Release 1.5.2

> 15/10/2022

Just the most recent mod updates. SME is still on 1.6.353.

#### Mod Changes

- Added Crash Logger SSE AE VR
- Updated DynDOLOD to 3 Alpha 102
- Updated Cathedral Assets Optimizer to 5.3.14
- Updated Address Library for SKSE Plugins to 8
- Updated SSE Display Tweaks to 0.5.12
- Updated powerofthree's Papyrus Extender to 1.5.3
- Updated MCM Helper to 1.4
- Updated QUI to 1.3.1.1
- Updated Spell Perk Item Distributor (SPID) to 0.6.3
- Updated Sound Fix for Large Sector Drives to 4.0
- Updated powerofthree's Tweaks to 1.7.5
- Updated Enhanced Visibility to 1.3.0
- Updated Enhanced Reanimation to 1.5.1
- Removed Crash Logger

#### Website Changes

- **Installation:** Added note that the CK should be installed on the same drive / in the same Steam Library as Skyrim SE

## Release 1.5.1

> 29/09/2022

- Fixed Wabbajack installer failing on missing CCs

## Release 1.5

> 28/09/2022

For the forseeable future, SME will continue to use **SSE 1.6.353** until all mods have been updated. However, I recompiled with the latest version of Skyrim in my Steam folder, meaning that users also need to have the latest version to install SME. Wabbajack will downgrade the copy of the game in your Game Root folder. This way, you don't have to downgrade your Steam installation.

#### Mod Changes

- Added Console Commands Extender
- Added HelpExtender
- Added NVIDIA Reflex Support
- Added Shadow Boost (disabled by default)
- Added HD Local Map
- Added Universal Cured Serana Eye Fix
- Added Dwemer Ballista Crash Fix
- Added AnimObject Swapper
- Added Animation Motion Revolution
- Updated ENBSeries binaries to 0.477
- Updated DynDOLOD to 3 Alpha 99
- Updated MCM Helper to 1.3.3
- Updated SSE Display Tweaks to 0.5.11
- Updated powerofthree's Tweaks to 1.7.1
- Updated Enhanced Reanimation to 1.5.0
- Updated Face Discoloration Fix to 1.0.3
- Updated Sound Fix for Large Sector Drives to 3
- Updated Assorted Mesh Fixes to 0.73
- New separator "Console Improvements" (moved some mods around)
- Redownloaded the mandatory CCs (as WJ will otherwise downgrade them)
- Recompiled with latest Skyrim SE version
- Recompiled with Wabbajack 3

#### Website

- **Installation:** Updated to reflect that Skyrim SE 1.6.640.0 is now required

## Release 1.4

> 19/08/2022

#### Mod Changes

- Added UIExtension
- Added Hearthfires Houses Building Fix
- Updated Synthesis to 0.23.7
- Updated Assorted Mesh Fixes to 0.69
- Fixed file structure for Keyboard Shortcuts Fixes (mod will actually work now)
- Fixed Profile Sync failing when mod names contain special symbols
- Root Builder is now disabled by default (as was originally intended)
- Sync Mod Order is now disabled by default (succeeded by Profile Sync)

#### Website Changes

- **Installation:** Added a note about the CK installation being mandatory
- **Installation:** Added a note to also set an AV exclusion for the appdata Nemesis folder
- **Installation:** Added Synthesis setup instructions

## Release 1.3

> 11/08/2022

Small maintenance update and expanded documentation.

#### Mod Changes

- Added Root Builder (MO2 plugin)
- Added Profile Sync (MO2 plugin)
- Updated SSE Creation Fixes Update to 3.3
- Updated powerofthree's Papyrus Extender to 5.2
- Updated College of Winterhold Quest Start Fixes to 0.4
- Updated DynDOLOD Resources to 3 Alpha 28
- Restored proper SSE Display Tweaks Custom INI (doesn't currently modify resolution)

#### Website Changes

- **Installation:** Added .NET 6.0 SDK installation instructions (Synthesis prerequisite)
- **Installation:** Added a warning about antivirus programs and recommended setting exclusions
- **Installation:** Added Wrye Bash setup instructions
- **Installation:** Added BodySlide setup instructions
- **Documentation:** Added warning to generate terrain LOD to a location outside the MO2 directory
- **Documentation:** Added link to Althro's guide to LOD generation

## Release 1.2.1

> 31/07/2022

- Hotfix for the SSE Display Tweaks configuration file

## Release 1.2

> 30/07/2022

With this update, I migrated the SME documentation to the new Skyrim SE Lists section of the website which breaks all links. I fixed those I could think of but might have missed some in which case please let me know on Discord.

In other news, I disabled the Fix Game Registry Path plugin for now. It is very convenient for LOOT (which uses the registry key to locate the game), but isn't really needed for anything else and also breaks Creation Organizer. On top of that, it becomes cumbersome to constantly update the path when swapping between modded setups. I found a different solution for making LOOT work.

#### Mod Changes

- Added Quest Journal Limit Bug Fixer
- Added Enhanced Invisibility
- Added Enhanced Reanimation
- Added Combat Music Fix SKSE
- Added Keywords Fixed
- Added dunPOISoldiersRaidOnStart Script Tweak
- Added Modern Toggle Walk-Run Fix - With Cobb Controlmap Fix
- Updated Wrye Bash to 310 (non-beta)
- Updated bundled ENBSeries binaries
- Removed the Bashed Patch that SOMEHOW snuck into the Data folder
- Removed Modern Toggle Walk-Run Fix
- Fix Game Registry Path is now disabled by default

#### Website Changes

- **Introduction:** Fixed loadorderlibrary.com link for SME under Features
- **Installation:** Improved the MO2 prerequisites section and added NET 4.8
- **Installation:** Removed the NET 5.0 requirement (no longer needed)
- **Installation:** Added LOOT post-installation setup instructions
- **Installation:** Added zEdit post-installation setup instructions
- **Recommendations:** Removed Blood (Green) Dragon Texture Fix (included in the USSEP)
- **Recommendations:** Added Farm Hat 01 Clipping Fix

## Release 1.1

> 21/07/2022

Following feedback, I decided to do some pruning where more controversial "fixes" were concerned and add a few more tools. Some of these I have not been using extensively before and while I tested them all, I cannot exclude the possibility that I missed something in the setup. If that is the case I will fix it asap.

Including a section of fix mods is very difficult as many are somewhat subjective or not compatible with / required for every setup. For one mod in particular, I have had people both very happy about its inclusion and completely opposed to it. So I decided to yeet most mods that could possibly be controversial and wrote up [a list of recommendations](/sme/recommendations) instead. Refer to that, please.

Thanks to Tyler/Night_Thastus and Parapets in particular for your feedback and recommendations!

- Added LOOT 0.17.0 (latest version is incompatible with MO2's inbuilt version)
- Added LOOT Config Loader for Mod Organizer
- Added Wrye Bash
- Added BodySlide and Outfit Studio
- Added EasyNPC
- Added LostDragonist's MO2 Plugins
- Added PapyrusUtils
- Added Sound Fix for Large Sector Drives
- Added Mage Armor Script Fix
- Added Lights Out - Solitude Lighthouse Fix
- Added Freed Prisoners Use Items
- Added Scare My Enemy Bug Fix
- Added Chillwind Depths CTD Fix
- Added Hearthfire Creep Cluster Fix
- Removed Fast Travel Time Scale Fix
- Removed Hearthfire Display Case Fix
- Removed Whose Quest Is It Anyway
- Removed Rude Imperial Soldiers Escort Fix
- Removed Dawnguard Don't Hunt Cured Vampires
- Removed Skyrim Ultimate Eye Remastered
- Removed HD Serpentine Dragon and Mesh Fix
- Removed Blood (Green) Dragon Texture Fix
- Removed D13 Faster Get Up Stand Up
- Removed 3rd Person Dual Wield Animation Fix
- Now using the (custom) SSE Display Tweaks config to control game res (Wabbajack will set it to your native monitor resolution)
- The Fuz Ro D-oh config file will no longer be dumped into the Overwrite

## Release 1.0.1

> 20/07/2022

Removed the accidentally included Creation manifest folder (caused installation to fail for people who don't own AE).

## Release 1.0

> 20/07/2022

Initial release.