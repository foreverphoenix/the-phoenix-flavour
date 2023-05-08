---
title: "Changelog"
weight: 8
type: docs
description: >
  Update notes for Skyrim Modding Essentials.
---

## Release 2.4.1

> 08/05/2023

- Updated ENBSeries Binaries (no version number change)
- Deleted scripts from DynDOLOD Resources (yes, I forgot again)

## Release 2.4

> 08/05/2023

With this update I am adding quite a few script-related fixes and improvements that I had previously been wary of. The simple reason for this that I am utterly clueless when it comes to Papyrus or really code of any kind, so I am stuck with trusting the mod authors know what they do which is not so easy because it is my responsibility that SME offers as solid a base as possible. On the other hand, nearly all of the additions are script modifications by ferrari365 who takes the time to explain their edits which is extremely helpful. I also had a close look at the respective comment sections (though user reports are generally unreliable) and decided that it should be safe enough to add their mods.

#### Mod Changes

- Added Vanilla Script (Micro)Optimizations
- Added Mannequin Management
- Added Beneath Bronze Waters Start Fix
- Added dunfolgunthurbossbattle Script Fix
- Added The Taste of Death Improved Shutdown
- Added Soul Cairn Script Tweaks
- Added dlc2tribalwerebearscript Fix
- Added dlc2dunfrostmoontriggerscript Optimization
- Added dlc2dunnchardarkdoorseal Script Infinite Loop Fix
- Added dlc2dunseekerinvisscript Fix
- Added dlc2miraakscript Fix
- Added Bone Wolf Shutdown Fix
- Added lilebonymaces Patches
- Updated DynDOLOD to 3 Alpha 127
- Updated Universal Cured Serana Eye Fix to 0.2
- Updated DynDOLOD Resources to 3 Alpha 36
- Removed wideadbodycleanupscript Crash Fix
- Created new **Script Fixes** separator
- Created new **Late Loader** separator
- Moved the BodySlide / Outfit Studio installation from the Tools folder to a mod folder

#### Website Changes

- **Installation:** (Hopefully) fixed the BodySlide setup instructions

## Release 2.3.3

> 28/04/2023

Small update to add DynDOLOD NG for people who would like to try out the experimental version (with the large ref bug workarounds). Only use it if you know what you are doing and remember it requires all plugins to be 'cleaned' of deleted references. Also added a super neat MO2 plugin, LOOT Warning Checker, that is helpful for finding plugins that need 'cleaning' for DynDOLOD NG.

- Added LOOT Warning Checker MO2 Plugin
- Added DynDOLOD NG
- Updated DynDOLOD to 3 Alpha 125
- Updated DynDOLOD Scripts to 2.82.5
- Updated DynDOLOD Resources to 3 Alpha 35
- Removed Nchuanthumz Papyrus Load Fix (part of USCCCP)

## Release 2.3.2

> 22/04/2023

Small maintenance update with some much-needed fixes for the documentation.

- Added Mod Organizer 2 Splash Screen - Intro Title Style
- Updated xLODGen to 98
- Updated Spell Perk Item Distributor to 6.5.2
- Updated Keyword Item Distributor to 3.0.2
- Updated FormList Manipulator - FLM to 1.6.0
- Updated DynDOLOD Resources to 3 Alpha 34
- Updated ENBSeries Binaries (no version number change)
- Set Pause to True in the QUI TOML (game will be paused while viewing the plugin explorer)

#### Website Changes

- **Installation:** Fixed a bunch of typos
- **Installation:** Removed Antivirus Exclusion section
- **Installation:** Added Tools Setup > Cathedral Assets Optimizer section
- **Installation:** Added Tools Setup > Nemesis section
- **Documentation:** Updated ENB instructions for Root Builder

## Release 2.3.1

> 08/04/2023

**Website:** Fixed a bunch of broken links in the features list on the [Introduction](/skyrim-se/sme/introduction/) page. Thanks to /u/onedoor for making me aware!

- Added SkyUI - Survival Mode Integration - Widescreen Fix (disabled by default)
- Added Dragonactorscript Infinite Loop Fix
- Updated Synthesis to 0.25.4
- Updated DynDOLOD to 3 Alpha 122
- Updated Spell Perk Item Distributor to 6.5.1
- Updated Sprint Sneak Movement Speed Fix to 1.1.1
- Updated DynDOLOD Resources to 3 Alpha 33
- Updated ENBSeries Binaries (no version number change)
- Removed Race Menu - Widescreen Fix (not needed anymore)
- Separated config files from Enhanced Invisibility and Enhanced Reanimation
- Config Files for Enhanced Invisibility and Enhanced Reanimation are no longer modified
- Flagged SkyUI_SE.esp as ESL

