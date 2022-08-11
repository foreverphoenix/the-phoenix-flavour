---
title: "Changelog"
weight: 8
type: docs
description: >
  Update notes for Skyrim Modding Essentials.
---

## Release 1.3.1

> TBD

#### Mod Changes

- Fixed file structure for Keyboard Shortcuts Fixes (mod will actually work now)

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