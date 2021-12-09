---
title: "Step 5: Interface"
weight: 5
type: docs
description: >
  Additional mods to improve the user interface and HUD.
---

##### [Remove Quicksave Button from SkyUI Systems Menu](https://www.nexusmods.com/skyrimspecialedition/mods/28334?tab=files)

#### Download Instructions

- **Main Files:** Remove QuickSave Button

#### FOMOD Instructions

- **Options:** 1b - Save-Load-etc, MCM renamed

> While quicksaving is not actually broken as the mod page claims ([more about that here](https://www.reddit.com/r/skyrimmods/comments/7bkazq/whats_the_real_deal_with_quicksavesautosaves/)), I personally like the re-ordering and decluttering of the Pause menu. The mod includes the [Flashing Savegame Fix for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/20406).

##### [Wider MCM Menu for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/22825?tab=files)

#### Download Instructions

- **Main Files:** Opt. 1 - Wider MCM Menu for SkyUI

##### [Favorite Things - Extended Favorites Menu for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/27177?tab=files)

#### Download Instructions

- **Main Files:** Opt. 1 - Modified Vanilla Favorites

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

- **Optional Files:** moreHUD SE Light Master- Pre AE

#### Additional Instructions

- Double-click **moreHUD** in your mod order.
- Switch to the **Filetree** tab and rename the plugin:
  - AHZmoreHUD.**esl** >> AHZmoreHUD.**esp** 

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

##### [Oxygen Meter](https://www.nexusmods.com/skyrimspecialedition/mods/57452?tab=files)

#### Download Instructions

- **Main Files:** Oxygen Meter - SSE

##### [Horse Stamina HUD](https://www.nexusmods.com/skyrimspecialedition/mods/47076?tab=files)

#### Download Instructions

- **Main Files:** Horse Stamina HUD

##### [Convenient Reading UI](https://www.nexusmods.com/skyrimspecialedition/mods/50202?tab=files)

#### Download Instructions

- **Main Files:** Convenient Reading

#### Additional Instructions

- Double-click **Convenient Reading** in your mod order.
- Switch to the **INI Files** tab and select the **Convenient Reading.ini**.
- In **Line 12** set **sBookStealTextColor=** to **0xFF0000**.
- Hit **CTRL + S** to save your changes and close the window.

> This will make the Steal button in the book UI red so it's easier to see.

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

##### [Shouts in the Dragon Tongue (SIDT)](https://www.nexusmods.com/skyrimspecialedition/mods/5515?tab=files)

#### Download Instructions

- **Main Files:** SIDT - Words Only

#### Additional Instructions

- ESL-ify **SIDT - Special Edition.esp** with SSEEdit ([instructions](/tpf/guide-resources/basic-instructions/#esl-ifying-plugins)).

##### [Smaller Vanilla Cursor](https://www.nexusmods.com/skyrimspecialedition/mods/20617?tab=files)

#### Download Instructions

- **Main Files:** Smaller Vanilla Cursors

#### FOMOD Instructions

* **Step 1:** Right

> Of course you can select the "Left" option if you are left-handed.

##### [Sovngarde - A Nordic Font](https://www.nexusmods.com/skyrimspecialedition/mods/386?tab=files)

#### Download Instructions

- **Main Files:** Sovngarde - A Nordic Font Light V8.9

#### Additional Instructions

- Double-click **Sovngarde - A Nordic Font** in your mod order.
- Switch to the **Text Files** tab and select the **fontconfig.txt** file.
- Create a new line below `fontlib "Interface\fonts_drukaatieburti.swf"`.
- Paste `fontlib "Interface\fonts_consolas.swf"` into the new **Line 6**.
- In **Line 7**, change `"SovngardeConsole"` to `"Consolas"`.
- Press **CTRL + S** to save your changes and close the window.

> This way you can use Sovngarde's font for most of the game with Dear Diary's Consolas font for the console.

![Sovngarde Consolas](/Pictures/tpf-x/installation/sovngarde-consolas.png)

##### [A Quality World Map (AQWM)](https://www.nexusmods.com/skyrimspecialedition/mods/5804?tab=files)

#### Download Instructions

- **Main Files:** 8.4 A Quality World Map - Classic with All Roads

#### Additional Instructions, Part 1

Unpack **icepenguinworldmapclassic - textures.bsa** through Mod Organizer 2.

Delete the following file(s) and/or folder(s):

- `icepenguinworldmapclassic - textures.bsa`
- `icepenguinworldmapclassic.esp`
- `icepenguinworldmapclassic.ini`

> The BSA is unpacked and deleted in order to allow us to more reliably be able to find conflicting files in generated terrain LOD later on. The plugin's weather edits and its associated INI file are replaced by Weather of World.

##### [Dynamic Snow for Map](https://www.nexusmods.com/skyrim/mods/29877?tab=files)

#### Download Instructions

- **Main Files:** Type 1

##### [Weather of World](https://www.nexusmods.com/skyrimspecialedition/mods/58782?tab=files)

#### Download Instructions

- **Main Files:** Weather of World

##### [CoMAP - Common Marker Addon Project](https://www.nexusmods.com/skyrimspecialedition/mods/56123?tab=files)

#### Download Instructions

- **Main Files:** CoMAP

#### FOMOD Instructions

- **CoMAP Core Pack:** CoMAP 1.5.97 (Pre-AE)
- **Configs:** CoMAP Config Pack
- **Obscured Undiscovered Options:** Obscured Undiscovered HUD Markers - Diamond
- **Author's Cut Options:** Hearthfire Homes are Settlements
- **Khajiit Caravan Markers:** Hidden Until Discovered
- **Other Addons:**
  - Jorrvaskr Map Marker
  - ~~Wyrmstooth Travel Marker Tweaks~~

#### Additional Instructions

- Double-click **CoMAP - Common Marker Addon Project** in your mod order.
- Switch to the **INI Files** tab and select the **MapMarkerFramework.ini** file.
- In **Line 13**, change `"fMarkerScale="` to `0.75`.
- Press **CTRL + S** to save your changes and close the window.

> This will reduce the size of all map markers by 25%.

##### [Menu and Load Smoke Removed for ENB](https://www.nexusmods.com/skyrimspecialedition/mods/51986?tab=files)

#### Download Instructions

- **Main Files:** Menu and Load Smoke Removed for ENB

##### [Main Menu Design Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/30810?tab=files)

#### Download Instructions

- **Main Files:** Main Menu Design Replacer (clean)

##### [Yet Another Main Menu Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/53798?tab=files)

#### Download Instructions

- **Main Files:** Yet Another Main Menu Replacer

##### [KenMOD - Time On Loading Screen](https://github.com/KenneyNL/Skyrim-Mods/blob/main/Time%20On%20Loading%20Screen/Files/Interface/loadingmenu.swf)

*This mod is now available only on Github. Because its installation is a little more involved, you can skip it if you like. All it does is add a tiny 24h clock to loading screens: [Preview here](https://raw.githubusercontent.com/KenneyNL/Skyrim-Mods/main/Time%20On%20Loading%20Screen/PreviewB.png).*

- Download the [**loadingmenu.swf**](https://github.com/KenneyNL/Skyrim-Mods/blob/main/Time%20On%20Loading%20Screen/Files/Interface/loadingmenu.swf) file from KenneyNL's Github (click the **Download** button on the top right).

![Download KenMOD Time](/Pictures/tpf/mod-installation/kenmod-time-download.png)

- Move the downloaded file to your **temp** folder.
- Create a new folder called **Interface** and move the **loadingmenu.swf** file inside.
- Right-click the **Interface** folder and select **Add to archive**.
- Rename the archive to **KenMOD - Time On Loading Screen**.
- Move the new mod to `\Your Modding Folder\ARCHIVE\MO2 Downloads\`.
- In MO2, press F5 to refresh and the mod will appear in the **Downloads** tab.
- From there, you can install it as usual.

#### Configuration File

- Right-click **KenMOD - Time On Loading Screen** in your mod order and select **Open in Explorer**.
- Open the **interface** folder. Right-click inside and select **New** >> **Text Document**.
- Name the file **loadingmenu_settings.txt** and open it.
- Paste the following inside:

```
// Clock settings (1 = true, 0 = false)
&showAnalog=1&
&showTimeString=1&
&twelveHourClock=0&

// Misc settings
&showLevelProgressPercentage=0&

// Static background (hides 3D model and hints, for potential spoilers)
&showStaticBackground=0&

// Turn on/off modules
&showHints=1&
&showLevelProgress=1&
&showTime=1&
```

- Save your changes and close the text file.

> If you prefer a 12h clock, feel free to set the fourth line to `&twelveHourClock=1&`.

---

#### Continue with the [Mesh Improvements](/tpf/mod-installation-2/step-1/) page.