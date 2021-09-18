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

- Download the **(Part 2) Engine Fixes - skse64 Preloader and TBB Lib** main file manually. 
- Open the downloaded archive.
- Extract the following files into your **root** folder:
  * **d3dx9_42.dll**
  * **tbb.dll**
  * **tbbmalloc.dll**
- Click **Yes** when asked to overwrite.

> **Root folder:** Steam\steamapps\common\Skyrim Special Edition\

#### INI Tweaks

- Double-click **SSE Engine Fixes** in your mod order.
- Switch to the **Text Files** tab and select the **EngineFixes.toml**.
- In **Line 13**, set **Regular Quicksaves** to **true**.
- Close the window and click **Yes** when asked to save.

> This is done so that quicksaves have proper names and stop overwriting each other.

##### [.NET Script Framework](https://www.nexusmods.com/skyrimspecialedition/mods/21294?tab=files)

#### Download Instructions

- **Main Files:** NetScriptFramework SkyrimSE v17

##### [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

#### Download Instructions

- **Main Files:** SSE Display Tweaks

#### INI Tweaks

- Double-click the mod in your mod order and switch to the **INI Files** tab.
- Select the **SSEDisplayTweaks.ini** and edit the following:
  - **207** `FramerateLimit=60` if you want to cap the framerate (see note)
  - **601** `LoadScreenFilter=true` to enable the load screen filter
  - **603** `LoadScreenBlock=DynDOLOD.esm,Lanterns Of Skyrim II.esm` to block load screens added by those plugins
- Hit CTRL+S to save and close the window.

> You can leave the framerate uncapped if you prefer, it will no longer break the game.That being said, general physics weirdness (like flying objects) still happens more frequently at higher framerates. Additionally, achieving a framerate consistently above 60, especially with ENB, *especially* on resolutions of 1440p and upwards, requires very solid hardware. I personally think 60 is the sweet spot for everyone.

##### [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250?tab=files)

#### Download Instructions

* **Main Files:** More Informative Console 0.43

##### [Dear Diary - Better More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/46437?tab=files)

#### Download Instructions

- **Main Files:** Dear Diary - Better More Informative Console

##### [Autorun](https://www.nexusmods.com/skyrimspecialedition/mods/45451?tab=files)

#### Download Instructions

- **Main Files:** Autorun

#### Additional Instructions

Game settings can be implemented in two ways: They can be added to a plugin or toggled in the console using the `SetGS` command. When using the console, the command would have to be entered every time the game is restarted. Fortunately we have Autorun which will execute any console commands configured in its text file automatically when loading a save.

- Double-click **Autorun** in Mod Organizer 2.
- Switch to the **Text Files** tab and select the **Autorun.txt** file.
- Copy and paste the following lines into the text field:

```
cl off
SetGS fPhysicsDamage1Mass 9999999
SetGS fSandboxCylinderTop 576
SetGS fSandboxCylinderBottom -576
SetGS fCombatAimProjectileRandomOffset 70
```

- Close the window and click **Yes** when asked to save.

> The added commands will expand the radius in which NPCs can move when they sandbox and lower NPC's accuracy with ranged attacks, as well as disable character lighting and physics damage sustained when colliding with clutter objects.

![ACC Add MFS](/Pictures/tpf/mod-installation/autorun-commands.png)

##### [Unofficial High Definition Audio Project (UHDAP)](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files)

#### Download Instructions

Click "Manual Download" for all files:

- **Main Files:** Music - HQ 
- **Main Files:** Voices EN - Part 1
- **Main Files:** Voices EN - Part 2

> With large files, there's always a risk that MO2 won't download them properly and they may get corrupted.

#### Installation Instructions

- Wait for all three archives to be downloaded.
- Move the files to your downloads folder: `Your Modding Folder\ARCHIVE\MO2 Downloads`.
- Mod Organizer 2 may freeze briefly as it processes the files.
- Once it unfreezes, you will find them in the **Downloads** tab (right pane).
- Right-click each of the three archives (one at a time) and select **Query Info**.
- After all data has been retrieved from the Nexus, install the archives as usual by double-clicking them.

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

##### [WACCF Greatsword Weapon Speed Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/50250?tab=files)

#### Download Instructions

- **Miscellaneous Files:** WACCF Greatsword Weapon Speed Tweaks

##### [Skyrim Particle Patch](http://enbseries.enbdev.com/forum/viewtopic.php?t=1499)

#### Download Instructions

- Find the **SPECIAL EDITION** section in the forum post linked above.
- Click the **LATEST VERSION (GOOGLE DRIVE)** link (see picture).
- Download the archive from Google Drive and move it manually to `Your Modding Folder\ARCHIVE\MO2 Downloads`.
- Go to the **Downloads** tab and double-click the mod to install it as usual.
- I recommend renaming it simply to **Skyrim Particle Patch** after the installation.

![Skyrim Particle Patch download link](/Pictures/tpf/mod-installation/skyrim-particle-patch-download.png)

#### Additional Instructions

- Delete the following file(s) and/or folder(s):
  - `meshes\clutter\deadanimals\`
  - `textures\effects\gradients\gradwhitewater.dds`
  - `Particle Patch for ENB SSE.esp`

> The plugin is not needed. Its functionality was replaced by ENB Helper. The texture can cause water spray to look much darker than intended with Realistic Water Two.