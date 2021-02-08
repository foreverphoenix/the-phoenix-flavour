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

#### Engine Fixes TOML

- Double-click **SSE Engine Fixes** in your mod order.
- In the **Textfiles** tab, select the **EngineFixes.toml** config file.
- Edit the following line:
  - `SleepWaitTime = true`
- Save your changes (CTRL + S) and close the editor.

##### [.NET Script Framework (NSF)](https://www.nexusmods.com/skyrimspecialedition/mods/21294?tab=files)

#### Download Instructions

- **Main Files:** NetScriptFramework SkyrimSE v14

##### [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

#### Download Instructions

- **Main Files:** SSE Display Tweaks

#### INI Tweaks

- Double-click the mod in your mod order and switch to the **INI Files** tab.
- Select the **SSEDisplayTweaks.ini** and edit the following:
  - `BorderlessUpscale=true` if you play at a lower resolution than your monitor's default (Skyrim @1080p on a 1440p monitor).
  - `EnableVSync=false` if you want uncapped FPS. Will cause screentearing on monitors without G-Sync or FreeSync.
- Hit CTRL+S to save and close the window.

##### [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250?tab=files)

#### Download Instructions

* **Main Files:** More Informative Console for SKSE 2.17-2.19

##### [Autorun](https://www.nexusmods.com/skyrimspecialedition/mods/45451?tab=files)

#### Download Instructions

- **Main Files:** Autorun

#### Additional Instructions

The first set of console commands we want run automatically can be added now (more mod-related ones will come later). [Multiple Floors Sandboxing](https://www.nexusmods.com/skyrimspecialedition/mods/4524) merely changes two existing game settings which can simply edited through the console, thus removing the need for an additional plugin.

- Double-click **Autorun Console Commands** in Mod Organizer 2.
- Switch to the **Textfiles** tab and select the **Autorun.txt** file.
- Add the following two lines in the text field:

```
SetGS fSandboxCylinderTop 576
SetGS fSandboxCylinderBottom -576
```

- Close the window and click **Yes** when asked to save.

![ACC Add MFS](/Pictures/skyrim-se/mod-installation/acc-add-mfs.png)

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

![Skyrim Particle Patch download link](/Pictures/skyrim-se/mod-installation/skyrim-particle-patch-download.png)

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `textures\effects\gradients\gradwhitewater.dds`
  - `Particle Patch for ENB SSE.esp`

> The plugin is not needed. Its functionality was replaced by ENB Helper. The texture can cause water spray to look much darker than intended with Realistic Water Two.

##### [Static Mesh Improvement Mod (SMIM)](https://www.nexusmods.com/skyrimspecialedition/mods/659?tab=files)

#### Download Instructions

- **Main Files:** SMIM SE 2-08

#### FOMOD Instructions

- **Main Installer Choice:** Skyrim 2016 Special Edition: Everything

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  * `meshes\architecture\farmhouse\walkway\walkwaycwall01.nif`
  * `meshes\architecture\solitude\doors\sgatedoor.nif`

> The first mesh will be replaced either by the fixed version contained in Skyrim Landscape and Water Fixes or by Real Walls 3D. Deleting the second mesh will allow you to use a different retexture for the Solitude city gate.