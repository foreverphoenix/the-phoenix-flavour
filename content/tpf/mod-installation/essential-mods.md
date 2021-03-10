---
title: "Essential Mods"
weight: 2
type: docs
description: >
  Basic mods and frameworks.
---

##### [Address Library for SKSE Plugins](https://www.nexusmods.com/skyrimspecialedition/mods/32444?tab=files)

#### Download Instructions

- **Main Files:** All in one

##### [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files)

#### Download Instructions

- **Main Files:** (Part 1) Engine Fixes

#### Preloader

- Download the following file manually:
  * **(Part 2) Engine Fixes - skse64 Preloader and TBB Lib**
- Open the downloaded archive.
- Extract the following files into your **root** folder:
  * **d3dx9_42.dll**
  * **tbb.dll**
  * **tbbmalloc.dll**
- Click **Yes** when asked to overwrite.

#### INI Tweaks

- Double-click **SSE Engine Fixes** in your mod order.
- Switch to the **Text Files** tab and select the **EngineFixes.toml**.
- In **Line 13**, set **Regular Quicksaves** to **true**.
- Close the window and click **Yes** when asked to save.

> This is done so that quicksaves have proper names and stop overwriting each other.

##### [.NET Script Framework (NSF)](https://www.nexusmods.com/skyrimspecialedition/mods/21294?tab=files)

#### Download Instructions

- **Main Files:** NetScriptFramework SkyrimSE v14

##### [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

#### Download Instructions

- **Main Files:** SSE Display Tweaks

#### INI Tweaks

- Double-click the mod in your mod order and switch to the **INI Files** tab.
- Select the **SSEDisplayTweaks.ini** and edit the following:
  - **79** `EnableVSync=false` if you have a G-Sync or FreeSync monitor.
  - **205** `FramerateLimit=60` if VSYNC is disabled but you want to cap the framerate.
- Hit CTRL+S to save and close the window.

##### [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250?tab=files)

#### Download Instructions

* **Main Files:** More Informative Console for SKSE 2.17-2.19

##### [Autorun](https://www.nexusmods.com/skyrimspecialedition/mods/45451?tab=files)

#### Download Instructions

- **Main Files:** Autorun

#### Additional Instructions

The first set of console commands we want run automatically can be added now (more mod-related ones will come later). [Multiple Floors Sandboxing](https://www.nexusmods.com/skyrimspecialedition/mods/4524) merely changes two existing game settings which can simply edited through the console, thus removing the need for an additional plugin.

The third command will disable a fairly ugly effect called "character lighting".

- Double-click **Autorun Console Commands** in Mod Organizer 2.
- Switch to the **Text Files** tab and select the **Autorun.txt** file.
- Add the following two lines in the text field:

```
SetGS fSandboxCylinderTop 576
SetGS fSandboxCylinderBottom -576
cl off
```

- Close the window and click **Yes** when asked to save.

![ACC Add MFS](/Pictures/tpf/mod-installation/acc-add-mfs.png)

##### [Unofficial High Definition Audio Project (UHDAP)](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files)

#### Download Instructions

- **Main Files:** Music - HQ
- **Main Files:** Voices EN - Part 1
- **Main Files:** Voices EN - Part 2

*If your internet connection is slow, there's a risk that MO2 won't properly download these files. In that case it is recommended to click "Manual Download", then move the files to your MO2 downloads directory. Refresh MO2 and the archives will appear in the Downloads tab. Right-click them and select "Query Info", then install them as usual.*

##### [Unofficial Skyrim Special Edition Patch (USSEP)](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files)

#### Download Instructions

- **Main Files:** Unofficial Skyrim Special Edition Patch

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `Unofficial Skyrim Special Edition Patch.modgroups`

##### [Disable USSEP Book](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** Disable USSEP Book

##### [Weapons, Armor, Clothing and Clutter Fixes (WACCF)](https://www.nexusmods.com/skyrimspecialedition/mods/18994?tab=files)

#### Download Instructions

- **Main File** - Weapons Armor Clothing and Clutter Fixes

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `WACCF_BashedPatchLvlListFix.esp`
  * `Weapons Armor Clothing & Clutter Fixes.modgroups`

##### [Skyrim Particle Patch](http://enbseries.enbdev.com/forum/viewtopic.php?t=1499)

#### Download Instructions

- Find the **SPECIAL EDITION** section in the forum post linked above and click the **GOOGLE DRIVE** link (see picture).
- Download the archive from Google Drive and move it manually to `Your Modding Folder\ARCHIVE\MO2 Downloads`.
- Go to the **Downloads** tab and double-click the mod to install it as usual.
- I recommend renaming it simply to **Skyrim Particle Patch** after the installation.

![Skyrim Particle Patch download link](/Pictures/tpf/mod-installation/skyrim-particle-patch-download.png)

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `textures\effects\gradients\gradwhitewater.dds`
  - `Particle Patch for ENB SSE.esp`

> The plugin is not needed. Its functionality was replaced by ENB Helper. The texture can cause water spray to look much darker than intended with Realistic Water Two.