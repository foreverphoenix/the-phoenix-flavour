---
title: "Interface"
weight: 4
type: docs
description: >
  Small edits that do not qualify as fixes.
---

## 4.1 SkyUI

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/12604?tab=files)

- **Main Files:** SkyUI_5_2_SE

#### Additional Instructions

- Run SSEEdit through Mod Organizer 2.
- Click **OK** in the plugin selection window to load all plugins.
- Wait for your mods to be loaded up before you proceed.
- Right-click **SkyUI_SE.esp** in the left pane and select **Add Masters**.
- Check **Skyrim.esm** and click **OK**.
- Click **Yes, I’m sure** when the warning comes up.
- Close SSEEdit and click **OK** to save your changes.

> The plugin had no masters assigned to it which causes errors. Every plugin needs to have at least Skyrim.esm as a master.

## 4.2 Fix Note Icon for SkyUI (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/32561/?tab=files)

- **Main Files:** FixNotesForSkyUI SKSE64 2.0.17

## 4.3 Remove Quicksave Button from SkyUI Systems Menu (optional)

While quicksaving is not actually broken as the mod page claims ([more about that here](https://www.reddit.com/r/skyrimmods/comments/7bkazq/whats_the_real_deal_with_quicksavesautosaves/)), I personally like the re-ordering and decluttering of the Pause menu. It will look as follows:

- MCM
- Save
- Load
- Settings
- Controls
- Quit

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/28334?tab=files)

- **Optional Files:** Remove QuickSave and Help Buttons (1)

> While optional, I highly recommend installing this mod as it also contains the [Flashing Savegame Fix](https://www.nexusmods.com/skyrimspecialedition/mods/20406) for SkyUI which solves a very annoying issue.

## 4.4 Wider MCM Menu for SkyUI (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/22825?tab=files)

- **Main Files:** Opt. 1 - Wider MCM Menu for SkyUI

> You can download any one of the main files. Check the GIFs and choose your preferred version.

## 4.5 Favorite Things - Extended Favorites Menu for SkyUI (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/27177?tab=files)

- **Main Files:** Opt. 1 - Modified Vanilla Favorites

> You can download any one of the main files. Check the pictures and choose your preferred version.

## 4.6 Stay At The System Page (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/19832?tab=files)

- **Main Files:** Stay At System Page

## 4.7 RaceMenu

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/19080?tab=files)

- **Main Files:** RaceMenu Special Edition v0-4-12

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `RaceMenuPlugin.esp`

## 4.8 Immersive HUD - iHUD

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/12440?tab=files)

- **Main Files:** Immersive HUD - iHUD

## 4.9 SkyHUD

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/463?tab=files)

- **Main Files:** SkyHUD v090B v4
- **Update Files:** Patch - SkyHUD v090B ==merge with the main file==

#### FOMOD Instructions

* **Install:** Loose Files
* **Preset:** Vanilla Small
* **Optional:** Install iHUD compatibility patch

#### Additional Instructions

**This is optional.**

* Double-click **SkyHUD** in your mod order.
* In the **Text Files** tab, select the **skyhud.txt**.
* Edit the following lines:
  * `bAltArrow=1`
  * `bAltCompass=1`
  * `bDotCrosshair=1`
* Close the window and confirm when asked to save.

> This will change the compass to a slimmer one and improve the arrow display. The crosshair will be turned into a simple dot.

## 4.10 Undiscovered Means Unknown (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/9762?tab=files)

- **Main Files:** Undiscovered Means Unknown - Compass and Map Markers

#### FOMOD Instructions

* **Main:**
  * Only the Compass
* **Do you wish for the player's location to be marked on the map?**
  * Yes
* **Have you installed SkyUI?**
  * Yes
* **Have you installed a HUD-altering mod?**
  * SkyHUD
* **Have you installed the mod Customizeable UI Replacer?**
  * No
* **Font choice:**
  * Custom font
* **Which colored map marker mod have you installed?**
  * Default - Skyrim SE
* **Do you wish for enemies to be visible in the compass?**
  * Yes *(this can easily be disabled in SkyHUD in the future)*
* **Which icon do you wish to use for undiscovered locations?**
  * Nothing (an Invisible Icon)

## 4.11 moreHUD (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/12688?tab=files) 

- **Main Files:** moreHUD SE Light Master

#### Additional Instructions

- Double-click **moreHUD** in your mod order.
- Switch to the **Filetree** tab.
- Rename the following file:
  * AHZmoreHUD.**esp**

