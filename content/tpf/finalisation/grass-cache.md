---
title: "Grass Cache"
weight: 7
type: docs
description: >
  Generating grass cache.
---

## About Grass Cache

Grass cache is generated using No Grass In Objects, a mod we installed and configured earlier in the [Essential Mods](/tpf/mod-installation/essential-mods) step. This will allow us to use NGIO's extended grass feature so grass is rendered further in the distance until it blends with terrain LOD (almost) seamlessly.

### MO2 Plugin

- Close Mod Organizer 2.
- Open the Nexus page for [No Grass In Objects](https://www.nexusmods.com/skyrimspecialedition/mods/42161?tab=files).
- Under **Optional Files**, manually download **Grass Generation MO2 Plugin v1**.
- Open the download archive and extract **GrassPrecacher.py** to `Mod Organizer 2\plugins`.
- Restart Mod Organizer 2.

## Grass Generation

Generating grass cache takes a good chunk of time. Skyrim is launched and will be displaying the loading screen during the entire process. It can and will crash any number of times in which case the MO2 plugin will automatically restart it. **Stay away from your PC until the process is complete.** There will be a small message box informing you when grass cache was fully generated.

- In Mod Organizer 2, there will be a new **Precache Grass** option under **Tools**.
- Select it to begin the grass generation process.
- A warning will pop up. If you are ready, click **Yes**.

![Start Grass Cache](/Pictures/tpf/finalisation/start-grass-cache.png)

## Output

- When the message box pops up - **Grass generation finished successfully!** - click **OK**.
- Back in Mod Organizer 2, you will be informed that grass cache was successfully generated, click **OK** again.
- Double-click your ***Overwrite*** and delete the **NetScriptFramework** folder inside (it contains grass cache crash logs).
- Close the ***Overwrite*** again and right-click it.
- Select **Create Mod** and name it **Grass Cache**.
- Right-click the new mod and select **Ignore missing data**.
- Activate the mod in your mod order.