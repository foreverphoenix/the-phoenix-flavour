---
title: "Paper UI Overhaul"
weight: 3
type: docs
description: >
  Addon by Phoenix featuring various Interface mods and tweaks.
---

## About the addon

- **Author:** Phoenix
- **Support:** #tpf-addon-support
- Requires a complete, up-to-date and untouched TPF setup as base.
- No widescreen support (sorry).

Highly customisable UI overhaul featuring the SkyUI theme **Dear Diary** and various related mod. Includes *optional* support for QuickLoot and Paper World Map.

### Separator

- Create a new separator **PAPER UI OVERHAUL** in Mod Organizer 2.
- Place it right above the **GRAPHICS BASELINE** separator.
- All mods you install from this Addon go below that new separator.

> Feel free to change the colour for the new separator so it is distinct from the "official" ones.

### Incompatible Mods

A number of mods from the main guide will have to be disabled (unchecked in the mod order) for compatibility with this addon:

- **TWEAKS:** Better MessageBox
- **INTERFACE:** Remove QuickSave Button from SkyUI System Menu
- **INTERFACE:** Wider MCM Menu for SkyUI
- **INTERFACE:** Favorite Things - Extended Favorites Menu for SkyUI
- **INTERFACE:** Roboto Font Replacer
- **INTERFACE:** KenMOD - Time on Loading Screen

## Dear Diary

##### [moreHUD - Inventory Edition](https://www.nexusmods.com/skyrimspecialedition/mods/18619?tab=files)

#### Download Instructions

- **Main Files:** moreHUD Inventory Edition Loose Version

##### [Dear Diary - Paper SkyUI Menus Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/23010?tab=files)

#### Download Instructions

- **Main Files:** Dear Diary

#### FOMOD Instructions

- **Install Journal, Stats, System Menu?** Yes
- **Install Mod Configuration Menu?** Yes
- **Install Map Menu?** Yes
- **Install Biege (sic) Map Markers replacer?** No
- **Install Inventory etc replacer?** Yes
- **Install MoreHUD I.E. replacer?** Yes
- **Install Favorites Menu?** Yes, extended version
- **Install Book Menu?** Yes
- **Install Lockpicking Menu?** Yes
- **What's your monitor aspect ratio?** 16x9 (normal)
- **Install Player Stats (Perks) Menu replacer?** Yes, Extended UI
- **Install Levelup Menu Replacer?** Yes
- **Install Sleep-Wait Menu replacer?** Yes
- **Install Messageboxes replacer?** Yes
- **Install Tutorials Menu replacer?** Yes
- **Install Training Menu replacer?** Yes
- **Install Tab Menu replacer?** Yes
- **Install Loading Menu replacer?** Yes
- **Install Main Menu frames replacer?** Yes, cleaned version
- **Install Main Menu background replacer?** No
- **Install Main Menu background replacer?** No
- **Replace the cursor?** No
- **Replace the main font?** Yes
- **Console Improvements:** 60 FPS More Informative Console
- **Button Arts:** Install Button Arts Replacer (RECOMMENDED)
- **Loading Spinner Removal:** No

#### Customisation

- Double-click the mod in Mod Organizer 2 and switch to the **Text Files** tab.
- Select the `interface\deardiaary\config.txt` right at the top.

There are many settings to change. Below are my recommendations but you don't have to copy all of them. Change what you like.

- **35** `sMCMButtonName = $MOD CONFIG` - looks better if it's shorter
- **42** `bInstantQuit = true` - few people quit to the main menu anyway
- **51** `bLockCheatMode = true` - if you really hate the minigame
- **58** `fCheatTimer = 15` - if you enabled the option above but want to try without the UI first (feel free to adjust)
- **94** `bNoPlayerMarker = false` - if you want to remove the player marker from the map
- **139** `bHideBookUI = true` - to hide UI elements when reading
- **147** `bHideLockUI = true` - to hide UI elements when picking locks
- **154** `iMaxSleepWait = 240` - to wait for 10 days for cell resets (useful for mod testing)

When you're done, simply close the window and click **Yes** when asked to save.

##### [Wood and Paper - SkyUI - Dear Diary Skin](https://www.nexusmods.com/skyrimspecialedition/mods/44174?tab=files)

#### Download Instructions

- **Main Files:** Wood and Paper - A Dear Diary Skin

