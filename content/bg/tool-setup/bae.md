---
title: "Bethesda Archive Extractor"
weight:
type: docs
description: >
  How to set up Bethesda Archive Extractor.
---

{{< alert color="info" title="Summary" >}}
> This module covers the installation of Bethesda Archive Extractor.<p>
> **Prerequisite(s):** None{{< /alert >}}

## About Bethesda Archive Extractor

**Bethesda Archive Extractor** is a lovely tool for viewing and (selectively) extracting BSAs.

## Installation

- Download [Bethesda Archive Extractor](https://www.nexusmods.com/skyrimspecialedition/mods/974?tab=files) from its Nexus page.
- Create a folder called **Bethesda Archive Extractor** in your **Modding Tools** directory.
- Extract the downloaded archive into the new folder.

### Set as default

Setting BAE as the default app for opening BSAs will allow you to quickly peek inside archives the same way you can inside 7ZIP or RAR files. This can be immensely convenient for asset management.

To set it as the default app, we need a BSA.

- Navigate to your **data folder**.
- Right-click any BSA and select **Open with**.
- Check the **Always use this app to open.bsa files** option.
- Click **More apps**, scroll all the way to the bottom, and click **Look for another app on this PC**.
- Navigate to `\Modding Tools\Bethesda Archive Extractor\` and double-click **BAE.exe**.

This will immediately open whichever BSA you picked in BAE. As you can see, there is a filtering option and you have the ability to browse and unpack files. See [Extracting BSAs](/bg/additional-modules/extracting-bsas/#via-bethesda-archive-extractor) for more information.

{{< alert color="info" >}}**Tip:** Double-clicking a BSA in Mod Organizer 2 will open MO2's own preview window which also has a filtering option and useful information about compression. However, if you right-click the BSA and select **Open**, it will use the default app (BAE) instead.{{< /alert >}}