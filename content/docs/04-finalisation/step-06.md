---
title: "DynDOLOD"
weight: 6
type: docs
description: >
  Improving distant terrain and tree LOD with TexGen and DynDOLOD.
---

## 6.1 DynDOLOD and Performance

Contrary to popular belief, DynDOLOD is not inherently performance-intense. With the **Low** or **Medium** presets and regular tree LOD, you will hardly notice any performance impact, even on weaker machines, while still drastically improving distant terrain.

More hardware-taxing is however what is typically referred to as "ultra tree LOD" or simply 3D tree LOD. This is a DynDOLOD feature which disables regular tree LOD, the two dimensional, flat "cut-outs". Instead, object LOD is generated for distant trees, utilising 3D meshes which drastically improve the visual quality of tree LOD to the point where you can barely tell fully-rendered trees and distant trees apart anymore.

3D tree LOD is not recommended for people with less than 4GB VRAM. There is a potential performance impact but it is usually negligible on most modern machines (and very much worth the visual improvement).

**You will have the option to generate either regular or 3D tree LOD.** Choose accordingly. Later on, you can always re-run DynDOLOD to generate the other type of tree LOD, depending on how well the game runs for you.

## 6.2 DynDOLOD Setup

### 6.2.1 File Download

* Download the [**DynDOLOD**](https://www.nexusmods.com/skyrimspecialedition/mods/32382) main file manually.
* Navigate to `Your Modding Folder\Tools` and create a new **DynDOLOD** folder.
* Open the downloaded **DynDOLOD** archive and move all files into your new directory.

### 6.2.2 TexGen Executable

* Switch back to Mod Organizer 2 and open the **Executables** window (Tools > Executables or CTRL + E).
* Click the blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`and double-click **TexGenx64.exe**.
* Under **Arguments**, add the following:
  * `-sse`

### 6.2.3 DynDOLOD Executable

* Once again, click the blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`and double-click **DynDOLODx64.exe**.
* Under **Arguments**, add the following:
  * -sse
* Click **OK** to save and close the **Executables** window.

![Texgen DynDOLOD Executables](/Pictures/finalisation/texgen_dyndolod_executables.png)

## 6.3 TexGen Configuration

TexGen is a component of DynDOLOD, used to generate textures based on your mod setup.

* Launch **TexGen** through Mod Organizer 2.
* Set **LOD Texture Size** to `512` if you have 4GB of VRAM or more.
* Hit **Start**.

> The generation will take a while (about 10 minutes for me) and I recommend you step away from your PC in the meantime.

![TexGen Settings](/Pictures/finalisation/texgen_settings.png)

## 6.4 TexGen Output

* Once TexGen has finished, click **Save and Exit**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`.
* Cut (CTRL + X) the **TexGen_Output** folder and paste (CTRL+V) it to `Mod Organizer 2\mods`.
* Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your mod order.
* Place it right above the **WEATHER** separator and activate it.

![TexGen Output Mod Order](/Pictures/finalisation/texgen_mod_order.png)

## 6.5 Tweak for 3D Tree LOD

> Only follow these instructions if you are planning to generate 3D tree LOD.

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD`.
- Double-click **DynDOLOD_SSE.ini**.
- Edit the following line to disable traditional tree LOD:
  * `TreeLOD=0`
- Save and close **DynDOLOD_SSE.ini**.

## 6.6 DynDOLOD - LOD Generation

* Launch **DynDOLOD** through Mod Organizer 2.
* A window will come up, click **Advanced**.
* You can see a list of all worldspaces at the top. Right-click inside and **Select all**.
* Select one preset:
  * **Low** if you already struggle with performance.
  * **Medium** as the default option plus regular tree LOD.
  * **High** for modern machines and 3D tree LOD.
* Under **Load rules for** check both **Candles** and **FXGlow**.
* Double-check with the picture below that everything is configured correctly, then click **OK**.

**Step away from your PC while DynDOLOD is working.**

![DynDOLOD Settings](/Pictures/finalisation/dyndolod_settings.png)

## 6.7 DynDOLOD Output

* Once DynDOLOD is done, click **Save & Exit**.
* Go to `Your Modding Folder\Tools\DynDOLOD`.
* Cut (CTRL+X) the **DynDOLOD_output** folder and paste it (CTRL+V) to `Mod Organizer 2\mods`.
* Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your load order.
* Rename the file and add the preset you selected, eg: `DynDOLOD (Medium)`.
* Place it last below the **PATCHER OUTPUT** separator and activate it.
* Move **DynDOLOD.esm** below your other ESMs at the top of your load order.
* Leave **DynDOLOD.esp** at the very bottom as the last plugin.