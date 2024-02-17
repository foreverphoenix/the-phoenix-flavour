---
title: "Downgrade Skyrim"
weight:
type: docs
description: >
  How to downgrade to an older version of Skyrim.
---

{{< alert color="info" title="Summary" >}}
> This module covers how to revert to an older version of Skyrim.<p>
> **Prerequisite(s):** [Clean Install](/skyforge/modding-resources/clean-install){{< /alert >}}

If there has been a recent Skyrim SE update, this guide (and possibly the rest of the modding community) may not have caught up yet in which case <u>downgrading to the last supported version of Skyrim is recommended</u>. You can either use halgari’s automatic downgrade patcher or do it manually through the Steam console.

Perform a [Skyrim Version Check](/skyforge/modding-resources/skyrim-version-check/) to find out which version you have installed.

- [Skyrim SE Patch Notes](https://en.uesp.net/wiki/Skyrim:Special_Edition_Patch) on UESP.net

## Unofficial Skyrim Downgrade Patcher

{{< alert color="warning" >}}Neither the Downgrade Patcher nor the Skyrim Downloader can currently downgrade from **Skyrim SE 1.6.1170**. Use the manual method instead.{{< /alert >}}

- Determine which version of **Skyrim SE** you are on and which version you require ([instructions](/skyforge/modding-resources/skyrim-script-extender/#version-check)).
- Download the corresponding full patcher from [the mod page](https://www.nexusmods.com/skyrimspecialedition/mods/57618?tab=files) (click **Manual Download**).
  - You will probably find the required version under **Old Files** (use CTRL+F to search).
- Move the downloaded executable to your installation under `\Steam\steamapps\common\Skyrim Special Edition\`.
- Run the executable and wait for it to finish (should take only a few seconds).

{{< alert color="info" >}}Alternatively, you can use halgari’s [Unofficial Skyrim Downloader](https://www.nexusmods.com/skyrimspecialedition/mods/61756). I will add instructions for this at a later date.{{< /alert >}}

## Manual Method

If it is not possible to use either automated solution, you can downgrade manually by using the Steam console.

- Press the **Windows** key + **R**.
- Enter `steam://open/console` and press Enter.

![Open Steam Console](/Pictures/skyforge/modding-resources/downgrade-skyrim/open-steam-console.png)

This will open the **Console** view in Steam through which we can now directly download depot files.

- Run the following lines in the console <mark>one by one</mark>:
  - `download_depot 489830 489831 3660787314279169352`
  - `download_depot 489830 489832 2756691988703496654`
  - `download_depot 489830 489833 5291801952219815735`

This will download the files for **Skyrim SE 1.6.640.0**. Because of the file size it will take a while.

![Download from Depot](/Pictures/skyforge/modding-resources/downgrade-skyrim/download-from-depot.png)

All depot files will be downloaded to the following location:

```
/Steam/steamapps/content/app_489830/
```

- Copy the files from each of the three **depot_xxxxxx** folders into your Skyrim **Root** folder and overwrite.

This will completely revert all game files to **1.6.640.0**. As a consequence, the new Creations Menu is completely disabled.

### Creations

With this method only the four free creations will be reverted to the older versions. **You can skip this** and choose not to overwrite the files. If you own the AE DLC and downloaded it during the [Clean Install](/skyforge/modding-resources/clean-install/) step, you should be able to run the creations (free and paid) from 1.6.1170.0 in SSE 1.6.640.0 without issues so long as you install the Backported Extended ESL Support (see next section). Otherwise, CC Fishing will cause crashes.

### Backported Extended ESL Support

The 1.6.1130.0 update doubled the amount of Form IDs that be stored in [ESL Plugins](/skyforge/knowledge-base/esl-plugins/). So far, only some official files use Form IDs in the new range, but in time new mods with plugins will be released that do, too. In order to prevent crashes with these plugins in SSE 1.6.640.0 you should absolutely install the [Backported Extended ESL Support](/skyforge/mod-recommendations/utilities-frameworks/) by Nukem. 

---

#### Next Steps

- To prevent Skyrim from automatically updating in the future, consider [Update Proofing](/skyforge/modding-resources/update-proofing) the game.
- [MO2 Setup](/skyforge/tool-setup/mo2/)