> This is faster than ESL-ifying the ESP.

## 4.12 moreHUD - Inventory Edition (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/18619?tab=files)

- **Main Files:** moreHUD Inventory Edition

#### Additional Instructions

- Double-click **moreHUD - Inventory Edition** in your mod order.
- Switch to the **Filetree** tab.
- Rename the following file:
  * AHZmoreHUDInventory.**esp**

> This is faster than ESL-ifying the ESP.

## 4.13 A Matter of Time - A Clock HUD Widget (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/12937?tab=files) 

- **Main Files:** AMatterOfTime_v3_0_0_alpha_4

## 4.14 A Matter of Time - Phoenix Preset (optional)

This is my personal preset for AMOT. It uses the slim clock widget to match the slim compass from SkyHUD and has a small 24h clock with the ingame time centered below. You can change the clock to 12h through the MCM at any time.

Even if you have the preset installed, you can configure the AMOT settings to your liking. It will only be applied if you load it through the MCM specifically.

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

- **Main Files:** A Matter of Time - Phoenix Preset

> **Mod Dependency:** Only install this mod if you installed A Matter of Time. Otherwise skip it.

![My AMOT Preset Preview](/Pictures/mod_installation/amot_preset_preview.jpg)

## 4.15 Shouts in the Dragon Tongue (SIDT) (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/5515?tab=files)

- **Main Files:** SIDT - Words Only

## 4.16 Skyrim SE Skill Interface Retexture (SSIRT) (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/1523?tab=files)

- **Main Files:** SSIRT SE v4.1

#### FOMOD Instructions

Below are my personal choices. Feel free to make your own!

- **Background:**
  - Background - Irradiant Stars - HDR Nebula
- **Perk Lines:**
  - Default
- **Perk Line Colour:**
  - Default
- **Constellations:**
  - HD Default
- **Perk Stars:**
  - Option 2
- **Dawnguard:**
  - HD Masser and Secunda and More Stars
- **Vampire Background:**
  - HDR Nebula

##  4.17 No More Laser-Printed Book (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/462?tab=files)

- **Main Files:** No More Laser-Printed Book

## 4.18 Immersive Bookreading and Lockpicking (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/4541?tab=files)

- **Main Files:** Immersive Bookreading
- **Main Files:** Immersive Lockpicking

## 4.19 JS Lockpicking UI (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/22160?tab=files)

- **Main Files:** 2k Textures

## 4.20 A Quality World Map

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/5804?tab=files)

- **Main Files:** 8.4 A Quality World Map - Classic with All Roads

#### Additional Instructions, Part 1

* Unpack **icepenguinworldmapclassic - textures.bsa** through Mod Organizer 2.
* Delete the following file(s) and/or folder(s):
  * `icepenguinworldmapclassic.esp`

> The BSA is deleted in order to allow A Quality World Map to overwrite some LOD files from Cathedral Landscapes. The plugin only contains one record which is completely overwritten by the AQWM+Luminosity lighting patch and it is no longer needed to load the BSA so it is redundant.

#### Additional Instructions, Part 2

* Double-click **A Quality World Map** in your mod order.
* Switch to the **Filetree** tab.
* Rename the following file:
  * `icepenguinworldmapclassic.ini` >> `maplightfix.ini`

> Since we just deleted the plugin, it can no longer load the INI file. By renaming it, the INI will now be loaded by the Luminosity map lighting patch (installed later on).

## 4.21 Dynamic Snow for Map (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrim/mods/29877?tab=files)

- **Main Files:** Type 1

## 4.22 Dawnguard Map Markers (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/20931?tab=files)

- **Main Files:** Dawnguard Map Markers

## 4.23 Smaller Vanilla Cursor (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/20617?tab=files)

- **Main Files:** Smaller Vanilla Cursors

#### FOMOD Instructions

* **Step 1:** Right

> If you are left-handed, feel free to select the "Left" option.

## 4.24 ReCleaned Menu (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/26680?tab=files)

- **Main Files:** ReCleanedMenus

## 4.25 Loading Screen Smoke Removed (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrimspecialedition/mods/4634?tab=files)

- **Main Files:** Loading Screen Smoke Removed v1.0

## 4.26 KenMOD - Time on Loading Screen (optional)

#### [Download Instructions](https://www.nexusmods.com/skyrim/mods/98?tab=files)

- **Main Files:** Time on loading v5