> This mod is optional. You can skip it if you prefer the default Dear Diary skin!

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `interface\deardiary\startmenu\`

> I prefer the vanilla main menu, plus it's easier this way to access to CC (just have to disable ReCleaned Menu).

##### [Paper UI Sounds](https://www.nexusmods.com/skyrimspecialedition/mods/38944?tab=files)

#### Download Instructions

- **Main Files:** Paper UI Sounds
- **Optional Files:** Red X custom destination marker >> `merge with the main file`

#### FOMOD Instructions

- **ESPFE:** ESPFE
- **Blade menu sounds:** Paper rustle
- **Menu button sounds:** Scribbly sounds
- **Confirm and cancel sounds:** Papery sounds
- **Mouseover sound:** Pen tap (recommended)
- **Map marker sounds:** Pencily map marker rollover sounds
- **Journal Sounds:** Shamplo's journal sounds
- **Quest Messages:** More varied quest updates
- **Quest Activation:** Scribbly quest activate sounds
- **Objective Update:** Scrupply objective updates
- **New Game sound:** None
- **Discovery sound:** ~~Writing sounds~~
- **Sneak attack sound:** None
- **Level up and skill increase sounds:** Page turning, blown by wind (recommended)
- **Level up music:** ~~Silent replacement~~

## Heads-Up-Display

##### [QuickLoot](https://www.nexusmods.com/skyrimspecialedition/mods/21085?tab=files)

#### Download Instructions

- **Main File:** QuickLootRE

> This mod is optional since most people either love it or hate it.

##### [Paper HUD](https://www.nexusmods.com/skyrimspecialedition/mods/34513?tab=files)

#### Download Instructions

- **Main File:** Paper HUD V4

#### FOMOD Instructions

- **Which do you use?** SkyHUD
- **Style:** *choose what you like*
- **MoreHUD Compatibility:** Yes
- **QuickLoot Retexture:** *depends on whether you installed QuickLoot*
- **WheelMenu:** None
- **Frostfall:** ~~Yes~~
- **Wearable Lanterns:** ~~Yes~~

## Loading Screens

##### [TESG Loadscreen Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/5794?tab=files)

#### Download Instructions

- **Main Files:** TESG Loadscreen Replacer v1.0

#### FOMOD Instructions

- **Loading Screen Options:** Fullscreen option

##### [Oblivion-like Loading Menus](https://www.nexusmods.com/skyrimspecialedition/mods/38708?tab=files)

#### Download Instructions

- **Main File:** Oblivion-like Loading Menu 16x9

#### FOMOD Instructions

- **Menu Style:** Paper
- **Custom Load Screens:** No
- **Choose mods you have installed:** ~~TES Legends - Loading Screens~~
- **Choose one:** TES General Loadscreen Replacer

## Paper World Map

This section is **optional** because it comes with a few **downsides**. First up, there are two paper world map mods out there but the one available on the mod page of our main world map overhaul (A Quality World Map) only affects Skyrim while Solstheim will have the regular top-down 3D map.

The alternative by Warburg includes a Solstheim map by another mod author. Unfortunately the paper textures and tone of the two maps match neither each other nor the Dear Diary paper. Ambient occlusion from ENB causes visual bugs on the Skyrim map and you will also have to regenerate DynDOLOD and Occlusion to fix some conflicts.

### Incompatible Mods

If you do decide to accept those downsides and install Warburg's Paper World Map, you need to disable a few more mods:

- **INTERFACE:** A Quality World Map
- **INTERFACE:** Dynamic Snow For Map (Type 1)
- **INTERFACE:** Dawnguard Map Markers
- **LIGHTING:** Luminosity - A Quality Worldmap Compatibility Patch

### Dear Diary Tweak

- Double-click the mod in Mod Organizer 2 and switch to the **Text Files** tab.
- Select the `interface\deardiaary\config.txt` right at the top.
- In Line **80**, change the value for `fMapMarkerAlpha =` to **90**.
- Close the window and click **Yes** when asked to save.

##### [Paper World Map](https://www.nexusmods.com/skyrimspecialedition/mods/10836?tab=files)

#### Download Instructions

- **Main Files:** Paper World Map SSE

#### FOMOD Instructions

- **Skyrim:** *choose one*
- **Solstheim (Dragonborn DLC):** Texture 2
- **Marker Style:** None

##### [Flat Map Markers](https://www.nexusmods.com/skyrimspecialedition/mods/22122?tab=files)

#### Download Instructions

- **Main Files:** Flat Map Markers SSE

##### [Warburg's Paper World Map - Flat Mesh](https://www.nexusmods.com/skyrimspecialedition/mods/23114?tab=files)

#### Download Instructions

- **Main Files:** Flat Map Mesh with JSON

## Final Steps

Thankfully interface mods are rather tame so there are no major additional steps to complete.

### Load Order

- Extended UI for Skyrim Uncapper Adamant Arena.esp
- Dawnguard Map Markers.esp >> `will be disabled if you chose to install Paper World Map`
- **TESGLoadingScreens.esp**
- **TESG LoadScreens Patch.esp**
- **Paper UI Sounds.esp**
- **Paper World Map.esp** >> `only if you chose to install Paper World Map`
- HD Lods SSE.esp
- ...
- Conflict Resolution Patch.esp
- **Paper World Map Unofficial Fix - Vanilla.esp** >> `only if you chose to install Paper World Map`
- Facegen Output.esp
- Facegen Output0.esp

> Remember that you will have to re-adjust the load order after applying an update to the base setup.

### LOD and Occlusion

If you installed the Paper World Map mods, you will now have to regenerate **DynDOLOD** and **Occlusion**. Re-doing TexGen is not necessary.

### Mod Configuration

No changes from the instructions for the base setup except for that you HAVE to "Load user settings" in the MCM for **A Matter of Time** to properly apply the preset for Paper HUD. Until you do that, your HUD will not look as intended.

![Apply AMOT Preset](/Pictures/skyrim-se/mod-configuration/load-amot-preset.jpg)

## Changelog

### Release 1.0

- Initial release.