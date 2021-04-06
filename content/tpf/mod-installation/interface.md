---
title: "Interface"
weight: 5
type: docs
description: >
  Improvements for menus and the HUD.
---

##### [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604?tab=files)

#### Download Instructions

- **Main Files:** SkyUI_5_2_SE

##### [Fix Note Icon for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/32561/?tab=files)

#### Download Instructions

- **Main Files:** FixNotesForSkyUI SKSE64 2.0.17 and 2.0.19

##### [Remove Quicksave Button from SkyUI Systems Menu](https://www.nexusmods.com/skyrimspecialedition/mods/28334?tab=files)

#### Download Instructions

- **Main Files:** Remove QuickSave Button

#### FOMOD Instructions

- **Options:** 2b - Save-MCM-etc, MCM renamed

> While quicksaving is not actually broken as the mod page claims ([more about that here](https://www.reddit.com/r/skyrimmods/comments/7bkazq/whats_the_real_deal_with_quicksavesautosaves/)), I personally like the re-ordering and decluttering of the Pause menu. The mod includes the [Flashing Savegame Fix for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/20406).

##### [Wider MCM Menu for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/22825?tab=files)

#### Download Instructions

- **Main Files:** Opt. 1 - Wider MCM Menu for SkyUI

##### [Favorite Things - Extended Favorites Menu for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/27177?tab=files)

#### Download Instructions

- **Main Files:** Opt. 1 - Modified Vanilla Favorites

##### [Stay At The System Page](https://www.nexusmods.com/skyrimspecialedition/mods/19832?tab=files)

#### Download Instructions

- **Main Files:** Stay At System Page

##### [RaceMenu](https://www.nexusmods.com/skyrimspecialedition/mods/19080?tab=files)

#### Download Instructions

- **Main Files:** RaceMenu Special Edition v0-4-16

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `RaceMenuPlugin.esp`

##### [Immersive HUD - iHUD](https://www.nexusmods.com/skyrimspecialedition/mods/12440?tab=files)

#### Download Instructions

- **Main Files:** Immersive HUD - iHUD

##### [SkyHUD](https://www.nexusmods.com/skyrimspecialedition/mods/463?tab=files)

#### Download Instructions

- **Main Files:** SkyHUD v090B v4
- **Update Files:** Patch - SkyHUD v090B >> `merge with the main file`

#### FOMOD Instructions

* **Install:** Loose Files
* **Preset:** None
* **Optional:**
  * Install iHUD compatibility patch
  * ~~Extra presets~~

##### [SkyHUD - TPF Preset](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** SkyHUD - TPF Preset

##### [SkyHUD - Alternate White Dot Crosshair](https://www.nexusmods.com/skyrimspecialedition/mods/47121?tab=files)

#### Download Instructions

- **Main Files:** white dot

##### [moreHUD](https://www.nexusmods.com/skyrimspecialedition/mods/12688?tab=files)

#### Download Instructions

- **Main Files:** moreHUD SE Light Master

#### Additional Instructions

- Double-click **moreHUD** in your mod order.
- Switch to the **Filetree** tab.
- Rename the following file:
  * AHZmoreHUD.**esp**

> This is faster than ESL-ifying the ESP version.

##### [moreHUD - TPF Preset](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** moreHUD - TPF Preset

##### [A Matter of Time - A Clock HUD Widget](https://www.nexusmods.com/skyrimspecialedition/mods/12937?tab=files)

#### Download Instructions

- **Main Files:** AMatterOfTime_v3_0_0_alpha_4

##### [A Matter of Time - Phoenix Preset](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** A Matter of Time - TPF Preset

#### About the mod

This is my personal preset for AMOT. It uses the slim clock widget to match the slim compass from SkyHUD and has a small 24h clock with the ingame time centered below. You can change the clock to 12h through the MCM at any time.

Installing the preset won't prevent you from being able to configure the AMOT settings to your liking. It will only be applied if you load it through the MCM.

![My AMOT Preset Preview](/Pictures/tpf/mod-installation/amot-preset-preview.jpg)

##### [Shouts in the Dragon Tongue (SIDT)](https://www.nexusmods.com/skyrimspecialedition/mods/5515?tab=files)

#### Download Instructions

- **Main Files:** SIDT - Words Only

##### [Skyrim SE Skill Interface Retexture (SSIRT)](https://www.nexusmods.com/skyrimspecialedition/mods/1523?tab=files)

#### Download Instructions

- **Main Files:** SSIRT SE v4.1

#### FOMOD Instructions

- **Background:** Background - Irradiant Stars - HDR Nebula
- **Perk Lines:** Default
- **Perk Line Colour:** Default
- **Constellations:** HD Default
- **Perk Stars:** Option 2
- **Dawnguard:** HD Masser and Secunda and More Stars
- **Vampire Background:** HDR Nebula

##### [No More Laser-Printed Book](https://www.nexusmods.com/skyrimspecialedition/mods/462?tab=files)

#### Download Instructions

- **Main Files:** No More Laser-Printed Book

##### [JS Lockpicking UI](https://www.nexusmods.com/skyrimspecialedition/mods/22160?tab=files)

#### Download Instructions

- **Main Files:** 2k Textures

##### [A Quality World Map (AQWM)](https://www.nexusmods.com/skyrimspecialedition/mods/5804?tab=files)

#### Download Instructions

- **Main Files:** 8.4 A Quality World Map - Classic with All Roads

#### Additional Instructions, Part 1

* Unpack **icepenguinworldmapclassic - textures.bsa** through Mod Organizer 2.
* Delete the following file(s) and/or folder(s):
  * `icepenguinworldmapclassic - textures.bsa`
  * `icepenguinworldmapclassic.esp`

> The BSA is unpacked and deleted in order to allow A Quality World Map to overwrite some LOD files from Cathedral Landscapes. The plugin only contains one record which is completely overwritten by the AQWM+Luminosity lighting patch.

#### Additional Instructions, Part 2

* Double-click **A Quality World Map** in your mod order.
* Switch to the **Filetree** tab.
* Rename the following file:
  * `icepenguinworldmapclassic.ini` >> `maplightfix.ini`

> Since we just deleted the plugin, it can no longer load the INI file. By renaming it, the INI will now be loaded by the Luminosity map lighting patch (installed later on).

##### [Dynamic Snow for Map](https://www.nexusmods.com/skyrim/mods/29877?tab=files)

#### Download Instructions

- **Main Files:** Type 1

##### [Dawnguard Map Markers](https://www.nexusmods.com/skyrimspecialedition/mods/20931?tab=files)

#### Download Instructions

- **Main Files:** Dawnguard Map Markers

##### [Smaller Vanilla Cursor](https://www.nexusmods.com/skyrimspecialedition/mods/20617?tab=files)

#### Download Instructions

- **Main Files:** Smaller Vanilla Cursors

#### FOMOD Instructions

* **Step 1:** Right

> Obviously you can select the "Left" option if you are left-handed.

##### [Roboto Font Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/1779?tab=files)

#### Download Instructions

- **Main Files:** Roboto Main Font Replacer

#### Additional Instructions

- Double-click **Roboto Font Replacer** in your mod order.
- Switch to the **Text Files** tab and select the **fontconfig.txt** file.
- Create a new line below `fontlib "Interface\fonts_en6.swf"`.
- Paste `fontlib "Interface\fonts_consolas.swf"` into the new **Line 4**.
- In **Line 5**, change `"Arial"` to `"Consolas"`.
- Close the window and click **Yes** when asked to save.

> This way we can use Roboto for dialogue, menus, etc and Dear Diary's Consolas font (packaged with Dear Diary - Better More Informative Console installed in the Essential Mods section) for the console.

![Roboto Console Font](/Pictures/tpf/mod-installation/roboto-console-font.png)

##### [ReCleaned Menu](https://www.nexusmods.com/skyrimspecialedition/mods/26680?tab=files)

#### Download Instructions

- **Main Files:** ReCleanedMenus

##### [DRELDYN's Original Main Menu Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/6992?tab=files)

#### Download Instructions

- **Main Files:** DRELDYN's Original Main Menu Overhaul

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `music`

> I prefer the original main menu track, Song of the Dragonborn.

##### [Loading Screen Smoke Removed](https://www.nexusmods.com/skyrimspecialedition/mods/4634?tab=files)

#### Download Instructions

- **Main Files:** Loading Screen Smoke Removed v1.0

##### [KenMOD - Time on Loading Screen](https://www.nexusmods.com/skyrim/mods/98?tab=files)

#### Download Instructions

- **Main Files:** Time on loading v5