---
title: "DynDOLOD"
weight: 4
type: docs
description: >
  Improving distant terrain and tree LOD with TexGen and DynDOLOD.
---

## DynDOLOD and Performance

Contrary to popular belief, DynDOLOD is not inherently performance-intense. With the **Low** or **Medium** presets and regular tree LOD, you will hardly notice any performance impact, even on weaker machines, while still drastically improving distant terrain.

More hardware-taxing is however what is typically referred to as "ultra tree LOD" or simply 3D tree LOD. This is a DynDOLOD feature which disables regular tree LOD, the two dimensional, flat "cut-outs". Instead, object LOD is generated for distant trees, utilising 3D meshes which drastically improve the visual quality of tree LOD to the point where you can barely tell fully-rendered trees and distant trees apart anymore.

3D tree LOD is not recommended for people with less than 4GB VRAM. There is a potential performance impact but it is usually negligible on most modern machines (and very much worth the visual improvement).

**You will have the option to generate either regular or 3D tree LOD.** Choose accordingly. Later on, you can always re-run DynDOLOD to generate the other type of tree LOD, depending on how well the game runs for you.

## DynDOLOD Setup

* Download the [DynDOLOD](https://www.nexusmods.com/skyrimspecialedition/mods/32382) main file manually.
* Navigate to `Your Modding Folder\Tools` and create a new **DynDOLOD** folder.
* Open the downloaded **DynDOLOD** archive and move all files into your new directory.

### TexGen Executable

* Switch back to Mod Organizer 2 and open the **Executables** window (Tools > Executables or CTRL + E).
* Click the blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`and double-click **TexGenx64.exe**.
* Under **Arguments**, add the following:
  * `-sse`

### DynDOLOD Executable

* Once again, click the blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`and double-click **DynDOLODx64.exe**.
* Under **Arguments**, add the following:
  * -sse
* Click **OK** to save and close the **Executables** window.

![Texgen DynDOLOD Executables](/Pictures/skyrim-se/finalisation/texgen-dyndolod-executables.png)

## TexGen Configuration

TexGen is a component of DynDOLOD, used to generate textures based on your mod setup.

* Launch **TexGen** through Mod Organizer 2.
* Set **LOD Texture Size** to `512` if you have 4GB of VRAM or more.
* Hit **Start**.

> The generation will take a while (about 10 minutes for me) and I recommend you step away from your PC in the meantime.

![TexGen Settings](/Pictures/skyrim-se/finalisation/texgen-settings.png)

## TexGen Output

* Once TexGen has finished, click **Exit**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`.
* Cut (CTRL + X) the **TexGen_Output** folder and paste (CTRL+V) it to `Mod Organizer 2\mods`.
* Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your mod order.
* Place it below the **PATCHER OUTPUT** separator and activate it.

## Tweaks for 3D Tree LOD

> Only follow these instructions if you are planning to generate 3D tree LOD.

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD`.
- Double-click **DynDOLOD_SSE.ini**.
- Edit the following line to disable traditional tree LOD:
  * `TreeLOD=0`
- Save and close **DynDOLOD_SSE.ini**.

### Solstheim Trees

- Check **Enhanced Landscapes - Solstheim 3D Trees** in your mod order (**TREES & PLANTS** separator).

## DynDOLOD Generation

> Continue here for both 2D or 3D LOD.

* Launch **DynDOLOD** through Mod Organizer 2.
* In the DynDOLOD Help window, click **OK**.
* If you are not generating 3D tree LOD, there will be a window where you have to click **Advanced**.
* In the **Advanced** window, you can see a list of all worldspaces at the top.
* Right-click inside and **Select all**.
* Under **Load rules for** check both **Candles** and **FXGlow**.
* Select one of the presets:
  * **Low** if you already struggle with performance.
  * **Medium** as the default option plus regular tree LOD.
  * **High** for modern machines and 3D tree LOD.
* Double-check with the picture below that everything is configured correctly, then click **OK**.

**Step away from your PC while DynDOLOD is working.** This may take around 20-30 minutes.

![DynDOLOD Settings](/Pictures/skyrim-se/finalisation/dyndolod-settings.png)

## DynDOLOD Output

* Once DynDOLOD is done, click **Save & Exit**.
* Go to `Your Modding Folder\Tools\DynDOLOD`.
* Cut (CTRL+X) the **DynDOLOD_output** folder and paste it (CTRL+V) to `Mod Organizer 2\mods`.
* Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your load order.
* Place it last below the **PATCHER OUTPUT** separator and activate it.
* Move **DynDOLOD.esm** below your other ESMs at the top of your load order.
* Leave **DynDOLOD.esp** at the very bottom as the last plugin.
* Make sure both plugins are activated.

## DynDOLOD Loading Screens

As DynDOLOD was such a revolutionary mod when it came out, there's been an ongoing joke that one had to give their firstborn to the author, sheson, for using it - like in the [fairy tale](https://en.wikipedia.org/wiki/Rumpelstiltskin). Also there's a golden cow. Both memes were added to the mod as easter eggs and while the cow is optional in the FOMOD, the [three loading screens](/Pictures/skyrim-se/finalisation/dyndolod-loading-screen.png) featuring those memes are part of the generated DynDOLOD.esm.

Removing the loading screens can be done easily in SSEEdit after generating DynDOLOD. You can skip this step if they don't bother you.

- Run **SSEEdit** through Mod Organizer 2.
- Click **Yes** in the plugin selection window to load all plugins.
- Wait until SSEEdit has loaded up your plugins.
- Double-click **DynDOLOD.esm** in the left pane.
- Right-click the **Load Screen** section and click **Remove**.
- Click **Yes, I'm absolutely sure** and confirm deletion of all records.
- Close SSEEdit and click **OK** to save your changes.

![Delete DynDOLOD Load Screens](/Pictures/skyrim-se/finalisation/delete-dyndolod-loadscreens.png)