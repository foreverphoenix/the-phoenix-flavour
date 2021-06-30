---
title: "DynDOLOD"
weight: 8
type: docs
description: >
  Improving distant terrain and tree LOD with TexGen and DynDOLOD.
---

## DynDOLOD and Performance

Contrary to popular belief, DynDOLOD is not inherently performance-intense. In fact, generating with the **Low** profile may even improve performance over vanilla in some places.

However, for TPF we are going to use the **High** preset with 3D tree LOD which is quite taxing, especially for people with 4GB of VRAM or less. Especially 3D tree LOD is a substantial improvement visually, however, as it replaces the vanilla 2D "cut-outs" with proper models for the leaves for a seamless transition.

*If you find High + 3D tree LOD too intense for your system, there are instructions in the Performance Guide that you can try out after completing base TPF.*

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

## INI Adjustments

Before we generate LOD with DynDOLOD, we need to tweak a few settings:

- Navigate to `\Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\`.
- Open **DynDOLOD_SSE.ini** in Notepad++.

Enable expert mode in DynDOLOD:

- In **Line 8**, set `Expert=` to `1`.

Generate a terrain underside mesh for Dynamic Volumetric Lighting and Sun Shadows:

- Uncomment **Line 270** (remove the semicolon).
- In **Line 275**, set `Terrain Underside=` to `1`.

And finally:

- Press **CTRL + S** to save your changes and close the window.

![DynDOLOD INI Tweaks](/Pictures/tpf/finalisation/dyndolod-ini-tweaks.png)

## TexGen

Some of the TexGen settings were adopted from the [STEP guide for SSE](https://stepmodifications.org/wiki/SkyrimSE:2.0.0#Run_TexGen). The STEP team is known for extensively testing these settings.

- Launch **TexGen** through Mod Organizer 2.
- Under **Stitched Object LOD Textures**, set **Texture size** to `512`.
- Under **Rendered Object LOD Textures**, set **Texture size** to `512`.
- Under **Trees/Grass Billboards**, check the boxes for **Tree**, **HD Tree**, and **Rendered**.
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

DynDOLOD has a multitude of features and settings through which performance impact and visual improvements can be balanced out. I've chosen to defer to the expertise of the STEP team who have spend vastly more time than me experimenting with various DynDOLOD settings. With their permission, I have included their Optimal preset for DynDOLOD 3.00 created for the [STEP Skyrim SE guide](https://stepmodifications.org/wiki/SkyrimSE:2.0.0).

### DynDOLOD Preset

- Click [here](https://stepmodifications.org/wiki/images/3/30/DynDOLOD_SSE_Optimal.ini) to download the STEP Optimal preset for DynDOLOD.
- Save the **DynDOLOD_SSE_Optimal.ini** to `\Your Modding Folder\Tools\DynDOLOD\Edit Scripts\DynDOLOD\Presets\`.
- Open the INI file in Notepad++.
- Near the top, in **Line 2**, change the output folder to be within your DynDOLOD installation folder.
- For me, that would be: `F:\Modding\Skyrim SE Mods\Tools\DynDOLOD 3.0 Alpha 33\DynDOLOD_Output\`.
- Save your changes and close Notepad++.

![DynDOLOD Preset Output](/Pictures/tpf/finalisation/dyndolod-preset-output.png)

### Run DynDOLOD

- Run **DynDOLOD** through Mod Organizer 2.
- Make sure all worldspaces in the top left box are ticked.
- Click **Load Preset** (one of the buttons on the bottom left).
- The DynDOLOD Presets folder should be opened automatically, double-click the **DynDOLOD_SSE_Optimal.ini**.
- Click **OK** to start generating LOD.

**Step away from your PC while DynDOLOD is working.** This may take around 20-30 minutes.

![DynDOLOD Settings](/Pictures/tpf/finalisation/dyndolod-settings.png)

### DynDOLOD Output

- Once DynDOLOD is done, click **Save & Exit**.
- Navigate to `\Your Modding Folder\Tools\DynDOLOD\`.
- Cut (CTRL+X) the **DynDOLOD_Output** folder and paste it (CTRL+V) to `\Mod Organizer 2\mods\`.
- Refresh Mod Organizer 2 (F5) and it will appear at the bottom of your load order.
- Place it last below the **PATCHER OUTPUT** separator and activate it.
- Move **DynDOLOD.esm** below your other ESMs at the top of your load order.
- Leave **DynDOLOD.esp** at the very bottom as the last plugin.
- Make sure both plugins are activated.