## Release 2.3

> 16/03/2023

With this update I am including relevant ModGroups I created while working on Aurora / TPF. The CC ones are not for any of the four mandatory ones so they are off by default and they may also use different CRCs since I slightly modified some plugins. In that case, you can quickly update them in xEdit (or just disable all ModGroups altogether if they are not part of your workflow).

- Added Initially Disable - SSEEdit Script
- Added ModGroups file for several creations (hiding conflicts with the official master files)
- Added ModGroups file for the Unofficial Skyrim Creation Club Content Patch
- Added ModGroups file for Myrwatch - Editable Home Cells (Cell Bug Workaround)
- Added Sunder and Wraithguard - Editable Vault Cell (Cell Bug Workaround) - USCCCP Patch
- Added Scrambled Bugs - Script Effect Archetype Crash Fix
- Added ModGroups file for Chillwind Depths CTD Fix
- Added Sprint Sneak Movement Fix
- Updated DynDOLOD to 3 Alpha 119
- Updated Quest Journal Limit Fixer to 0.2.1
- Updated Scrambled Bugs to 21.0
- Updated Scrambled Bugs - Settings
- Updated Rock Traps Trigger Fixes to 1.2
- Updated Bug Fixes SSE to 10.0
- Updated Actor Limit Fix to 9.0
- Updated DynDOLOD Resources to 3 Alpha 32
- Moved USSEP ModGroups file to separate mod folder
- Expanded USSEP ModGroups to hide some conflicts with CCs

## Release 2.2

> 10/03/2023

It has recently been brought to my attention that the latest version of the Creation Kit and the updated version of CK Fixes *may* have some lingering issues. As a matter of precaution I decided to (for the time being) roll back to CK 1.5.73 and the original CK Fixes.

Regarding the removal of Mannequin Management: Technically, the mod should have been redundant since Skyrim 1.6.629.0 in which Beth slapped the Immobile flag on the MannakinRace record (an undocumented change, of course). This should (?) resolve the issue.

- Added ACMOS Road Generator
- Added Creation Kit Fixes
- Added Wider MCM Menu for SkyUI
- Added Skyrim Ultimate Eye Meshes Ruhmastered
- Added Ore Vein Texture Fix
- Added Ore Vein Cube Map and Shader Fixes
- Added Whiterun Fence Base Seam Fix
- Added Farm Hat 01 Clipping Fix
- Added Guild Master's Armor First Person Texture Fix
- Added Glowing Mushroom Collision Fixes
- Added No More Swimming In Air - Fixed Floating SwimIdle
- Added Wider MCM Menu for SkyUI - Widescreen Fix (disabled by default)
- Added ENB IMOD Separator (disabled by default)
- Updated DynDOLOD to 3 Alpha 118
- Removed Creation Kit Fixes Update
- Removed Mannequin Management
- Removed Cumulative Fix for Eye Meshes
- Actually applied my custom ENB hotkeys as outlined in the documentation (oops)
- Fixed minor issue in the mesh from Hearthfire Creep Cluster Fix to prevent random CTDs
- Deleted change to the iron ore smelting recipe from Hearthfire Houses Building Fix
- Restored some erroneously deleted meshes in Labyrinthian Shalidor's Maze Fixes
- Reinstalled the Particle Patch for ENB to select the BSA-packed version
- Removed redundant copy of the ENB binaries from the Tools folder
- Rolled back the Creation Kit to 1.5.73

## Release 2.1.1

> 23/02/2023

So turns out that I, at some point, fucked up the SSE Display Tweaks config file which should NOT replace the default one, but add to it. Even if you are not installing this update (which should be true for all existing users), please rename the config file in the SSE Display Tweaks - Settings mod to **SSEDisplayTweaks_Custom.ini** and reinstall the main SSE Display Tweaks mod to restore the full INI. Sorry for the inconvenience.

Also I re-arranged the separators again, distributing the CC-related mods to existing sections. They are still of by default though.

#### Mod Changes

- Added Staves (Creation) - Minor Fixes
- Added CC Horse Armor Stays Token
- Removed Horse Armor No Longer Disappears
- Fixed SSE Display Tweaks config file

## Release 2.1

> 23/02/2023

I have begun work on a visuals-only mod list based on SME and immediately felt the need to improve the baseline. After deciding to adopt a standardised system of separators across my various setups, I modified the ones in SME accordingly and, while I was at it, I also switched up the garish colours. MO2 is prettier now, yay.

Most importantly, I added the **Essential Mods - Creation Club** section with a handful of mods that I consider, well, essential when using any creations. They are all optional and disabled by default; the AE DLC is no requirement for SME.

