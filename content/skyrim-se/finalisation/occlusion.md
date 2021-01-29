---
title: "Occlusion"
weight: 5
type: docs
description: >
  Instructions to regenerate Occlusion with xLODGen.
---

## SSELODGen

While SSELODGen is primarily made to regenerate terrain LOD, we are only going to use it to rebuilt occlusion data. Cathedral Landscape is already packaged with specially made terrain LOD to minimize pop-in and seams.

- Download the latest version of [xLODGen](https://forum.step-project.com/topic/13451-xlodgen-terrain-lod-beta-66-for-fnv-fo3-fo4-fo4vr-tes5-sse-tes5vr-enderal/) from MEGA (see screenshot for the link).
- Navigate to `Your Modding Folder\Tools` and create a new **SSELODGen** folder.
- Open the downloaded archive, double-click the **xLODGen** folder, and extract all files into your new directory.

![Download xLODGen](/Pictures/skyrim-se/finalisation/xlodgen-download.png)

### Add xLODGen to MO2

- In Mod Organizer 2, open the **Executables** window (Tools > Executables or CTRL + E).
- Click the blue plus icon to add a new executable and select **Add from file**.
- Navigate to `Your Modding Folder\Tools\SSELODGen` and double-click **xLODGenx64.exe**.
- Change the **Title** to **SSELODGen**.
- Under **Arguments**, add `-sse`.
- Click **OK** to close the window.

![Add xLODGen to MO2](/Pictures/skyrim-se/finalisation/add-xlodgen-to-mo2.png)

## Generate Occlusion Data

- Run **SSELODGen** through Mod Organizer 2.
- In the worldspaces window, check **Tamriel "Skyrim"** and **DLC2SolstheimWorld "Solstheim"**.
- Uncheck all options except for **Occlusion**.
- Set **Quality** to **3**.
- Set **Height** to **100**.
- Click **Generate** and wait for the process to complete.

![Generate Occlusion Data](/Pictures/skyrim-se/finalisation/generate-occlusion-data.png)

## Output

- Once SSELODGen returns `LOD generation complete`, you can close the window.
- Right-click the **Overwrite** folder in Mod Organizer 2 and select **Create mod**.
- Enter **SSELODGen - Occlusion Data** as the name and click **OK**.
- Activate the mod in the mod order.
- Make sure **Occlusion.esp** is at the bottom of your load order and checked.