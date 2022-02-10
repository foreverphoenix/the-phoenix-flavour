---
title: "UI Adjustments"
weight: 1
type: docs
description: >
  Support for ultrawide monitors and more interface mods, including NORDIC UI.
---

This customisation page features support for a number of UI mods that can be added to the default TPF setup. Please pay close attention to the instructions as some of these mods replace existing ones or are mutually exclusive. Each section can be skipped.

---

## Ultrawide Support

All interface mods are made by default for 16:9 aspect ratio monitors (1920x1080, 2560x1440, 3840x2160) and need patches in order to work with 21:9 monitors (2560x1080, 3440x1440). Not all mods have patches available so you are limited in your mod choices, but for most base TPF mods there are patches available on a single mod page.

### Adjust the resolution

Depending on your choices in the main guide, you may still need to adjust the game resolution:

- Open the **INI Editor** in Mod Organizer 2 (see screenshot below).
- In the **SkyrimPrefs.ini** tab, scroll to the **[Display]** section.
- Adjust the `iSize H` and `iSize W` lines accordingly.
- Click the **Save** button at the bottom before closing the window.

![Change Resolution](/Pictures/tpf/customisation/change-resolution.png)

### [Complete Widescreen Fix for Vanilla and SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/1778?tab=files)

#### Download Instructions

- **Main Files:** Complete Widescreen Fix for SkyUI 5.2 SE Alpha - 2560x1080
- **Optional Files:** Better Dialogue Control Widescreen Fix
- **Optional Files:** Better MessageBox Control Widescreen Fix
- **Optional Files:** Creation Club - Widescreen Fix
- **Optional Files:** Opt. 1 - Wider MCM Menu for SkyUI - Widescreen Fix
- **Optional Files:** SkyHud - High Resolution Widescreen Fix

### [Ultrawide Forget Spell Patch](https://www.nexusmods.com/skyrimspecialedition/mods/54854?tab=files)

#### Download Instructions

- **Main Files:** Ultrawide Forget Spell Patch

---

## HUD Clock Widget

Can be used on an **ultrawide** monitor but you may have to adjust my preset.

![AMOT Preview](/Pictures/tpf/customisation/amot-preset-preview.jpg)

### [A Matter of Time - A Clock HUD Widget](https://www.nexusmods.com/skyrimspecialedition/mods/12937?tab=files)

#### Download Instructions

- **Main Files:** AMatterOfTime_v3_0_0_alpha_4

### [A Matter of Time - Settings Loader](https://www.nexusmods.com/skyrimspecialedition/mods/55365?tab=files)

#### Download Instructions

- **Main Files:** A Matter Of Time - Settings Loader

### [A Matter of Time - TPF Preset](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** A Matter of Time - TPF Preset

---

## Oblivion-like Loading Screens

Fully replaces the loading screen UI as well as all loading screens. Do not use if you have an **ultrawide** monitor, there is a patch but it currently does not function correctly (images are not centered correctly in the loading screens).

![Loading Screens Comparison](/Pictures/tpf/customisation/loading-screens-comparison.png)

### [TESG Loadscreen Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/5794?tab=files)

#### Download Instructions

- **Main Files:** TESG Loadscreen Replacer v1.0

#### FOMOD Instructions

- **Loading Screen Options:** Fullscreen option

### [Oblivion-Like Loading Menu](https://www.nexusmods.com/skyrimspecialedition/mods/38708?tab=files)

#### Download Instructions

- **Main Files:** Oblivion-like Loading Menu 16x9

#### FOMOD Instructions

- **Menu Style:** *choose either option* >> `see the comparison image above`
- **Custom Load Screens:** No
- **Choose mods you have installed:** ~~TES Legends - Loading Screens~~
- **Choose one:** TES General Loadscreen Replacer

---

## NORDIC UI

