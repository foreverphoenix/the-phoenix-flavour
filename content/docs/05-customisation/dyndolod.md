---
title: "DynDOLOD"
weight: 11
type: docs
description: >
  Instructions for re-generating DynDOLOD.
---

## Preparations

#### Old Output

If you installed anything from **Tree Tweaks** or **Arthmoor's Towns**, you MUST re-generate LOD with DynDOLOD - either with 3D or regular tree LOD.

- Re-running TexGen is **not required** so you can keep your **TexGen_Output** active.
- Uncheck **DynDOLOD ({Preset})** in your mod order.

#### Empty Cache

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\cache`.
- Delete everything inside (CTRL+A and DEL).

#### Tree LOD Type

- Navigate to `Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\`.
- Open **DynDOLOD_SSE.ini** in Notepad++.
- Find the following line: `TreeLOD=<value>`.
  - Set to `1` for regular tree LOD.
  - Set to `0` for 3D tree LOD.

## Running DynDOLOD

* Launch **DynDOLOD** through Mod Organizer 2.
* A window will come up, click **Advanced**.
* You can see a list of all worldspaces at the top. Right-click inside and **Select all**.
* Select a preset:
  * **Low** if you already struggle with performance.
  * **Medium** as the default option plus regular tree LOD.
  * **High** for modern machines and 3D tree LOD.
* Under **Load rules for** check both **Candles** and **FXGlow**.
* Double-check with the picture below that everything is configured correctly, then click **OK**.

**Step away from your PC while DynDOLOD is working.**

![DynDOLOD Settings](/Pictures/finalisation/dyndolod_settings.png)

## DynDOLOD Output

* Once DynDOLOD is done, click **Save & Exit**.
* Go to `Your Modding Folder\Tools\DynDOLOD`.
* Cut (CTRL+X) the **DynDOLOD_output** folder and paste it (CTRL+V) to `Mod Organizer 2\mods`.
* Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your load order.
* Rename the file and add the preset you selected, eg: `DynDOLOD - Customisation (Medium)`.
* Place it last below the (deactivated) `DynDOLOD ({Preset})` and activate it.
* Move **DynDOLOD.esm** below your other ESMs at the top of your load order.
* Leave **DynDOLOD.esp** at the very bottom as the last plugin.