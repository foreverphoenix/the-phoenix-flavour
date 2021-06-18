---
title: "DynDOLOD"
weight: 8
type: docs
description: >
  Improving distant terrain and tree LOD with TexGen and DynDOLOD.
---

## DynDOLOD and Performance

Contrary to popular belief, DynDOLOD is not inherently performance-intense. In fact, generating with the **Low** profile may even improve performance over vanilla in some places.

However, for TPF we are going to use the **High** preset with 3D tree LOD which is quite taxing, especially for people with 4GB of VRAM or less. Especially 3D tree LOD is a substantial improvement visually as it replaces the vanilla 2D "cut-outs" with proper models for the leaves for a seamless transition.

**If you have 4GB of VRAM or less:** Please skip this entire page and use the DynDOLOD instructions from the [Performance Guide] instead.

## DynDOLOD Setup

- Open the Nexus page for [DynDOLOD](https://www.nexusmods.com/skyrimspecialedition/mods/32382?tab=files).
- Under **Miscellaneous Files**, download the latest version of **DynDOLOD 3.00** manually.
- Navigate to `Your Modding Folder\Tools` and create a new **DynDOLOD** folder.
- Open the downloaded **DynDOLOD** archive and move all files into your new directory.

### TexGen Executable

* Switch back to Mod Organizer 2 and open the **Executables** window (Tools > Executables or CTRL + E).
* Click the blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`and double-click **TexGenx64.exe**.
* Under **Arguments**, add `-sse`.

### DynDOLOD Executable

* Once again, click the blue plus icon to add a new executable and select **Add from file**.
* Navigate to `Your Modding Folder\Tools\DynDOLOD`and double-click **DynDOLODx64.exe**.
* Under **Arguments**, add `-sse`.
* Click **OK** to save and close the **Executables** window.

![Texgen DynDOLOD Executables](/Pictures/tpf/finalisation/texgen-dyndolod-executables.png)

## TexGen

- Launch **TexGen** through Mod Organizer 2.
- Under **Trees/Grass Billboards**, check the boxes for **Tree**, **HD Tree**, and **Rendered**.
- Increase **Min Texture Size** to **256**.
- Click **Start** to begin the process.

> The generation will take a while (around 20 minutes for me) and you should step away from your PC in the meantime.

![TexGen Settings](/Pictures/tpf/finalisation/texgen-settings.png)

### TexGen Output

- Once TexGen has finished, click **Exit TexGen**.
- Navigate to `Your Modding Folder\Tools\DynDOLOD`.
- Cut (CTRL + X) the **TexGen_Output** folder and paste (CTRL+V) it to `Mod Organizer 2\mods`.
- Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your mod order.
- Place it below the **PATCHER OUTPUT** separator and activate it.

## DynDOLOD Generation

- Run **DynDOLOD** through Mod Organizer 2.
- In the DynDOLOD Wizard window, click **Advanced**.
- In the **Advanced** window, you can see a list of all worldspaces at the top.
- Right-click inside and **Select all**.
- Under **Load rules for** check both **Candles** and **FXGlow**.
- Also check **Glow Windows**, **High** and **Fake lights in child worlds**.

Select one of the presets:

- **Low** if you struggle with performance.
- **Medium** as the default option.
- **High** for modern machines.

If you have 4GB of VRAM or more, you can generate 3D tree LOD.

- Check the box for **Ultra** next to **Generate tree LOD**.
  
Click **OK** to start generating LOD.

**Step away from your PC while DynDOLOD is working.** This may take around 20-30 minutes.

![DynDOLOD Settings](/Pictures/tpf/finalisation/dyndolod-settings.png)

## DynDOLOD Output

* Once DynDOLOD is done, click **Save & Exit**.
* Go to `Your Modding Folder\Tools\DynDOLOD`.
* Cut (CTRL+X) the **DynDOLOD_output** folder and paste it (CTRL+V) to `Mod Organizer 2\mods`.
* Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your load order.
* Place it last below the **PATCHER OUTPUT** separator and activate it.
* Move **DynDOLOD.esm** below your other ESMs at the top of your load order.
* Leave **DynDOLOD.esp** at the very bottom as the last plugin.
* Make sure both plugins are activated.