---
title: "Step 2: Essential Mods"
weight: 2
type: docs
description: >
  Basic mods and fixes.
---

##### [SSE Engine Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/17230?tab=files)

#### Download Instructions

- **Main Files:** (Part 1) SSE Engine Fixes for 1.5.39 - 1.5.97

#### Preloader

SSE Engine Fixes requires the SKSE64 Preloader by meh and sheson. Download the **(Part 2) Engine Fixes - skse64 Preloader and TBB Lib** main file manually from the mod page.

Open the archive and extract the following files into your **Stock Game** folder:

- **d3dx9_42.dll**
- **tbb.dll**
- **tbbmalloc.dll**

Click **Yes** when asked to overwrite.

##### [SSE Display Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/34705?tab=files)

#### Download Instructions

- **Main Files:** SSE Display Tweaks

##### SSE Display Tweaks - Custom INI

SSE Display Tweaks supports a custom INI file in which settings from the main configuration file can be selectively overwritten. This way, you will not have to redo your changes every time the mod updates.

- Open your `\Mod Organizer 2\mods\` directory and create a new folder called **SSE Display Tweaks - Custom INI** inside.
- Create a new folder called **SKSE** inside the **SSE Display Tweaks - Custom INI** folder.
- Create a new folder called **Plugins** inside the **SKSE** folder.

The resulting file path should be: `\Mod Organizer 2\mods\SSE Display Tweaks - Custom INI\SKSE\Plugins\`.

- Inside the **Plugins** folder, right-click and select **New** >> **Text Document**.
- Rename the new file to **SSEDisplayTweaks_Custom.ini** (make sure to change the file extension).
- Open the new INI file in your preferred editor and add the following lines to it:

```
[Render]
Fullscreen=false
Borderless=true
FramerateLimit=60
```

*This will force Borderless Fullscreen regardless of your INI settings so that (on Windows 10 systems) the DXGI flip model feature works, improving performance. The framerate will be capped at 60FPS which is still ideal for Skyrim although increasing or removing the cap will no longer break the game.*

- Save your changes and close the editor.
- Back in Mod Organizer 2, press F5 to refresh the interface.
- The new mod will now show up below the main SSE Display Tweaks. Activate it.

##### [Unofficial High Definition Audio Project (UHDAP)](https://www.nexusmods.com/skyrimspecialedition/mods/18115?tab=files)

#### Download Instructions

Click "Manual Download" for all files:

- **Main Files:** Music - HQ 
- **Main Files:** Voices EN - Part 1
- **Main Files:** Voices EN - Part 2

> With large files, there's always a risk that MO2 won't download them properly and they may get corrupted.

#### Installation Instructions

- Wait for all three archives to be downloaded.
- Move the files to your downloads folder: `\Your Modding Folder\ARCHIVE\MO2 Downloads\`.
- Mod Organizer 2 may freeze briefly as it processes the files.
- Once it unfreezes, you will find them in the **Downloads** tab (right pane).
- Right-click each of the three archives (one at a time) and select **Query Info**.
- After all data has been retrieved from the Nexus, install the archives as usual by double-clicking them.
- Don't change their names and simply select **Merge** for the second and third file to place all in the same mod folder.

##### [Unofficial Skyrim Special Edition Patch (USSEP)](https://www.nexusmods.com/skyrimspecialedition/mods/266?tab=files&file_id=209150)

#### Download Instructions

- **Main Files:** Unofficial Skyrim Special Edition Patch

> The link leads to directly to USSEP 4.2.5b which is the last version for pre-AE SSE. Unfortunately, Arthmoor insists on removing all old files from his mod pages even when they are still needed by most users.

#### Additional Instructions

Delete the following file(s) and/or folder(s):

- `Unofficial Skyrim Special Edition Patch.modgroups`

##### [Disable USSEP Book](https://www.nexusmods.com/skyrimspecialedition/mods/26092?tab=files)

#### Download Instructions

- **Main Files:** Disable USSEP Book

##### [Skyrim Landscape and Water Fixes](https://www.nexusmods.com/skyrimspecialedition/mods/26138?tab=files)

#### Download Instructions

- **Main Files:** Skyrim Landscape and Water Fixes - FOMOD

#### FOMOD Instructions

- **Patches:**
  - ~~ELFX~~
  - ~~Relighting Skyrim~~
  - ~~CACO~~
  - Landscape Fixes for Grass Mods
- **Walkway Wall FIX:**
  - Walkway Wall FIX SMIM
- **Optional:**
  - Missing Lights Fix
  - ~~ELFX - Exteriors Fixed Mesh~~

##### [Weapons, Armor, Clothing and Clutter Fixes (WACCF)](https://www.nexusmods.com/skyrimspecialedition/mods/18994?tab=files)

#### Download Instructions

- **Main File** - Weapons Armor Clothing and Clutter Fixes

#### Additional Instructions

Delete the following file(s) and/or folder(s):

- `WACCF_BashedPatchLvlListFix.esp`

##### [WACCF Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/43466?tab=files)

#### Download Instructions

- **Main Files:** WACCF Tweaks

##### [WACCF Greatsword Weapon Speed Tweaks](https://www.nexusmods.com/skyrimspecialedition/mods/50250?tab=files)

#### Download Instructions

- **Miscellaneous Files:** WACCF Greatsword Weapon Speed Tweaks

##### [SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/12604?tab=files)

#### Download Instructions

- **Main Files:** SkyUI_5_2_SE

##### [Fix Note Icon for SkyUI](https://www.nexusmods.com/skyrimspecialedition/mods/32561/?tab=files)

#### Download Instructions

- **Main Files:** FixNotesForSkyUI SKSE64 2.0.17 and 2.0.19

##### [SkyUI Ghost Item Bug Fix](https://www.nexusmods.com/skyrimspecialedition/mods/49106?tab=files)

#### Download Instructions

- **Main Files:** SkyUI - Ghost Item Bug Fix

##### [More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/19250?tab=files)

#### Download Instructions

* **Main Files:** More Informative Console 0.43

##### [Dear Diary - Better More Informative Console](https://www.nexusmods.com/skyrimspecialedition/mods/46437?tab=files)

#### Download Instructions

- **Main Files:** Dear Diary - Better More Informative Console

---

#### Continue with the [Assorted Plugins](/tpf/mod-installation-basics/step-3/) page.