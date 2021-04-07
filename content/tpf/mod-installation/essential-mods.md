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

##### [Dear Diary - Better More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/46437?tab=files)

#### Download Instructions

- **Main Files:** Dear Diary - Better More Informative Console

##### [Autorun](https://www.nexusmods.com/skyrimspecialedition/mods/45451?tab=files)

#### Download Instructions

- **Main Files:** Autorun

#### Additional Instructions

Game settings can be implemented in two ways: They can be added to a plugin or toggled in the console using the `SetGS` command. When using the console, the command would have to be entered every time the game is restarted. Fortunately we have Autorun which will execute any console commands configured in its text file automatically when loading a save.

- Double-click **Autorun Console Commands** in Mod Organizer 2.
- Switch to the **Text Files** tab and select the **Autorun.txt** file.
- Copy and paste the following lines into the text field:

```
cl off
SetGS fPhysicsDamage1Mass 9999999
SetGS fSandboxCylinderTop 576
SetGS fSandboxCylinderBottom -576
```

- Close the window and click **Yes** when asked to save.

> The added commands will expand the radius in which NPCs can move when they sandbox as well as disable character lighting and physics damage sustained when colliding with clutter objects.

![ACC Add MFS](/Pictures/tpf/mod-installation/autorun-commands.png)

##### [Unofficial High Definition Audio Project (UHDAP)](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files)

#### Download Instructions

- **Main Files:** Music - HQ
- **Main Files:** Voices EN - Part 1
- **Main Files:** Voices EN - Part 2

*If your internet connection is slow, there's a risk that MO2 won't properly download these files. In that case it is recommended to click "Manual Download", then move the files to your MO2 downloads directory. Refresh MO2 and the archives will appear in the Downloads tab. Right-click them and select "Query Info", then install them as usual.*

##### [Project Clarity AIO - Skyrim Textures Redone](https://www.nexusmods.com/skyrimspecialedition/mods/45306?tab=files)

#### Download Instructions

- **Main Files:** Project Clarity AIO Half Res BSA
- **Update Files:** Hotfix To v2.1 Half Res >> `merge with the main file`

*Same as above - very large main file should be downloaded and moved manually.*

#### Additional Instructions

- Run **SSEEdit** through Mod Organizer 2.
- In the plugin selection window click **OK**.
- Wait until SSEEdit returns `Background Loader: finished`.
- Select the first of the Project Clarity plugins, **Half Res Packed.esp**.
- On the right under **Record flags**, right-click and select **Edit**.
- Click **Yes I'm absolutely sure** when the warning window appears.
- Check the box for **ESM** at the top of the list and click **OK**.

The plugin is now ESM-ified and will load with all other ESMs. This allows us to place it above the USSEP in the load order which means that the assets packed in its BSAs will be overwritten by assets packed in the BSA loaded with the USSEP.

- Repeat the process for all other **Half Res Packed---.esp** plugins.
- Once you have ESM-ified all plugins, close the window.
- Make sure all Project Clarity plugins appear in the list to be saved and are checked.
- Click **OK** to close SSEEdit and save your changes.

![ESMify Project Clarity](/Pictures/tpf/mod-installation/esmify-project-clarity.png)

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

##### [Hooded Skeleton Corpse Fix for WACCF](https://www.nexusmods.com/skyrimspecialedition/mods/47985?tab=files)

#### Download Instructions

- **Main Files:** Hooded Skeleton Corpse Fix for WACCF

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

##### [No Grass In Objects](https://www.nexusmods.com/skyrimspecialedition/mods/42161?tab=files)

#### Download Instructions

- **Main Files:** Grass Control v6

> The Grass Generation MO2 plugin will be installed later on before we precache grass.

#### INI Tweaks

- Double-click **No Grass In Objects** in your mod order.
- Switch to the **Text Files** tab and select the **GrassControl.config.txt** file.
- In **Line 99**, change **UseGrassCache** to **True**.
- In **Line 111**, change **ExtendGrassDistance** to **True**.
- In **Line 134**, change **EnsureMaxGrassTypesPerTextureSetting** to **15**.
- In **Line 149**, change **OverwriteGrassDistance** to **12000**.
- In **Line 163**, change **OverwriteGrassFadeRange** to **8000**.
- In **Line 187**, change **OnlyLoadFromCache** to **True**.
- Close the window and click **Yes** when prompted to save.