#### Mod Changes

- Added Unofficial Skyrim Creation Club Content Patch
- Added Myrwatch - Editable Home Cells (Cell Bug Workaround)
- Added Sunder and Wraithguard - Editable Vault Cell (Cell Bug Workaround)
- Added SkyUI - Survival Mode Integration
- Added Survival Mode Prompt Removed
- Added Arcane Blacksmith's Apron - Hood Fixes
- Added Nchuanthumz Papyrus Load Fix
- Added Horse Armor No Longer Disappears
- Added Nix-Hound Eyes Fix (Creation Club Nixhound Patch)
- Updated Papyrus Tweaks NG to 4.1.0
- Updated DynDOLOD to 3 Alpha 116
- Shuffled around some mods and separators

## Release 2.0

> 22/02/2023

After a long hiatus, here's a major update for y'all.

- Updated to SSE 1.6.640.0 (Steam) / SSE 1.6.659 (GOG)
- Root Builder is now enabled by default
- Cleaned non-vanilla files out of the Stock Game Folder

I also re-arranged some separators.

FYI, one of the added mods (Rock Traps Trigger Fixes) requires a new game.

#### Mod Changes

- Added updated MO2 plugin for GOG support
- Added Creation Organizer
- Added CK Fixes Update
- Added FormList Manipulator
- Added Payload Interpreter
- Added Unique Map Weather
- Added Keyboard Shortcuts Fix (SKSE Preloader)
- Added Papyrus Tweaks NG
- Added ConsolePlusPlus
- Added Combat Music Fix NG
- Added Animation Queue Fix
- Added Magic Student (WIChangeLocation04) Quest Fix
- Added Rock Traps Trigger Fixes
- Added DynDOLOD - DLL
- Added DynDOLOD - Scripts
- Added Dynamic Animation Casting - NG
- Updated Root Builder to 4.4.2
- Updated Profile Sync to 1.1.1
- Updated Crash Logger SSE AE VR to 1.8.0
- Updated ENBSeries Binaries to 0.488
- Updated PapyrusUtil SE - Modders Scripting Utility Functions (Steam) to 4.4
- Updated Papyrus Extender to 5.5.0
- Updated JContainers to 4.2.3
- Updated Spell Perk Item Distributor (SPID) to 6.4.0
- Updated Keyword Item Distributor to 2.2.0
- Updated Sound Record Distributor to 1.3.0
- Updated Base Object Swapper to 2.5.1
- Updated MergeMapper to 1.4.0
- Updated Scaleform Translation Plus Plus to 1.6.0
- Updated Fuz Ro D-oh - Silent Voice to 2.3
- Updated QUI to 0.3.2
- Updated SSE Engine Fixes to 6.1.1
- Updated Fix Note Icon for SkyUI to 1.2.6
- Updated RaceMenu to 0.4.19.14
- Updated More Informative Console to 1.1.0
- Updated ConsoleUtilSSE to 1.4
- Updated Console Commands Extender to 1.11
- Updated NVIDIA Reflex Support to 1.1.2
- Updated Auto Input Switch to 1.2.0
- Updated Bug Fixes SSE to 9
- Updated powerofthree's Tweaks to 1.8.0
- Updated Scrambled Bugs to 20
- Updated Equip Enchantment Fix to 1.3.6
- Updated Actor Limit Fix to 8
- Updated NPC AI Process Position Fix - NG to 1.1.1
- Updated Animated Static Reload Fix - NG to 1.0.1
- Updated HD Local Map to 1.0.2
- Updated Mfg Fix to 1.6.1
- Updated Shadow Boost to 1.3
- Updated ENB Helper to 2.2
- Updated ENB Input Disabler to 1.0.3
- Updated ENB Helper Plus to 1.0.4
- Updated Particle Patch for ENB to 1.2.3
- Updated CritterSpawn Congestion Fix to 1.3
- Updated Assorted Mesh Fixes to 0.78
- Updated DynDOLOD Resources to 3 Alpha 31
- Updated Animation Motion Revolution to 1.5.3
- Updated Dynamic Animation Replacer to 1.1.3
- Updated SSE NIF Optimizer to 3.2.0
- Updated Synthesis to 0.25.3
- Updated zEdit to 0.6.7
- Removed Creation Organizer
- Removed Show Animation Command (no 1.6.640+ support)
- Removed Keyboard Shortcuts Fix
- Removed Combat Music Fix SKSE
- Config files are now all separated from their "parent" mod and suffixed with "- Settings"
- Enabled SleepWaitTime in the SSE Engine Fixes - Settings
- Moved ENB files into MO2 (using Root Builder folder structures)
- Fixed zEdit file path

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