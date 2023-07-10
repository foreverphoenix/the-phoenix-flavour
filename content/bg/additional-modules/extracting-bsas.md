---
title: "Extracting BSAs"
weight:
type: docs
description: >
  How to extract Bethesda Softworks Archives (BSAs).
---

{{< alert color="info" title="Summary" >}}
> This module covers various methods of extracting BSAs.<p>
> **Prerequisite(s):** Depends on the method{{< /alert >}}

## Extraction Methods

You need to extract a BSA if:

1. You want to install a Skyrim LE mod that contains a BSA (it would crash the game).
2. You want assets from the BSA to overwrite loose files.
3. You want to selectively modify or remove assets from the BSA.

(Going through MO2 is easily the most convenient option. Use BAE for selective extraction or for BSAs outside of MO2.)

### Through Mod Organizer 2

If a mod is already installed via Mod Organizer 2, you can extract it through the MO2 interface.

{{< alert color="warning" >}}Please make sure you have [BSA Extractor 2](https://www.nexusmods.com/skyrimspecialedition/mods/92044?) installed. Check the [Mod Organizer 2](/bg/tool-setup/mo2/#bsa-extractor-2) page for instructions.{{< /alert >}}

- In Mod Organizer 2, switch to the **Archives** tab.

Here, you will find all currently installed archives (BSAs). If they are checked, it means there is a plugin of the same name to load it.

- Right-click the BSA and select **Extract**.
  - *If a mod has multiple BSAs and you want to extract all of them, right-click the **mod name** instead.*
- Navigate to `\Mod Organizer 2\mods\<mod name>\` and confirm.

This will extract the BSA into the mod folder. You can delete the BSA afterwards.

{{< alert color="info" >}}You can also extract the BSA to a different location or a new mod folder if you only want partial/temporary access.{{< /alert >}}

![Extract through MO2](/Pictures/bg/additional-modules/extracting-archives/extract-through-mo2.png)

### Via Bethesda Archive Extractor

[Bethesda Archive Extractor](/bg/tool-setup/bae/) is probably the most versatile tool for extracting BSAs (perhaps the name gave it away). It allows you to unpack one BSA at a time, either in its entirety or in parts. You can also extract files and folders via simple drag-and-drop.

The instructions linked above cover how to set BAE as the default app for BSAs. 

- View any BSA by double-clicking it or by going through the MO2 **Filetree**, right-clicking the BSA, and selecting **Open**.
- Click **Extract** to select a target folder to extract all currently checked assets to (all assets are checked by default).

Uncheck the BSA and check files or folders to selectively extract from the archive:

![BAE Selective Extraction](/Pictures/bg/additional-modules/extracting-archives/bae-selective-extraction.png)

### Via Cathedral Assets Optimizer

You can create a dedicated profile in [Cathedral Assets Optimizer](/bg/tool-setup/cao/) for extracting BSAs.

- Click the **New** button to create a new profile and use the **SSE** profile as the basis.
- Disable everything except for the **Extract BSA** and **Delete Backups** options in the **BSA** tab.

{{< alert color="info" >}}**Delete Backups:** CAO will usually create backups of the extracted BSAs in the same folder. If you want to recover the BSAs it is usually easier to reinstall the mod through Mod Organizer 2 which is why I recommend setting CAO to delete the backups.{{< /alert >}}

To extract a BSA using CAO, click **Open Directory** and navigate to the location of the BSA. Click **Select Folder**. CAO will extract the assets from <u>all BSAs within that folder</u> into the same folder.