[NORDIC UI](https://www.nexusmods.com/skyrimspecialedition/mods/49881) is a full reskin of the SkyUI interface that I personally like a great deal. It is quite a departure from the vanilla look and thus not everyone will like it. However, if you do, here's how to install it.

As for **ultrawide** support, there is a [patch](https://www.nexusmods.com/skyrimspecialedition/mods/53909) for the main NORDIC UI mod. However, NORDIC UI - Miscellaneous Patches does not include ultrawide support and neither do the other files related to NORDIC UI. If you are on an ultrawide monitor, please skip NORDIC).

### Mods to disable

Please fully disable the following mods in MO2 which are replaced by, included with or incompatible with NORDIC UI:

- **ASSORTED PLUGINS:** Forget Spell
- **INTERFACE:** Remove Quicksave Button from SkyUI Systems Menu
- **INTERFACE:** Wider MCM Menu for SkyUI
- **INTERFACE:** Favorite Things - Extended Favorites Menu for SkyUI
- **INTERFACE:** SkyHUD - TPF Preset
- **INTERFACE:** SkyHUD - Alternate White Dot Crosshair
- **INTERFACE:** Convenient Reading UI
- **INTERFACE:** Smaller Vanilla Cursor
- **INTERFACE:** Main Menu Design Replacer
- **INTERFACE:** Yet Another Main Menu Replacer

> While not technically incompatible, I would also not use **A Matter of Time** with **NORDIC UI** as the styles do not match.

### [NORDIC UI - Interface Overhaul](https://www.nexusmods.com/skyrimspecialedition/mods/49881?tab=files)

#### Download Instructions

- **Main Files:** NORDIC UI (Final Design)

#### FOMOD

- **Main:**
  - HUD (SkyHUD)
  - Boxes
  - Race Menu (Vanilla)
  - Cursor
  - Dialogue Menu
  - Favorite Menu
  - Icons
  - Pause Menu (Journal)
  - ~~Map Markers~~
  - Skill Menu
  - Skill Menu 3D Visuals
  - Start Menu
  - Start Menu 3D Background
  - Game Menus
  - UI Sounds
  - ~~QuickLoot Patch~~
  - ~~TDM Patch~~
  - SkyHUD Preset
- **Loading Screen:** Default / None >> `see highlighted note below`

> For the loading screens it depends on whether or not you installed Oblivion-like Loading Screens. If you did, select "None" in the NORDIC UI FOMOD, others "Default".

### **NORDIC UI - True Directional Movement Patch**

#### Installation Instructions

We are installing this patch separately in order to be able to place it below TDM and overwrite.

- Create a new, empty mod in Mod Organizer 2 called **NORDIC UI - True Directional Movement Patch**.
- Find the **NORDIC UI** archive in your downloads pane, right-click it and select **Open in Explorer**.
- In the archive, navigate to `Nordic UI - Interface Overhaul\TDM\Data\`.
- Extract the **interface** folder inside into your new mod folder.

### [NORDIC UI - Miscellaneous Patches](https://www.nexusmods.com/skyrimspecialedition/mods/54102?tab=files)

#### Download Instructions

- **Main Files:** NORDIC UI - Miscellaneous Patches

#### FOMOD Instructions

- **moreHUD Inventory:** Vanilla
- **Stat Screen Colored Icons:** 2.4 style Icons
- **Even Better MessageBox Controls:** Install
- **Extended Hotkey System:** ~~Install~~
- **MCM:** Wider MCM
- **Remove QuickSave from System Menu:** ~~Install~~
- **Loading Screen:** ~~Install~~
- **Tween Menu:** Install
- **Spacing:** SkyUI Item Card Fixes spacing

### [Hand to Hand - An Adamant Addon - NORDIC UI Patch](https://www.nexusmods.com/skyrimspecialedition/mods/59790?tab=files)

#### Download Instructions

- **Miscellaneous Files:** Hand to Hand - Nordic UI Consistency Patch

### [Dot Crosshair for NORDIC UI](https://www.nexusmods.com/skyrimspecialedition/mods/58059?tab=files)

> Install this if you don't like NORDIC UI's default crosshair. Both this mod and NORDIC UI - Persistent Meters edit hudmenu.swf which means they are mutually exclusive.

#### Download Instructions

- **Main Files:** Dot crosshair for NORDIC UI

### [NORDIC UI - Persistent Meters](https://www.nexusmods.com/skyrimspecialedition/mods/55162?tab=files)

> Install this if you don't want the Magicka and Stamina meters to fade away. Both this mod and Dot Crosshair for NORDIC UI edit hudmenu.swf which means they are mutually exclusive.

#### Download Instructions

- **Main Files:** NORDIC UI - Persistent Meters

---

## QuickLoot

QuickLoot adds a popup window when hovering over lootable containers (chests, barrels, etc as well as dead bodies). Install only one of the reskins, they are mutually exclusive.

![QuickLoot Preview](/Pictures/tpf/customisation/quick-loot-preview.jpg)

### [QuickLoot RE](https://www.nexusmods.com/skyrimspecialedition/mods/21085?tab=files)

#### Download Instructions

Download **QuickLootRE 2.8.6** from the Old Files section.

- **Old Files:** QuickLootRE

### [No Lockpick Activate (SKSE) - Updated](https://www.nexusmods.com/skyrimspecialedition/mods/26790?tab=files)

#### Download Instructions

- **Main Files:** No Lockpick Activate

> This mod is strongly recommended in conjunction with QuickLoot. Without it, you would still be forced into the regular looting menu when unlocking containers.

### [QuickLootRE Texture Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/39045?tab=files)

#### Download Instructions

- **Main Files:** QuickLootRE Texture Replacer

> Skip this and install the next mod instead if you also have NORDIC UI.

#### FOMOD Instructions

- **Options:** Dialogue Style

### **NORDIC UI - Quick Loot Patch**

#### Installation Instructions

Install this patch for Quick Loot if you also installed NORDIC UI:

- Create a new, empty mod in Mod Organizer 2 called **NORDIC UI - Quick Loot Patch**.
- Find the **NORDIC UI** archive in your downloads pane, right-click it and select **Open in Explorer**.
- In the archive, navigate to `Nordic UI - Interface Overhaul\QuickLoot\Data\`.
- Extract the **interface** folder inside into your new mod folder.

---

## Loading Screen Clock

> Please note that you cannot combine this mod with **NORDIC UI** or **Oblivion-like Loading Screens**.

![Loading Clock Preview](/Pictures/tpf/customisation/loading-clock-preview.jpg)

### [KenMOD - Time On Loading Screen](https://github.com/KenneyNL/Skyrim-Mods/blob/main/Time%20On%20Loading%20Screen/Files/Interface/loadingmenu.swf)

#### Download Instructions

- Download the [**loadingmenu.swf**](https://github.com/KenneyNL/Skyrim-Mods/blob/main/Time%20On%20Loading%20Screen/Files/Interface/loadingmenu.swf) file from KenneyNL's Github (click the **Download** button on the top right).

![Download KenMOD Time](/Pictures/tpf/mod-installation/kenmod-time-download.png)

#### Installation Instructions

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

## Font Replacer

> Right-click >> Open in new tab to see the image in full size.

![Font Replacer Comparison](/Pictures/tpf/customisation/font-replacer-comparison.png)

### [Roboto Font Replacer](https://www.nexusmods.com/skyrimspecialedition/mods/1779?tab=files)

#### Download Instructions

- **Main Files:** Roboto Main Font Replacer

#### Additional Instructions

- Double-click **Roboto Font Replacer** in your mod order.
- Switch to the **Text Files** tab and select the **fontconfig.txt** file.
- Create a new line below `fontlib "Interface\fonts_en6.swf"`.
- Paste `fontlib "Interface\fonts_consolas.swf"` into the new **Line 4**.
- In **Line 5**, change `"Arial"` to `"Consolas"`.
- Close the window and click **Yes** when asked to save.

![Roboto Console Font](/Pictures/tpf/customisation/roboto-consolas.png)

### [Main Font Replacement - Fertigo Pro](https://www.nexusmods.com/skyrimspecialedition/mods/14356?tab=files)

#### Download Instructions

- **Main Files:** Fertigo Pro Font SSE

#### Additional Instructions

- Double-click **Main Font Replacement - Fertigo Pro** in your mod order.
- Switch to the **Text Files** tab and select the **fontconfig.txt** file.
- Create a new line below `fontlib "Interface\fonts_en2.swf"`.
- Paste `fontlib "Interface\fonts_consolas.swf"` into the new **Line 4**.
- In **Line 5**, change `"Arial"` to `"Consolas"`.
- Close the window and click **Yes** when asked to save.

![Fertigo Consolas](/Pictures/tpf/customisation/fertigo-consolas.png)

---

## Cursor Replacer

Only install one cursor replacer at a time.

If you have NORDIC UI, but don't want its cursor, make sure either **Smaller Vanilla Cursor** or the **ESO Style Cursor** are placed *below* NORDIC UI in the mod order.

![Cursor Replacer Comparison](/Pictures/tpf/customisation/cursor-replacer-comparison.png)

### [ESO Style Cursor](https://www.nexusmods.com/skyrimspecialedition/mods/39670?tab=files)

#### Download Instructions

- **Main Files:** ESO Style Cursor

#### FOMOD Instructions

- **Choose Type:** *choose one option* >> `the comparison above shows White, Medium`