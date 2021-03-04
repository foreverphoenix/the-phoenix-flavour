---
title: "Changelog"
weight: 4
type: docs
description: >
  Update notes for all non-Beta versions.
---

## Release 1.5

> TBD

#### Mod Changes

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
- Added FallUI
- Added FallUI Workbench
- Added FallUI Map
- Re-added LooksMenu
- Added Better Confirm Boxes for PC
- Added Better Confirm Boxes for PC - Widescreen Patch
- Added Retro Radio Replacer
- Added Classic Wasteland Survival Guide - Magazine Retexture
- Added U.S. Covert Operations Manual - Magazine Retexture
- Added Total Hack - Magazine Retexture
- Added The Hunting Rifle Set
- Added The Ballistic Series
- Added Fixed Creature Death Drops
- Updated Workshop Framework to 2.0.9
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

#### Simple Sorting Overhaul

As we have now switched to FallUI from DEF_INV, I updated my INNRs (naming rules) to have the same format as Ruddy's sorting patcher that FallUI was intended for. That means mods for armors and weapons will be displayed in smaller font below the item name.

I did take a look at the [Complex Sorter](https://www.nexusmods.com/fallout4/mods/48826) for FallUI which would be very convenient for me but ultimately I prefer my own icons and INNRs. Plus they already cover my power armor changes and include my preferred power armor naming scheme.

#### Website Changes

- **Finalisation:** Added Controller Fix instructions (required because of an issue with FallUI).
- **Finalisation:** Expanded FPS and VSYNCs instructions (they are DIY now)

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

- [Finalisation](/fallout/installation/finalisation/): Added this new page and moved the game resolution instructions here.
- [Finalisation](/fallout/installation/finalisation/): Added instructions on how to force VSYNC and cap the framerate.
- [New Game](/fallout/installation/new-game/): Removed LooksMenu related instructions as that mod was removed.
- [New Game](/fallout/installation/new-game/): Added *seriously* detailed instructions for Start Me Up.

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

- [Wabbajack](/fallout/installation/wabbajack/): Added new section on how change the game resolution.
- [Troubleshooting](/fallout/appendix/troubleshooting/): Added this page with a few known issues.

## Release 1.0.1

> 26/09/2020

- Rolled back to **Buffout 4** 1.7.0 as the latest version is causing crashes.

## Release 1.0

> 26/09/2020

Initial release. For more info, check the [Patreon post](https://www.patreon.com/posts/phoenix-flavour-42049352).