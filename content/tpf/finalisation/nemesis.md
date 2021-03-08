---
title: "Nemesis Behavior Engine"
weight: 3
type: docs
description: >
  Generating Nemesis.
---

## Nemesis Setup

**Nemesis Unlimited Behavior Engine** is a tool used to add custom animations to Skyrim. It is an open-source replacement and upgrade for FNIS, and required for several animation-related mods in TPF.

Nemesis will generate a number of files specifically for your setup. In order to simplify the file management, we will set up an output folder ahead of time.

### Nemesis Output Folder

- In Mod Organizer 2, click the tools icon above your mod order and select **Create empty mod** (see picture below).
- Rename the new mod folder to **Nemesis Output**.
- Drag the new empty mod (displayed in grey italics) below the **PATCHER OUTPUT** separator and activate it.

![Create Empty Mod](/Pictures/tpf/finalisation/create-empty-mod.png)

## Add Nemesis to MO2

* Open the **Executables** window in Mod Organizer 2 (Tools > Executables or CTRL + E).
* Click the blue plus icon and select **Add from file**.
* Navigate to `Mod Organizer 2\mods\Nemesis Unlimited Behavior Engine\Nemesis_Engine`.
* Double-click **Nemesis Unlimited Behavior Engine.exe**.
* Check the **Create files in mod instead of overwrite** checkbox and select **Nemesis Output** from the drop down menu.
* Click **OK** to close the Tools window.

![Add Nemesis to MO2](/Pictures/tpf/finalisation/add-nemesis-to-mo2.png)

## Generate Nemesis

- Run **Nemesis** (the executable we just added) through Mod Organizer 2.
- There will be two warnings about missing (not yet generated) cache, click **OK** to both.
- In Nemesis, a number of patches are available for mods that are not included in TPF. Do not check any of the boxes.
- Click the **Update Engine** button and wait for the process to be completed.
- When it's done, click the big **Launch Nemesis Behavior Engine** button.
- Nemesis will return `Behavior generation complete` after a few seconds and you can close the tool.
- Back in Mod Organizer 2, press F5 to refresh and you can see that files were added to the **Nemesis Output** mod folder.
- A **FNIS.esp** will appear at the bottom of your load order. Activate it.

> FNIS.esp is an empty dummy plugin used to trick XPMSSE, the skeleton replacer, into thinking it's actually present in the load order. Functionally, FNIS is replaced by Nemesis.