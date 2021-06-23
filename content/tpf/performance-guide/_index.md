---
title: "Performance Guide"
weight: 7
type: docs
description: >
  How to increase performance.
---

## Expectations

The Phoenix Flavour is already optimised to run well, meaning most modern machines should be able to consistently hold a high framerate. In the 4.6 update, the focus has shifted slightly so that the base setup is no longer quite as light as it used to be. For that reason, I have written this guide on how to improve your framerate.

It must be said upfront that a "high, stable framerate" in modded Skyrim means steady 60FPS. Those among you who prefer 100FPS+ will likely be disappointed as this is not easy to achieve without very strong hardware. It is not recommended as going about 72-75FPS will, despite SSE Display Tweaks, lead to some physics wonkiness (even if it won't break your game).

This guide exists for those struggling to achieve consistent 60 FPS.

**You do not have to follow all steps:** For example, if you really love 3D tree LOD and highly detailed distant terrain, you can hold on to your High + 3D Tree LOD DynDOLOD output. Instead, you can compromise with your ENB or grass overhaul choice and regenerate your INI files with the recommended performance settings.

> **Wabbajack Users:** You do not have to follow this guide. Your installation of TPF includes a Performance profile.

### Why do I have low performance?

There may be various reasons which include:

- **Playing at a high resolution (1440p or above):** Any of the options will help.
- **Having a low amount of VRAM (4GB or less):** Regenerate DynDOLOD on Medium with 2D tree LOD.
- **AMD CPU and/or GPU:** Replace Rudy ENB with Serio's ENB (ENBSeries is optimised for Intel/NVIDIA).
- **Older hardware in general:** Any of the options will help.

## Regenerating INI Files

One reason why TPF always used to be very performance-friendly was because we ran BethINI (the INI configuration tool) with the Medium preset. This has since changed (High is the default now) so the first thing we can do is revert to those more conservative settings. It should be noted that the visual degradation is not hugely noticeable, the difference in settings will mostly apply to distant objects. However, it should help you regain some frames.

- Make sure **Mod Organizer 2** is closed.
- Navigate to your Documents folder: `C:\Users\Your User Name\Skyrim Special Edition`.
- Copy the **Skyrim.ini** and **SkyrimPrefs.ini** inside (these are the default INIs).
- Navigate to your Profiles folder: `\Mod Organizer 2\profiles\The Phoenix Flavour\`.
- Paste the default INIs and overwrite the existing set in the folder.

> It is possible to tweak the BethINI configured INIs you already had. I just always preferred to re-do it from scratch.

### Re-running BethINI

- Navigate to `\Your Modding Folder\Tools\BethINI\` and double-click **BethINI.exe**.
- In the **Setup** tab, make sure the tool still points to your MO2 installation and TPF profile.
- In the **Basic** tab, make sure the **Resolution** matches your monitor's resolution.
- In the **Basic** tab, check **Recommended Tweaks** and click **Medium** (under Presets).
- In the **Basic** tab, uncheck **VSync** and **Lock Frame Rate**.
- In the **Interface** tab, uncheck **Mod Manager Menu** and optionally adjust your mouse sensitivity.
- In the **Detail** tab, check **Reflect Objects** under Water.
- In the **Detail** tab, set **Godrays** to **None** (this will give you a decent performance boost).
- In the **Detail** tab, increase **Particles** to **7500**.
- In the **Detail** tab, uncheck **Lens Flare** and **Anamorphic Lens Flare**.
- In the **Detail** tab, increase **Shadow Resolution** to **2048** and **Exterior Draw Distance** to **6000**.
- In the **Detail** tab, check **Tree Shadows** and uncheck **Ambient Occlusion**.
- In the **View Distance** tab, increase **Grass Fade** to **10000**.
- In the **Visuals** tab, lower **Contrast** to **-0.1800**.
- In the **Visuals** tab, increase **Grass Density** to **50**.
- In the **Visuals** tab, increase **Grass Diversity** to **15**.
- In the **Custom** tab, select **Section: Display**, then **Setting: bEnableLandFace**, change the value to **0**, and click **Save**.

Return to the **Basic** tab and click **Save and Exit**.

Re-open Mod Organizer 2.

## Grass Overhaul

A major reason for the performance loss from TPF 4.5 onwards was the removal of Cathedral Landscapes. Its grass module, while not looking ideal in some places, is incredibly performant, completely unrivaled in that aspect. Thus, I recommend replacing Veydosebrom with Cathedral Landscapes grass if you struggle with a low framerate.

The good news is that you can keep Cathedral 3D Pine Grass which was made by the same author as Cathedral Landscapes, JonnyWang, and is also impressively performance-friendly.

However, you need to **disable Veydosebrom** in your mod order.

##### [Cathedral Landscapes](https://www.nexusmods.com/skyrimspecialedition/mods/21954?tab=files)

#### Download Instructions

- **Main Files:** Landscapes - Cathedral Concept

#### FOMOD Instructions

- **Select Install:** Grass Only

#### Additional Instructions

- Delete the following file(s) and / or folder(s):
  - `Cathedral Landscapes.ini`

> All necessary grass-related INI tweaks are already covered in the BethINI instructions.

##### [Cathedral Landscapes - Swamp Grass Alternative](https://www.nexusmods.com/skyrimspecialedition/mods/44067?tab=files)

#### Download Instructions

- **Main Files:** Cathedral Landscapes - Snow as Marsh Grass Addon

### Mod and Load Order

- Place both new mods **above** Cathedral 3D Pine Grass in the mod order.
- Place the two new plugins **above** Cathedral 3D Pine Grass.esp in the load order.

> This way, Cathedral 3D Pine Grass will overwrite Cathedral Landscapes and replace its pine grass.

![Cath Grass Load Order](/Pictures/tpf/performance-guide/cath-grass-load-order.png)

## DynDOLOD

Another reason for performance loss is running DynDOLOD with the High profile and 3D tree LOD. The latter is especially heavy on VRAM so regenerating DynDOLOD with the Medium profile and 2D tree LOD is highly recommended if you have 4GB of VRAM or less.

Regenerating TexGen should not be necessary. You could, in theory, to lower the resolution of the LOD textures, but I do believe only regenerating DynDOLOD will yield a sizeable enough performance increase.

- Delete your current **DynDOLOD Output** and **SSELODGen - Occlusion Data**.
- Navigate to `\Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\Cache\`.
- Delete everything inside.

### Performance Profile

- Download the [**STEP DynDOLOD Performance Profile**](https://stepmodifications.org/wiki/images/c/c7/DynDOLOD_SSE_Performance.ini) (once again, thanks to STEP for allowing me to use their configurations!).
- Save the **DynDOLOD_SSE_Optimal.ini** to `\Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\Presets\`.

### Regenerating DynDOLOD

- Run **DynDOLOD** through Mod Organizer 2.
- Click **Load Preset** (one of the buttons on the bottom left).
- The **DynDOLOD Presets** folder should be opened automatically, double-click the **DynDOLOD_SSE_Optimal.ini**.
- In the **Options** section at the bottom, check **Generate Tree LOD** (this will toggle off the **Ultra** setting).

If you have *very* low-end specs (Skyrim SE minimum requirements or below), select the **Low** preset. This will largely remove DynDOLOD's performance impact. Otherwise, the loaded preset will be using the **Medium** mesh rules.

- Click **OK** to start generating LOD.

As usual, step away from your PC while DynDOLOD is being regenerated.

### DynDOLOD Output

- Once DynDOLOD is done, click **Save & Exit**.
- Navigate to `\Your Modding Folder\Tools\DynDOLOD\`.
- Cut (CTRL+X) the **DynDOLOD_output** folder and paste it (CTRL+V) to `\Mod Organizer 2\mods\`.
- Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your load order.
- Place it last below the **PATCHER OUTPUT** separator and activate it.
- Move **DynDOLOD.esm** below your other ESMs at the top of your load order.
- Leave **DynDOLOD.esp** at the very bottom as the last plugin.
- Make sure both plugins are activated.

### Occlusion

After regenerating DynDOLOD, the Occlusion.esp must also be regenerated.

- Run **SSELODGen** through Mod Organizer 2.
- In the worldspaces window, check **Tamriel "Skyrim"** and **DLC2SolstheimWorld "Solstheim"**.
- Uncheck all options except for **Occlusion**.
- The settings should still be correct (**Quality** to set to **3** and **Height** set to **100**).
- Click **Generate** and wait for the process to complete.

> Remember to step away from your PC while Occlusion is being generated. During the process your CPU will likely be maxed out and you risk blue screens if you try to keep doing something on the side.

### Occlusion Output

- Once SSELODGen returns **LOD generation complete**, you can close the window.
- Right-click the ***Overwrite*** folder in Mod Organizer 2 and select **Create mod**.
- Enter **SSELODGen - Occlusion Data** as the name and click **OK**.
- Activate the mod in the mod order.
- Make sure **Occlusion.esp** is at the bottom of your load order and active.

## ENBSeries

A major factor in performance loss is ENBSeries. While not as FPS-hungry as it used to be ENB presets will drop your performance and Rudy ENB, the TPF default, is not exactly lightweight.

You have several options here:

- You can install the Rudy ENB - Better Performance INI.
- You can swap to a more lightweight ENB preset (I recommend Serio's).
- You can remove ENBSeries altogether.

### Option 1: Rudy ENB Performance INI

If you like Rudy ENB and would prefer to stick with the preset, you can soften its performance impact by using the pre-packaged INI with appropriate tweaks:

- Navigate to `\Your Modding Folder\ARCHIVE\MO2 Downloads\` and find the **Rudy ENB** archive.
- Open the archive and navigate to `Rudy for SSE 4.01a1 CW\ADDONS\! Better Performance ini\`.
- Extract the **enbseries.ini** inside to `\Your Modding Folder\temp\`.
- Open **ENB Man** and select the **Skyrim SE** profile.
- Make sure the **Rudy ENB** preset is selected and click the red button at the bottom to uninstall it.
- Drop the **enbseries.ini** into the files window and overwrite the existing one.
- Click the green checkmark at the bottom to re-install the preset, now with the adjusted INI file.

### Option 2: Serio's ENB

Serio's ENB is my personal favourite ENB preset for Skyrim SE (right after Visceral ENB which is sadly very outdated). It used to be the default for TPF due to its very lightweight nature and should give you a performance improvement over the fully-featured Rudy ENB preset.

If you want to switch to Serio's ENB, uninstall Rudy ENB first:

- Open **ENB Man** and double-click the **Skyrim SE** profile.
- Click the red button at the bottom to remove all ENB-related files from your root folder.

Next we need to download Serio's ENB:

- Download [**Serio's ENB - TPF Tweaks**](https://www.nexusmods.com/skyrimspecialedition/mods/30506?tab=files) from the Nexus (Miscellaneous Files section).
- Open the download archive and double-click the **Serio's ENB - TPF Edits** folder inside.
- Extract the **enbseries** folder as well as the **enblocal.ini** and **enbseries.ini** to `\Your Modding Folder\temp\`.

Before we install the files through ENB Man, there is one edit that will improve the distant view with Serio's ENB:

- Open the **enbseries.ini** in Notepad++.
- Scroll down to **Line 1122** in the `[Water]` section.
- Change `DisableDistantReflection=` to `true`.
- Press **CTRL + S** to save your changes and close the window.

Now to install Serio's ENB:

- Go back into **ENB Man**.
- Click the arrow next to the Profiles drop-down and select **Blank Preset**.
- Enter **Serio's ENB for Cathedral Weathers** as the preset's name and click the green checkmark to confirm.
- Drag and drop the preset files from your temp folder into ENB Man.
- Click the red button twice when asked whether to import palettes.
- Make sure the latest version of ENBSeries is select under **Binaries** and that the box above it is checked.
- Click the green checkmark at the bottom to install the new preset.
 
### Option 3: Removing ENBSeries

I do not recommend removing ENB altogether *unless* you either:

- dislike ENB regardless of preset, *or*
- you have very low-end specs (Skyrim SE minimum requirements or below).

If the latter applies to you, you are likely happy about every single frame you can regain. To remove ENBSeries (binaries and preset):

- Open **ENB Man** and double-click the **Skyrim SE** profile.
- Click the red button at the bottom to remove all ENB-related files from your root folder.

Deleting ENB altogether will mean that none of the ENB particle light meshes from the guide will work. Nor will you have ambient occlusion. However, you can re-enable Skyrim's native ambient occlusion which is less performance-intense than ENBSeries ambient occlusion (nevermind a full preset).

To enable Skyrim's native ambient occlusion:

- In Mod Organizer 2, open the **INI Editor** (Tools >> Tool Plugins >> INI Editor).
- Switch to the **SkyrimPrefs.ini** tab.
- Scroll down to the `[Display]` section and set `bSAOEnable=` to `1`.
- Click the **Save** button at the bottom and close the window.

## Resolution Scale

SSE Display Tweaks contains the option to downscale from your current resolution: For instance, you can play at 1440p but downscale by 0.9 to gain better performance while still having more detail than setting the game to 1080p.

Very high resolutions (4K) will always have a *substantial* performance impact and scaling down is recommended, especially if you don't have the latest hardware.

Otherwise, using the resolution scale feature is only recommended if you truly struggle to achieve a playable framerate.

### Adjusting the resolution scale

- Double-click **SSE Display Tweaks** in your mod order (below the **ESSENTIAL MODS** separator).
- Switch to the **INI Files** tab and select the **SSEDisplayTweaks.ini**.
- Scroll to **Line 60** (the exact line may vary if SSE Display Tweaks updated recently) to the Resolution Scale settings.
- Uncomment the `Resolution=1920x1080` line (remove the # sign) and set the resolution to the one you play at.
- Uncomment the `ResolutionScale=0.75` line (remove the # sign) and increase the value to `0.85`.
- Press **CTRL + S** to save your changes and close the window.

> Setting the resolution scale to a value below 0.85 will look very blurry ingame and is not recommended. You can also try 0.9 or 0.95 for slightly less performance gain and better visuals.

![Resolution Scale](/Pictures/tpf/performance-guide/resolution-scale.png)