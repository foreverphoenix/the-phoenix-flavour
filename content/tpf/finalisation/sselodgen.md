---
title: "SSELODGen"
weight: 6
type: docs
description: >
  Generating terrain LOD textures with SSELODGen.
---

## Installation

SSELODGen is a tool for regenerating various LOD (level-of-detail) resources. We will be using it to generate better terrain LOD (distant ground textures) since the vanilla terrain LOD is of extremely low quality. This will also improve distant grass blending. Tree LOD and object LOD are much better handled with DynDOLOD (which is done in the next step) but afterwards we will once again use SSELODGen for Occlusion generation.

- Download the latest version of [SSELODGen](https://forum.step-project.com/topic/13451-xlodgen-terrain-lod-beta-66-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal/) from MEGA (see screenshot for the link).
- Navigate to `Your Modding Folder\Tools` and create a new **SSELODGen** folder.
- Open the downloaded archive, double-click the **xLODGen** folder, and extract all files into your new directory.

![Download xLODGen](/Pictures/tpf/finalisation/xlodgen-download.png)

### Add SSELODGen to MO2

- In Mod Organizer 2, open the **Executables** window (Tools > Executables or CTRL + E).
- Click the blue plus icon to add a new executable and select **Add from file**.
- Navigate to `Your Modding Folder\Tools\SSELODGen` and double-click **xLODGenx64.exe**.
- Change the **Title** to **SSELODGen**.
- Under **Arguments**, add `-sse -o:"...\Your Modding Folder\Tools\SSELODGen\Output\"` (change to full file path on your system).
- Click **OK** to close the window.

![Add xLODGen to MO2](/Pictures/tpf/finalisation/add-xlodgen-to-mo2.png)

## SSE-Terrain-Tamriel

- In the [SSELODGen](https://stepmodifications.org/forum/topic/13451-xlodgen-terrain-lod-beta-76-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal-enderalse/) post on the STEP forum, scroll down to **Recommended Optionals**.
- Click the **SSE-Terrain-Tamriel-Extended.esm** link (see screenshot).
- Download the file from MEGA.
- Create a new folder: `Mod Organizer 2\mods\SSE-Terrain-Tamriel-Extended`.
- Move the downloaded ESM into the new folder.
- In Mod Organizer 2, press F5 to refresh. The new mod will show up at the bottom of your load order.
- Place the mod anywhere below the **PATCHER OUTPUT** separator and enable it.
- In the load order, drag the new plugin up all the way below **Lanterns Of Skyrim II.esm**.
- Make sure the plugin is checked.

![SSE-Terrain-Tamriel](/Pictures/tpf/finalisation/download-lodgen-esm.png)

## Terrain LOD Generation

- Run **SSELODGen** through Mod Organizer 2.
- Wait for the tool to load your mods.
- Right-click in the **Worldspaces** window and **Select All**.
- On the right side, only **Terrain LOD** should be checked.
- Mirror the settings for all LOD levels (LOD4, LOD8, LOD16, LOD32) below.
- Click **Generate** to begin the process. This may take a while (around 40-50 minutes for me).

*All credits to TechAngel - we're using [his custom settings](https://stepmodifications.org/forum/topic/15184-xlodgen-terrain-settings-compare/?tab=comments#comment-242372).*

### LOD4 Settings

![SSELODGen LOD4](/Pictures/tpf/finalisation/sselodgen-lod4.png)

### LOD8 Settings

![SSELODGen LOD8](/Pictures/tpf/finalisation/sselodgen-lod8.png)

### LOD16 Settings

![SSELODGen LOD16](/Pictures/tpf/finalisation/sselodgen-lod16.png)

### LOD32 Settings

![SSELODGen LOD32](/Pictures/tpf/finalisation/sselodgen-lod32.png)

## Output

- Once the LOD generation is complete, close **SSELODGen**.
- Navigate to `Your Modding Folder\Tools\SSELODGen`.
- Rename the new **Output** folder inside to **SSELODGen - Terrain LOD**.
- Move the folder to `Mod Organizer 2\mods`.
- In Mod Organizer 2, press F5 to refresh.
- Activate the new mod in the mod order.
- Disable **SSE-Terrain-Tamriel-Extended** in the mod order.

## AQWM Conflict

The mod **A Quality World Map** is editing terrain LOD textures to add roads and other improvements to the map. Unfortunately these edited textures are now overwritten by the generated terrain LOD. We could potentially solve this problem by packing the generated terrain LOD files into a BSA so the loose files from A Quality World Map overwrite, but at the end of the day it is much faster to simply hide the conflicting files from the xLODGen output.

- Double-click **SSELODGen - Terrain LOD** in your mod order.
- Switch to the **Conflicts** tab and select **Advanced**.
- Click the **Overwrites** column to sort by overwriting mods.
- Highlight all files shown to overwrite A Quality World Map.
- Right-click them and select **Hide**.
- Close the window.

![AQWM Terrain LOD Conflict](/Pictures/tpf/finalisation/aqwm-xlodgen-conflict.png)