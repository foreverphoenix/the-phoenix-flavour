---
title: "Occlusion"
weight: 9
type: docs
description: >
  Regenerating Occlusion with SSLODGen.
---

## Generate Occlusion Data

We already installed SSELODGen for terrain LOD earlier so we simply need to fire it up again to generate Occlusion. Occlusion essentially tells the game what is visible to the player and must be rendered while invisible objects (on the other side of a mountain for instance) don't have to be rendered at the time.

This will also fix the giant hole in the Sea of Ghosts behind Winterhold.

- Run **SSELODGen** through Mod Organizer 2.
- In the worldspaces window, check **Tamriel "Skyrim"** and **DLC2SolstheimWorld "Solstheim"**.
- Uncheck all options except for **Occlusion**.
- Set **Quality** to **3**.
- Set **Height** to **100**.
- Click **Generate** and wait for the process to complete.

> Occlusion generation is very CPU intense and will likely hold your processor load at 100% for the duration. You absolutely have to step away from your PC while it generates if you don't want to risk a complete crash / blue screen.

![Generate Occlusion Data](/Pictures/tpf/finalisation/generate-occlusion-data.png)

### Output

- Once SSELODGen returns **LOD generation complete**, you can close the window.
- Right-click the ***Overwrite*** folder in Mod Organizer 2 and select **Create mod**.
- Enter **SSELODGen - Occlusion Data** as the name and click **OK**.
- Activate the mod in the mod order.
- Make sure **Occlusion.esp** is at the bottom of your load order and active.